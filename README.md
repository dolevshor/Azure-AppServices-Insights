# Azure App Services Insights

The 'Azure App Services Insights' workbook offers a comprehensive view of your Azure App Services resources.

It enables you to delve into and compare key metrics effortlessly, gaining insights into usage trends, optimizing performance, and guiding strategic decisions effectively.

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/014a0b66-4219-4d07-bb1a-9877917d9843)

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/73892ad3-5f9b-4ca6-acbc-8ec68fe3cf2b)

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/51d38b42-85f4-4055-a9d0-2e7faab51176)

## Introduction

Azure App Service offers flexible scaling options (both Scale Up and Scale Out), supports multiple operating systems (Windows and Linux), and enables hosting multiple apps on the same App Service Plan.

Managing multiple App Service Plans, App Services, and Staging Slots requires effective management, performance comparison, and operational oversight — this functionalities facilitated by this workbook. 


## Structure and Views

### Structure

This workbook contains 2 main parts:
- **Overview** - Holistic view of Azure App Services resources.
- **Monitor** - Holistic view of Azure App Services Metrics

> App Services resources = App Service Plans, App Services, Staging slots.

### Views

Types of views this workbook provides:

- **Overview**
  - App Service Plan
    - Name
    - Resource Group
    - Location
    - Kind
    - Size
    - Tier
    - Status
    - Number of Sites
    - Current Instances
    - Maximum scale (instance)
  - App Services + Slots
    - Name
    - Resource Group
    - Location
    - Kind
    - Type
    - SKU
    - App Service Plan
    - State

> The information displayed uses [KQL](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/) queries to query the [Azure Resource Graph](https://learn.microsoft.com/en-us/azure/governance/resource-graph/overview).

- **Monitor**
  - App Service Plan
    - CPU Percentage (Avg)
    - Memory Percentage (Avg)
  - App Service
    - CPU Time (Sum)
    - Memory Working Set (Avg)
  - Slots
    - CPU Time (Sum)
    - Memory Working Set (Avg) 

#### Filters

This workbook support to filter by:

- Resource Groups
- App Service Plans
- Apps (App Services + Staging slots)
- Time range

## How to use it?

Importing this Workbook to your Azure environment is quite simple.

Follow this steps to use the Workbook:

- Login to [Azure Portal](https://portal.azure.com/) <img src="https://user-images.githubusercontent.com/69309933/172941966-9e030031-6ccb-4ebf-bd2b-04bb623e5ff7.png" width="20" height="20">
- Go to _'Azure Workbooks'_

<img src="https://user-images.githubusercontent.com/69309933/172806635-14051976-328e-4623-96ab-0dd6a7bc7817.png" width="350">

- Click on _'+ Create'_

<img src="https://user-images.githubusercontent.com/69309933/172807465-cced3466-0669-423b-87b3-8fa70fdbf1d1.png" width="350">

- Click on _'+ New'_

<img src="https://user-images.githubusercontent.com/69309933/172807547-52d790ce-7852-4b4b-a81f-81e8b7fac26e.png" width="350"> 

- Open the Advanced Editor using the _'</>'_ button on the toolbar

<img src="https://user-images.githubusercontent.com/69309933/172807673-dfc63741-0c40-47c0-ab58-d39309b06e69.png" width="700"> 

- Select the _'Gallery Template'_ (step 1)
- Replace the JSON code with this JSON code [Azure AppService Insights JSON](https://raw.githubusercontent.com/dolevshor/Azure-AppService-Insights/main/Workbook/Azure%20App%20Service%20Insights.workbook) (step 2)
  - We use the _Gallery Templaty type_ (step 1), so we need to use the _'Azure App Service Insights.workbook'_ and not the _'Azure App Service Insights.json'_.
- Click _'Apply'_ (step 3)

<img src="https://user-images.githubusercontent.com/69309933/172807762-17aec6f9-4a81-4d5b-9017-673a0ab6b26e.png" width="700"> 

- Click in the ‘Save’ button on the toolbar

![image](https://github.com/dolevshor/Azure-AppServices-Insights/assets/69309933/88692b70-7d96-42e7-8852-590af825cfb5)

- Select a name and where to save the Workbook:
  - Title: _'Azure App Service Insights'_
  - Subscription: <_Subscription Name_>
  - Resource group: <_Resource Group Name_>
  - Location: <_Region_>
- Click _'Save'_
  
The Workbook is ready to use!
- Click on _'Workbooks'_
- Click on _'Azure App Service Insights'_ Workbook.

Start using the Workbook and analyze your Azure App Service resources.<br/>

> (Optional) You can filter by specific subscription/s or resource/s.
