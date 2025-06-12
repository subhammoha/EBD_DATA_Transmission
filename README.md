# EBD Project Data Transmission Templates

This repository organizes example payloads for transmitting project data to Salesforce via the API.  Each workflow stage for Single Family and Multi Family projects contains a JSON template and a placeholder directory for CSV uploads.

The directory structure is:

```
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

Each stage folder contains:

- `data.json` – an example JSON request body for that workflow step.
- `csv/` – a README file inside each `csv` folder that you can replace with your own CSV templates.

Replace the contents of the `csv` directories with your own files when you are ready to perform bulk uploads.

See [INSTRUCTIONS.md](INSTRUCTIONS.md) for API usage details.

