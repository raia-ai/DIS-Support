---
title: "Powershell Script to Add or Remove KPS Settings on Host Computer - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Powershell Script to Add or Remove KPS Settings on Host Computer - AG Internal."
long_description: "This document provides internal system administration information about Powershell Script to Add or Remove KPS Settings on Host Computer - AG Internal."
---

Copy and paste the script below in a Powershell window to edit KPS configuration on host PC. 

 
#Script to add and remove the KPS settings in Legap.ini and Legasuite.ini
function writeLegap {
 $dev = Read-Host -Prompt "Please enter the DIS printer device name. Example P2 or A6"
 (Get-Content -Path "C:\Program Files (x86)\DIS\Keystone\legap.ini") | ForEach-Object {
 if ($_ -like "PrinterDevice=") {
 "PrinterDevice=$dev"
 } else {
 $_
 }
 } | Set-Content -Path "C:\Program Files (x86)\DIS\Keystone\legap.ini"
}
#Set Legasuite.ini to the DefaultPrinter=DEFAULT
function writeLegasuite {
 (Get-Content -Path "C:\Program Files (x86)\DIS\Keystone\legasuite.ini") | ForEach-Object {
 if ($_ -like "DefaultPrinter=") {
 "DefaultPrinter=DEFAULT"
 } else {
 $_
 }
 } | Set-Content -Path "C:\Program Files (x86)\DIS\Keystone\legasuite.ini"
}
function clearConfig {
 function removeLegap {
 (Get-Content -Path "C:\Program Files (x86)\DIS\Keystone\legap.ini") | ForEach-Object {
 if ($_ -like "PrinterDevice=*") {
 "PrinterDevice="
 } else {
 $_
 }
 } | Set-Content -Path "C:\Program Files (x86)\DIS\Keystone\legap.ini"
}
 function removeLegasuite {
 (Get-Content -Path "C:\Program Files (x86)\DIS\Keystone\legasuite.ini") | ForEach-Object {
 if ($_ -like "DefaultPrinter=*") {
 "DefaultPrinter="
 } else {
 $_
 }
 } | Set-Content -Path "C:\Program Files (x86)\DIS\Keystone\legasuite.ini"
}
removeLegap
removeLegasuite 
}
clearConfig

function kps_Select {
write-output "1) Configure Keystone for KPS printer" | out-host
write-output "2) Remove KPS settings from Computer" | out-host 
$choice = Read-Host “Enter the number corresponding to the command”
switch ($choice) {
 '1' {
 writeLegap
 writeLegasuite
 }
 '2' {
 clearConfig
 }
 default {
 Write-Host "Invalid selection" -ForegroundColor Red
 }
 }
}
Clear-Host
kps_Select