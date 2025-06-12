# 📦 EBD Project Data Transmission

This repository enables API-based project data transmission for the **Equitable Building Decarbonization (EBD) Direct Install Program**, using JSON and CSV templates through Postman.

## 📁 Contents

- JSON & CSV templates for Single Family and Multifamily projects
- Postman collection and environment JSON files for authentication and requests
- Instructions for authentication, setup, and usage

## Directory Structure

```text
postman/
├── collections/
├── environments/
project-data-transmission-templates/
├── SingleFamily/
│   ├── Initial Enrollment/
│   │   ├── json
│   │   └── csv
│   ├── Final Enrollment/
│   │   ├── json
│   │   └── csv
│   ├── Installation/
│   │   ├── json
│   │   └── csv
│   └── Post-installation/
│       ├── json
│       └── csv
└── MultiFamily/
    ├── Initial Enrollment/
    │   ├── json
    │   └── csv
    ├── Final Enrollment/
    │   ├── json
    │   └── csv
    ├── Installation/
    │   ├── json
    │   └── csv
    └── Post-installation/
        ├── json
        └── csv
```

Each stage directory contains a sample `.json` payload and a `csv` Template. 


## 🛠 Setup Instructions

### 1. Install Postman Or Use Postman Web
Download from [https://www.postman.com/downloads](https://www.postman.com/downloads)

Web-[https://www.postman.com](https://www.postman.com)

### 2. Import Postman Collection
- Download the collection from [`postman/collections`](postman/collections/)
- Open Postman → Click **Import**
- Upload `EBD.postman_collection.json`


### 3. Import Environment
- Download the environment file from [`postman/environments`](postman/environments/)
- Set **EBD Portal** as the active environment

## 🔐 Authentication

1. Open the Postman collection → **Authorization** tab
2. Click **Get New Access Token**
3. Login with your Salesforce Experience Cloud credentials
4. Click **Use Token**

The token is stored and used automatically for all requests.

## 📤 Creating Records (Single or Multiple)

You can create **one or many** records using **either JSON or CSV**.

### ➤ JSON
- Use request: `Create A Single Project`
- Header: `Content-Type: application/json`
- Body → `raw → JSON` → paste your JSON
- Click **Send**

### ➤ CSV
- Use request: `Create Multiple Projects Through CSV`
- Header: `Content-Type: text/csv`
- Body → `binary` → upload `template.csv`
- Click **Send**

📨 A confirmation email will be sent with processing results.

## ♻️ Updating Records (Single or Multiple)

Updates can also be submitted via **JSON or CSV**.

### ➤ JSON
- Use request: `Update Project Data`
- Header: `Content-Type: application/json`
- Body → `raw → JSON` → paste your update JSON
- Click **Send**

### ➤ CSV
- Use the same request: `Update Project Data`
- Header: `Content-Type: text/csv`
- Body → `binary` → upload `update_template.csv`
- Click **Send**

📨 A confirmation email will be sent with processing results.


## 📌 Best Practices

- ✅ Use the official templates provided in this repository
- ✅ Do not rename CSV headers or change column order
- ✅ Validate JSON using [https://jsonlint.com](https://jsonlint.com)
- ✅ Use `MM/DD/YYYY` for date fields unless specified otherwise

## 📬 Contact


For any questions or support:  

[ecams.salesforcesupport@energy.ca.gov](mailto:ecams.salesforcesupport@energy.ca.gov)
