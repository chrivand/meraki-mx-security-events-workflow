![License: CISCO](https://img.shields.io/badge/License-CISCO-blue.svg)

# SecureX Orchestration Workflow to Retrieve and Parse Meraki MX Security Events
This sample workflow will retrieve all security events from Meraki for a specific Org ID. It will then filter out Malware Downloaded and IDS Priority 1 events. It then sends deatils for this to a Webex  Teams space. Please make sure to set the 3 variables ('api key meraki', 'api key webex', 'webex space ID' and 'Meraki Org ID') before running. You can also run this  scheduled by enabling a trigger.

## Features
* Retrieve Meraki MX security events.
* Filter out high priority events, right now: "Malware Downloaded" and "IDS Priority 1" events.
* Send Webex Teams notification to Space of choice.
* Possibility to run scheduled or based on trigger.

## Installation
1. Browse to your SecureX orchestration instance. For example this is the URL for US based instances: https://securex-ao.us.security.cisco.com/orch-ui/workflows/
2. Click on **IMPORT** to import the workflow:

![](screenshots/import-workflow.png)

3. Click on **Browse** and copy paste the content of the [meraki-mx-security-events.json](https://raw.githubusercontent.com/chrivand/meraki-mx-security-events-workflow/master/meraki-mx-security-events.json) file inside of the text window. 

![](screenshots/copy-paste.png)

4. Click on **IMPORT**. You will now receive an error that information is missing: 

![](screenshots/missing-info.png)

5. Click on update and fill in the Meraki and Webex API key. These are not stored as plain text, as they are stored as "secure strings" in SecureX.

> **Note:** To obtain your Meraki API key, please follow these steps: https://documentation.meraki.com/zGeneral_Administration/Other_Topics/The_Cisco_Meraki_Dashboard_API

> **Note:** Please retrieve your Webex key from: [https://developer.webex.com/docs/api/getting-started](https://developer.webex.com/docs/api/getting-started). Please be aware that the personal token from the getting started page only works for 12 hours. Please follow these steps to request a "bot" token: https://developer.webex.com/docs/integrations.

6. You are still missing 2 more values before you are done. Click on the workflow like below, and let's fill in the Meraki Org ID and Webex Team space ID.

![](screenshots/import-succes.png)

7. Click on the `Meraki Org ID` variable and fill in the Org ID of the Meraki organization that you want to track security events for. More info on this can be found here: https://documentation.meraki.com/zGeneral_Administration/Other_Topics/The_Cisco_Meraki_Dashboard_API#Organizations

![](screenshots/workflow-variables.png)

8. Next click on `webex space ID`. You can create a new space or find an existing one via these link: retrieve the Room ID from: https://developer.webex.com/docs/api/v1/rooms/list-rooms. 

9. Now it is time to test, click on **RUN** in the top right of your window, and eveyrhting shopuld be working now. If not try troubleshooting by click on the activity that is colored red. 

![](screenshots/run.png)

10. As a final step you could choose to schedule this workflow. 

![](screenshots/schedule.png)

## Notes

* Please test this properly before implementing in a production environment. This is a sample workflow!

## Author(s)

* Christopher van der Made (Cisco)
