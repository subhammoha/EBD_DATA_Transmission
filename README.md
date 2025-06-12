# 📦 EBD Project Data Transmission – Postman Guide

This repository enables API-based project data transmission for the **Equitable Building Decarbonization (EBD) Direct Install Program**, using JSON and CSV templates through Postman.

## 📁 Contents

- JSON & CSV templates for Single Family and Multifamily projects
- A Postman Collection for sending Create and Update API calls
- Instructions for authentication, setup, and usage

## Directory Structure

```text
project-data-transmission-templates/
├── SingleFamily/
│   ├── Initial Enrollment/
│   │   ├── data.json
│   │   └── csv/
│   ├── Installation/
│   │   ├── data.json
│   │   └── csv/
│   ├── Post-installation/
│   │   ├── data.json
│   │   └── csv/
│   └── Final Enrollment/
│       ├── data.json
│       └── csv/
└── MultiFamily/
    ├── Initial Enrollment/
    │   ├── data.json
    │   └── csv/
    ├── Installation/
    │   ├── data.json
    │   └── csv/
    ├── Post-installation/
    │   ├── data.json
    │   └── csv/
    └── Final Enrollment/
        ├── data.json
        └── csv/
```

Each stage directory contains a sample `data.json` payload and a `csv` folder. Replace the placeholder README within each `csv` directory with your own templates when you are ready to perform bulk uploads.

## 🛠 Setup Instructions

### 1. Install Postman
Download from [https://www.postman.com/downloads](https://www.postman.com/downloads)

### 2. Import Postman Collection
- Open Postman → Click **Import**
- Upload: `EBD Copy.postman_collection.json`

### 3. Import Environment
- Import the file: `EBD Portal.postman_environment.json`
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

## 📌 Best Practices

- ✅ Use the official templates provided in this repository
- ✅ Do not rename CSV headers or change column order
- ✅ Validate JSON using [https://jsonlint.com](https://jsonlint.com)
- ✅ Use `MM/DD/YYYY` for date fields unless specified otherwise

## 📬 Contact

For any questions or support:  
[ecams.salesforcesupport@energy.ca.gov](mailto:ecams.salesforcesupport@energy.ca.gov)
See [INSTRUCTIONS.md](INSTRUCTIONS.md) for API usage details.

