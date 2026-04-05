# Azure Storage Deployment with Secure Access, Cost Awareness, and Business Use Case

## Overview
This project demonstrates how to deploy and secure Azure Storage for a small business use case involving customer file storage.

The focus of this lab is not just resource creation, but applying security best practices, managing access, and making cost-conscious decisions while maintaining usability.

## Business Context
This solution simulates a small business needing secure file storage for customer data.

Internal users require controlled access to files, while external users may need temporary access without exposing permanent credentials.

## Resources Created
- Resource Group
- Azure Storage Account
- Blob Container
- Sample file upload

## Configuration Performed

### Storage Deployment
Created a Standard-tier storage account using Locally Redundant Storage (LRS) to balance cost and availability.

### Blob Storage
Configured a private container and uploaded sample customer data.

### Access Control (RBAC)
Implemented role-based access control to manage internal user permissions securely.

### Temporary Access (SAS)
Generated a Shared Access Signature (SAS) token to allow time-limited external access without exposing permanent credentials.

### Access Keys Review
Reviewed access keys and documented why they are less preferred compared to RBAC.

### Encryption
Verified encryption at rest using Microsoft-managed keys to protect stored data.

## Security Decisions
- Used private container access to prevent public exposure
- Implemented RBAC for controlled internal access
- Used SAS tokens for temporary, scoped external access
- Avoided reliance on access keys as a primary access method
- Verified encryption at rest for data protection

## Cost Awareness
Selected Standard performance tier and LRS redundancy to provide a cost-effective solution appropriate for a small business use case.

## Trade-Offs
- RBAC provides better security and control compared to shared keys, but requires role management
- SAS tokens enable temporary access but must be carefully scoped and time-limited
- Standard storage is cost-effective but may not be suitable for high-performance workloads

## Outcome
This project demonstrates the ability to deploy, secure, and explain Azure storage solutions while aligning technical decisions with business needs.

## Screenshots

### Resource Group
![Resource Group](screenshotsss/01-resource-group.png)

### Storage Account
![Storage Account](screenshotsss/02-storage-account.png)

### Blob Container
![Container](screenshotsss/03-container.png)

### RBAC Configuration
![RBAC](screenshotsss/04-rbac.png)

### SAS Token
![SAS](screenshotsss/05-sas.png)

### Access Keys
![Access Keys](screenshotsss/06-access-keys.png)

### Encryption
![Encryption](screenshotsss/07-encryption.png)
