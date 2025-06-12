# EBD Project API - Quick Reference

This guide summarizes how to use the provided JSON and CSV templates with the Salesforce API.

## 1. Authenticate
1. Open Postman and select the **EBD** environment.
2. In the collection's **Authorization** tab choose **Get New Access Token** and log in with your Salesforce credentials.
3. Click **Use Token**.

## 2. Create a New Project
- **Endpoint:** `POST {{domain_url}}/services/apexrest/EBD/EBDAPIStage1Creation/`
- Body: choose **raw** and set type to **JSON**. Paste the contents of a template like `SingleFamily/Initial Enrollment/data.json`.

To create multiple projects, set the `Content-Type` header to `text/csv` and upload a CSV file from one of the `csv` folders.

## 3. Update an Existing Project
- **Endpoint:** `PATCH https://ecams-energy--cecuat.sandbox.my.salesforce.com/services/apexrest/EBD/EBDAPIUpdateProjects/`
- Body: raw JSON with the fields to update, including the record `Id`.

## 4. Notes
- Authorization headers are automatically populated after authentication.
- If your token expires, repeat the authentication step.
- Replace field names if they differ in your Salesforce org.

For additional help, contact the EBD Salesforce Support Team.
ecams.salesforcesupport@energy.ca.gov 

