Project Title

Azure ARM Template Virtual Machine Deployment

Overview

This project demonstrates Infrastructure as Code (IaC) using Azure Resource Manager (ARM) templates to deploy a fully functional Linux Virtual Machine with networking components.

Resources Deployed
Virtual Machine (Ubuntu 22.04 LTS)
Virtual Network (VNet)
Subnet
Public IP Address
Network Interface (NIC)
Network Security Group (NSG with SSH access)
Deployment Steps
1. Login to Azure
az login
2. Create Resource Group
az group create --name arm-demo-rg --location eastus
3. Deploy Template
az deployment group create \
  --resource-group arm-demo-rg \
  --template-file template.json \
  --parameters parameters.json
Outputs
Public IP Address: (from deployment output)
Resource Group: arm-demo-rg
Verification

SSH into VM:

ssh azureuser@<public-ip>