---
title: "DataGrip Scripts and Queries for Service Logistics Plus - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about DataGrip Scripts and Queries for Service Logistics Plus - Ag Internal."
long_description: "This document provides internal system administration information about DataGrip Scripts and Queries for Service Logistics Plus - Ag Internal."
---

-- Tech-Specific Middle Tier Queries: 

 -- CHANGELOG 

 -- 2025-04-14 -- Basic tech query cleanup 

 -- 2024-11-05 -- Added simple tech inventory query 

 -- 2024-01-26 -- Added insert_system_request_sl_plus, SL Go 

 -- 2023-06-28 -- added new columns from web user history 

 -- 2023-05-08 -- Added Last Tech connection 

 -- 2022-12-01 -- Added query to show all WOs assigned to a Tech 

 -- **************************************a 

 -- Set Timezone to PST 

 SET time zone 'america/los_angeles'; 

 -- ************************************** 

 -- Use this to find Tech's web_user_id 

 SELECT * FROM web_user WHERE lower(description) ilike '%TECHNAME%'; 

 -- ************************************** 

 -- Lookup Tech Branch info 

 SELECT web_user.description as Web_User_Name, web_user.web_id as Web_User_WebID, web_user.external_key as Web_User_External_Key, web_user.email, department.description as Department, branch.branch_number as "branch_#", branch.description as branch_Name, branch.time_zone, branch.web_id as Branch_WebID, department.web_id as Department_WebID, truck.external_key as Truck_External_Key, role.external_key as Role_External_Key 

 FROM web_user 

 JOIN department on web_user.main_department_id = department.web_id 

 JOIN branch on web_user.main_branch_id = branch.web_id 

 LEFT JOIN truck on web_user.web_id = truck.user_id 

 LEFT JOIN web_user_role on web_user.web_id = web_user_role.web_user_id 

 LEFT JOIN role on web_user_role.role_id = role.web_id 

 WHERE web_user.web_id = TECHWEBID; 

 -- ************************************** 

 -- Find all WOs that are currently assigned to a Tech: 

 SELECT os.web_id AS os_web_id, oh.order_document_id AS "WO#", os.date_created AS os_date_created, os.date_updated AS os_date_updated, oh.date_updated AS oh_date_updated, 

 os.enterprise_id AS ent_id, enterprise.description, os.order_header_id AS oh_web_id, os.internal_segment_id, os.segment_name, os.date_opened, os.date_closed, os.web_status, 

 os.internal_status, os.date_started, os.date_work_completed, os.date_customer_signed, os.date_client_completed, os.comments AS os_slor_comments 

 FROM order_segment os 

 JOIN order_header oh ON os.order_header_id= oh.web_id 

 JOIN enterprise on oh.enterprise_id = enterprise.web_id 

 join order_technician ot on os.web_id = ot.order_segment_id 

 WHERE ot.user_id = TECHWEBID 

 AND internal_status = 0 -- is not INVOICED 

 AND os.segment_type <> 1 --is not a QUOTE 

 AND os.deleted = false 

 AND oh.deleted = false 

 AND ot.deleted = false --is ASSIGNED to the Tech 

 --AND order_document_id is not null 

 ORDER BY os.date_created desc; 

 -- ************************************** 

 -- Tech Recent System_Requests 

 SELECT system_request.web_id as "Web_Id", enterprise.description as "Enterprise", web_user.description as "Tech", system_request.web_user_id, system_request.type, system_request.status, 

 system_request.parameters, system_request.results->0->'result', system_request.date_created, system_request.date_updated, system_request.date_requested, 

 system_request.date_completed, system_request.to_address 

 FROM system_request 

 JOIN web_user on system_request.web_user_id = web_user.web_id 

 JOIN enterprise on web_user.enterprise_id = enterprise.web_id 

 WHERE web_user.web_id = TECHWEBID 

 ORDER BY date_created DESC 

 LIMIT 20; 

 -- ************************************** 

 -- Dup_Sync_Entity Database Cleanup Script. SL PLUS Only! 

 SELECT insert_system_request_sl_plus(TECHWEBID, 'YOUR.NAME@discorp.com', '00001234', 'DATABASE_CLEANUP'); 

 SELECT insert_system_request_sl_go(TECHWEBID, 'YOUR.NAME@discorp.com', '00001234', 'DATABASE_CLEANUP'); 

 -- ************************************** 

 -- Trigger_Unsent to be sent after Cleanup script 

 SELECT insert_system_request_sl_plus(TECHWEBID, 'YOUR.NAME@discorp.com', '00001234', 'TRIGGER_UNSENTS'); 

 SELECT insert_system_request_sl_go(TECHWEBID, 'YOUR.NAME@discorp.com', '00001234', 'TRIGGER_UNSENTS'); 

 -- ************************************** 

 -- Tech DB Request 

 SELECT insert_system_request_sl_plus(TECHWEBID, 'YOUR.NAME@discorp.com', '00001234', 'DATABASE_TRANSMISSION'); 

 SELECT insert_system_request_sl_go(TECHWEBID, 'YOUR.NAME@discorp.com', '00001234', 'DATABASE_TRANSMISSION'); 

 -- ************************************** 

 -- Review Recent System_Requests 

 SELECT sr.web_id as "Web_Id", enterprise.description as "Enterprise", web_user.description as "Tech", sr.web_user_id, sr.type, sr.status, sr.parameters, sr.results->0->'result', sr.date_created, sr.date_updated, sr.date_requested, sr.date_completed, sr.support_ticket_number ,sr.to_address 

 FROM system_request sr 

 JOIN web_user on sr.web_user_id = web_user.web_id 

 JOIN enterprise on web_user.enterprise_id = enterprise.web_id 

 ORDER BY date_created desc LIMIT 200; 

 -- ************************************** 

 -- Cancel System Request 

 UPDATE system_request set date_updated = now(), status = 'CANCELED' where web_id in (WEB_ID); 

 -- END