![License: CISCO](https://img.shields.io/badge/License-CISCO-blue.svg)

# SecureX Orchestration Workflow to Retrieve and Parse Meraki MX Security Events
This sample workflow will retrieve all security events from Meraki for a specific Org ID. It will then filter out Malware Downloaded and IDS Priority 1 events. It then sends deatils for this to a Webex  Teams space. Please make sure to set the 3 variables ('api key meraki', 'api key webex', 'webex space ID' and 'Meraki Org ID') before running. You can also run this  scheduled by enabling a trigger.

## Features
* Retrieve Meraki MX security events.
* Filter out high priority events, right now: "Malware Downloaded" and "IDS Priority 1" events.
* Send Webex Teams notification to Space of choice.
* Possibility to run scheduled or based on trigger.

## Installation
1. 

6. It is possible to integrate the script with Webex Teams. In order to do that, an API Access Token and a Room ID need to be entered in the config.json file. Please retrieve your key from: [https://developer.webex.com/docs/api/getting-started](https://developer.webex.com/docs/api/getting-started). Then create a dedicated Webex Teams space for these notifications and retrieve the Room ID from: [https://developer.webex.com/docs/api/v1/rooms/list-rooms](https://developer.webex.com/docs/api/v1/rooms/list-rooms). Please be aware that the personal token from the getting started page only works for 12 hours. Please follow these steps to request a "bot" token: [https://developer.webex.com/docs/integrations](https://developer.webex.com/docs/integrations). 


## Notes

* Please test this properly before implementing in a production environment. This is a sample workflow!

## Author(s)

* Christopher van der Made (Cisco)
