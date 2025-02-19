# SAP Automation Pilot
The goal of SAP Automation Pilot is to simplify and automate complex manual technical processes and flows. This enables DevOps teams to run their solutions on SAP BTP with minimal operational effort.

## SAP Automation Pilot is a low-code / no-code automation engine that allows you to:
- Automate sequences of steps,
- Execute scripts in a serverless manner,
- Use catalogs of commands provided by SAP to automate typical Ops tasks in and outside your SAP BTP landscape,
- Build custom automations.

Automations in SAP Automation Pilot can be triggered in various ways to best fit your operational needs - manually by the DevOps team, through the built-in scheduler, automatically via integration with services and ops platforms like SAP Cloud ALM, or by other applications and systems.

The service is designed to work with low latency, even under a heavy workload, and is capable of triggering hundreds of automations simultaneously.

## Use Case Implementation
To implement the desired solution, complete the following steps (use the links to explore the actions in detail):
- Integrate SAP Alert Notification service for SAP BTP with SAP Cloud ALM and activate the switch in SAP Cloud ALM for "SAP BTP: Application Crash".
- Integrate SAP Automation Pilot with SAP Cloud ALM.
- Configure SAP Alert Notification service for SAP BTP to start collecting the application audit events for Cloud Foundry.
- Create an automation flow in SAP Automation Pilot to enable an automated response to the potential app crash. Execute the following steps:
- Use content from the provided catalogs to get the latest app state and the most recent 20 events kept for your Cloud Foundry application. Consider using the commands "GetCfAppState" and "GetCfAppEvents";
- Model a custom command to fetch the last 100 lines from the application’s log file;
- Trigger the automation flow in SAP Automation Pilot created in the previous step.

### Result
By following the steps outlined above, you have implemented a comprehensive, end-to-end solution for automated incident response in your cloud application on SAP BTP. This solution not only detects and alerts you about issues but also automatically triggers recommended actions for troubleshooting and incident management. By structuring and automating the incident response process without the need for human intervention, you ensure faster problem resolution, more efficient project delivery, and higher client satisfaction.
