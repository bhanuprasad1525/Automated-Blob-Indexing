# Automated-Blob-Indexing

Automated Blob Indexing using Azure Event Grid & Azure Functions

This project implements a serverless Blob Indexing pipeline using Azure Event Grid, Azure Functions (Python), and Azure Cosmos DB.
Whenever a new file is uploaded to Azure Blob Storage, an Event Grid notification triggers a Function, which extracts metadata and stores an index entry in Cosmos DB.

Overview

Detects blob uploads in real time
Extracts metadata (blob name, size, content type, URL, timestamp)
Stores the metadata as a document in Azure Cosmos DB
Acts as a lightweight Blob Indexer for search, auditing, or tracking
- Trigger Source
Azure Event Grid → "Blob Created" event
- Target Storage
Cosmos DB (Core SQL API)
Testing:

  1️. Upload any file to Blob Storage
      Example:
           documents/sample.txt

  2️. Event Grid triggers the Function

  3️. Verify document in Cosmos DB

Technologies Used

- Azure Functions (Python)
- Azure Event Grid
- Azure Blob Storage
- Azure Cosmos DB
- Python SDK: azure-cosmos, azure-functions

Status

- Function Trigger working
- Event Grid integrated
- Cosmos DB write success
- Project deployment-ready
























