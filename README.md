## CMS Demo using Azure Synapse, Azure Data Factory and Power BI

#### Audience
If you belong to one of the below categories, you have landed at the right place!
1. If you are new to Azure Synapse and/or Azure Data Factory or just getting started.
2. If you are looking to set up a Data Warehousing demo environment using Azure Synapse, Azure Data Factory and PowerBI in just 4 steps.
3. If you are interested in reporting on Centers for Medicare and Medicaid Services (CMS) data with Azure Synpase and PowerBI.

#### Purpose
The purpose of this project is to 1) automate the deployment of Azure Resources (Azure Resource Group, Azure Data Lake Storage, Azure Synapse and Azure Data Factory) 2) automate downloading CMS data from https://cms.gov and load into Azure Synapse Tables. This CMS data can then be used for reporting using Power BI.

### Pre-requisites:
Azure Account with permissions to create Azure Resources (Storage, Azure Data Factory, Synapse)

### 4 Easy Steps for Deployment:
1. Login to Azure Portal and open Cloud Shell with Powershell prompt from the top navigation bar (see below image)

    ![Command Shell](https://github.com/kunal333/E2ESynapseDemo/blob/master/images/CommandShell.png)
2. Clone this Git Repository and switch to new directory (using commands below)
    `git clone https://github.com/kunal333/E2ESynapseDemo.git`

    `cd E2ESynapseDemo`

    ![Clone Git Repository](https://github.com/kunal333/E2ESynapseDemo/blob/master/images/CloneGitRepo.png)
3. Start script and provide Resource Group Name and User credentials (Example below)
    `PS /home/kunal/E2ESynapseDemo> ./deploySynapseStorageADF.ps1`

    `Do you want to use existing resource(s) for this CMS Demo or create everything new from scratch?  Enter 1 for New or 2 for Existing: 1`

    `Enter New Resource Group Name: SynapseDemo1`

    `Enter SQL Server Administrator Name: synapsedemo1server`

    `Enter SQL Server Password: Passw0rd!`

    ![Enter Details](https://github.com/kunal333/E2ESynapseDemo/blob/master/images/EnterDetails.png)
4. Next step is to get the Power BI tempate and connect to the Synapse instance. A tutorial of deploying the parameterized Power BI Template file is here: https://youtu.be/_mslQZM7NrU

### Useful Diagrams:
**Reference Architecture**
![Reference Architecture](https://github.com/kunal333/E2ESynapseDemo/blob/master/images/ReferenceArchitecture.png)

**PowerBI Dashboard**
![Image of Dashboard](https://github.com/kunal333/E2ESynapseDemo/blob/master/images/Dashboard%20Image.png)

**Data Flow Architecture**
![Source to Target](https://github.com/kunal333/E2ESynapseDemo/blob/master/images/Source%20to%20Target.png)

**Dimensional Data Model**
![Denormalized and Derived](https://github.com/kunal333/E2ESynapseDemo/blob/master/images/DimsDerived.png)

## Script Explained
If you're intereted to learn step by step process how the deployment script performs, it is explained <a href="https://github.com/kunal333/E2ESynapseDemo/blob/master/ScriptExplained.md" title="ScriptExplained">here</a>

### Contributing
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com)
with any additional questions or comments.

### License
Copyright (c) Microsoft Corporation. All rights reserved. Licensed under the MIT License. This project has adopted the Microsoft Open Source Code of Conduct. For more information see the Code of Conduct FAQ or contact opencode@microsoft.com with any additional questions or comments.
