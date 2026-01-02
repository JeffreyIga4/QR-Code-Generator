# Azure QR Code Generator

A simple serverless application that generates QR codes for a given URL using **Azure Functions** and **Node.js**.  
This project is designed as a short hands-on exercise to practice Azure Functions deployment and configuration.

---

## Features

- **Serverless**: Uses Azure Functions for minimal infrastructure management  
- **QR Code Generation**: Dynamically generates QR codes for provided URLs  
- **Node.js Runtime**: Runs on Node.js LTS supported by Azure Functions  
- **HTTP Trigger**: Accessible via a public HTTP endpoint  

---

## Prerequisites

- Node.js **20 LTS**
- Azure Functions Core Tools
- Azure CLI
- An active Azure subscription
- An Azure Storage Account

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/rishabkumar7/azure-qr-code.git
cd azure-qr-code
```

--- 
## Install Dependencies 
npm install

---
## Local configuration
### Create a local.settings.json file and input the following:
```bash
{
  "IsEncrypted": false,
  "Values": {
    "AzureWebJobsStorage": "<STORAGE_CONNECTION_STRING>",
    "FUNCTIONS_WORKER_RUNTIME": "node"
  }
}
```

--- 
## Runninng locally
```bash
func start
```

---
## Usage
### Send a request to the deployed function endpoint
```bash
curl -X POST https://<YOUR_FUNCTION_APP_NAME>.azurewebsites.net/api/GenerateQRCode \
  -H "Content-Type: application/json" \
  -d '{"url":"https://www.example.com"}'
```



