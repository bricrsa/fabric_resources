# Various helpful resources for Microsoft Fabric

## Useful Blogs

- [Blogs page](/blogs.md)
- [Officual Fabric Toolbox from Microsoft](https://github.com/microsoft/fabric-toolbox/tree/main)


## Useful training and repos

 - [Useful training and repos](/repos.md)

## Self authored or contributed

### Fabric Databricks Mirroring

Automation and helper notebooks for mirroring from UC using tags and schemas [repo](https://github.com/bricrsa/fabric-databricks-mirror-helper)

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

Write queries in [Azure Resource Graph Explorer](https://portal.azure.com/#view/HubsExtension/ArgQueryBlade) in the Azure Portal

Or however you want to connect to the Azure Resource Graph.

- [Current Capacity State](./kql/CapacityState.kql)
- [Current Capacity History](./kql/CapacityResourceChanges.kql)
- Example of the Capacity State chart
    ![CapacitiDashboard](/images/FabCapGraph.png)