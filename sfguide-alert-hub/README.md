# Alert Hub

<a href="https://emerging-solutions-toolbox.streamlit.app/">
    <img src="https://github.com/user-attachments/assets/aa206d11-1d86-4f32-8a6d-49fe9715b098" alt="image" width="150" align="right";">
</a>

The Alert Hub is a rule-based meta-data driven framework for alerts and notifications.  It enhances Snowflake's native alerting capabilities by adding a rich GUI and support for Jinja templating.  The framework can be tailored through custom condition/action queries or applying query templates that monitor the account objects or any type of events within the account and send out multi-channel notifications.

## Support Notice

All sample code is provided for reference purposes only. Please note that this code is
provided `as is` and without warranty. Snowflake will not offer any support for the use
of the sample code. The purpose of the code is to provide customers with easy access to
innovative ideas that have been built to accelerate customers' adoption of key
Snowflake features. We certainly look for customers' feedback on these solutions and
will be updating features, fixing bugs, and releasing new solutions on a regular basis.

Copyright (c) 2025 Snowflake Inc. All Rights Reserved.

## Deployment

- Using Snowsight, open a worksheet, set your role to ACCOUNTADMIN, copy/paste alert_hub_setup.sql and Run All
- Navigate to Projects on the left-hand side and select Streamlit
- Select ALERT_HUB
- Follow in-app instructions

> [!IMPORTANT]
> If using an email alert, the notification recipient must [verify their email address](https://docs.snowflake.com/en/user-guide/notifications/email-notifications#verify-the-email-addresses-of-the-email-notification-recipients).

## Usage

The app operates using JINJA templates, allowing for reuse of condition and action patterns across many alerts.  To construct an alert:

- Open the Conditions page, set up or select a Condition template, and define a Condition using parameters
- If you want an alert to send an email or write an event to a notification queue, set up the integration in the Notification Integration page
- Open the Actions page, set up or select an Action template, and define an action using Parameters
- Open the Alerts page to create an alert using configurated Conditions/Actions/Notification Integrations
- You can also manage existing alerts on the Alerts page

## Demo

There are two demos available, both should result in a sample alert being set up - please remember to disable the sample alert when finished demoing
- **demo.sql** provides a SQL-based walkthrough -  replace **<<YOUR_EMAIL_HERE>>** with your email
- **demo.md** provides a manual walkthrough - replace **<<YOUR_EMAIL_HERE>>** with your email

## Reset

To reset the solution, simply re-run the alert_hub_setup.sql - **Note** This will overwrite all of the configurations and set it back to default

## Tagging

Please see `TAGGING.md` for details on object comments.