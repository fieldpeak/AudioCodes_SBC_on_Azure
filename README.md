# Deploy an AudioCodes Session Border Controller on Azure
Deployment repo for AudioCodes SBC deployed on Microsoft Azure

## v1.0

### Azure_Create_1_ACvSBC - Az.ps1

This PowerShell script will deploy a single AudioCodes Session Border Controller with all required networking for the 2x Interfaces on Azure. It has several fields pre-populated for easy deployment and is recommeneded that this script be used to deploy Proof of Concept or testing environments only.

**Requirements:

Install the "AZ" PowerSehll module before using this script;

Install-Module Az

*** ***NOTE: Default password is "DirectRouting123!@#" and MUST BE CHANGED AS SOON AS POSSIBLE !!!

### Azure_AudioCodes_VE_SBC_Default_Config.ini

This .INI file contains the basics for configuring the AudioCodes Session Border Controller for Microsoft Teams Direct Routing. Download the .INI and edit the following changes:

Row 213: Replace SIP.TRUNK.IP.HERE with the routable IP address of your SIP Trunk Provider

Row 277: Replace the SBC.PSTN.IP.HERE with the Public facing Internet IP Address for the PSTN network provided at the end of the PowerShell script

Row 278: Replace the SBC.TEAMS.IP.HERE with the Public facing Internet IP Address for the TEAMS network provided at the end of the PowerShell script
