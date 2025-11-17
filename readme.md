# Various helpful resources for Microsoft Fabric

## *Contents*

- [Useful Blogs](#useful-blogs)
- [Useful training and repos](#useful-training-and-repos)
- [Fabric Databricks Mirroring](#fabric-databricks-mirroring)
- [Copilot Prompt for searching the Fabric Roadmap](#copilot-prompt-for-searching-the-fabric-roadmap)
- [Copy Data from one Lakehouse to anther to support data management for deployment between SDLC stages](#copy-data-from-one-lakehouse-to-anther-to-support-data-management-for-deployment-between-sdlc-stages)
- [Collect information for Fabric Capacities, Workspaces and Items and record in SCD2](#collect-information-for-fabric-capacities-workspaces-and-items-and-record-in-scd2))
- [Understanding Microsoft Fabric Capacity state and history from the Azure Resource Graph](#understanding-microsoft-fabric-capacity-state-and-history-from-the-azure-resource-graph)

<br><br>
***
***
<br><br>

## Useful Blogs

- [Blogs page](/blogs.md)
- [Official Fabric Toolbox from Microsoft](https://github.com/microsoft/fabric-toolbox/tree/main)


## Useful training and repos

 - [Useful training and repos](/repos.md)

## Self authored or contributed

### Fabric Databricks Mirroring

Automation and helper notebooks for mirroring from UC using tags and schemas [repo](https://github.com/bricrsa/fabric-databricks-mirror-helper)

### Set up a lakehouse with shortcuts in another workspace via notebook; with semantic model

Create shortcuts in another workspace from a schema enabled lakehouse [notebook](/notebooks/CreateShortcuts_blaster.ipynb)
Copy a semantic model to another workspace, rebind it and refresh [notebook](/notebooks/01%20Direct%20Lake%20-%20Semantic%20Model%20and%20Report%20Deployment.ipynb)

### Copilot Prompt for searching the Fabric Roadmap

Designed to work in Copilot in Bing on Edge browser. [Details of prompt](FabricRoadmapPrompt.md)


### Copy Data from one Lakehouse to anther to support data management for deployment between SDLC stages

Notebook: [Copy Data between Lakehouses](./notebooks/CopyDataForSDLC.ipynb)

### Collect information for Fabric Capacities, Workspaces and Items and record in SCD2

- Notebook: [List and Record Fabric Item Metadata using Semantic Link](./notebooks/ListCapacityWorkspaceItems.ipynb)
- Notebook: [List and Record Fabric Item Metadata using Semantic Link Labs - Admin APIs](./notebooks/ListCapacityWorkspaceItems.ipynb)
    - Allows all items to be recorded, even ones the running don't have access to
- Notebook: [Analyse Fabric Item Data - SQL](./notebooks/CapacityWorkspaceItemsAnalysis.ipynb)


### Understanding Microsoft Fabric Capacity state and history from the Azure Resource Graph

Write queries in [Azure Resource Graph Explorer](https://portal.azure.com/#view/HubsExtension/ArgQueryBlade) in the Azure Portal. Show capacity information in the Azure portal via an Azure Dashboard.

Or however you want to connect to the Azure Resource Graph.

- [Current Capacity State](./kql/CapacityState.kql)
- [Current Capacity History](./kql/CapacityResourceChanges.kql)
- Example of the Capacity State chart
    ![CapacityDashboard](/images/FabCapGraph.png)