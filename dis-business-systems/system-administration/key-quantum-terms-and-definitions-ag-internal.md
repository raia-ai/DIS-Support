---
title: "Key Quantum Terms and Definitions - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Key Quantum Terms and Definitions - Ag Internal."
long_description: "This document provides internal system administration information about Key Quantum Terms and Definitions - Ag Internal."
---

_Key Quantum Terms and Definitions - AG Internal_

CentOS/Ubuntu – This is the underlying Operating system that the Quantum servers use. Like your PC uses Windows, Quantum servers use CentOS or Ubuntu.
 Docker – This is the backbone of the Quantum server. This program manages and maintains the Quantum services. This also allows us to manage individual services on the quantum server without interfering with other areas. (user connections)
 SSH/PuTTY/BitVise – These programs all provide the same function. They allow you to connect directly to a Quantum servers command line. You can think of it as ‘GreenScreen’ for Quantum.
 Utilservlet – This is the workhorse for everything that Quantum does outside of greenscreen functions. Display, Email, Report Center, Datamine, *360, EasyFile, UnitPics, etc. all use the Utilservlet to function correctly.
 Service Logistics Servlet – This controls all Middle tier feeds from the Quantum server and serves the middle tier requests for any API integration. (MyPortal, Quantum API, Service Logistics, etc.)
 Apache/webproxy – This is the program/container that manages web connections to the server. This is used for QRA login and general web page loading.
 Tomcat/appserver – This is the program/container that manages the DIS applications. This is where the Utilservlet and Webclient applications are running. If you can load the webpage but the login fails to load, your problem lies here or in the LSEngine.
 LSengine – This is the backend connection to the AS400. The LSengine manages user sessions and provides panels from the AS400 screens. Most engine errors are displayed in pop-ups on the screen. “Connection is lost...” “Cannot communicate with server on port 1291.”
 SOLR – (Do not confuse with SLOR; a different DIS product.) This is the search database for Customer 360. Getting no search results can indicate a problem here.
 Portainer – This is the management/admin portal for Docker-based Quantum servers. Here we can manage individual services and change configuration files.
 Stack – This is the configuration of the services that are running in Docker. The stack consists of all necessary components for Quantum to function. These include Services, Volumes, and Networks.
 Services – These are the individual containers that run the Quantum applications. webproxy, appserver, SOLR, lsengine, etc. These can be updated and refreshed individually.