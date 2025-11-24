## Scenario

Business users want to extend existing enterprise semantic models.   
Business user want to use PowerQuery and other capability to augment models.  
Enterprise data do not want to give control of source models directly to business users.  


### Outline Solution

![Architecture](/images/WebModelShortcutsArch.png)

Assumptions:  
   - Direct Lake on OneLake is a viable option.  
   - Semantic models in the shared capacity or service, can be migrated to Fabric capacity and direct lake mode by converting PowerQuery imports into [DataFlow Gen 2](https://learn.microsoft.com/en-gb/power-bi/transform-model/export-query-results)

1. In user Fabric workspace (on capacity) create a new lakehouse to host shortcuts to source data.  
2. Use the UI or notebook to create shortcuts to relevant data. [Example Notebook - schema enabled lakehouses](/notebooks/CreateShortcuts_blaster.ipynb)  
3. Use a notebook to copy the relevant semantic model to the user workspace, rebind, refresh it.  
4. Ensure business user has appropriate workspace permissions (contributor). User takes ownership of semantic model.  

### Set up a lakehouse with shortcuts in another workspace via notebook; with semantic model

NOTE: Notebooks can run either PySpark or Python kernels. 

- Create shortcuts in another workspace from a schema enabled lakehouse [notebook](/notebooks/01%20CreateShortcuts%20blaster.ipynb)
- Copy a semantic model to another workspace, rebind it and refresh [notebook](/notebooks/02%20Direct%20Lake%20-%20Semantic%20Model%20Deployment.ipynb)
- After enabling permissions:
    - Destinations users will be able to modify their version of the semantic model, using their read-only shortcut data in their local lakehouse
    - Destinations users will be able to modify their version of the semantic model and use PowerQuery and OneLake catalog to augment the semantic model

### Enabling relevant permissions
- Users in destination workspace should be minimum contributors. This will allow them to see the metadata for the lakehouse and the semantic model, but not be able to read any data.
- Share permissions from Source Lakehouse    
    ![Share permissions](/images/Share_lakehouse.png)
- Change the destination semantic model settings     
    ![settings](/images/Semanticmodel_settings.png)
- Take over the semantic model (build permissions)    
    ![takeover](/images/Semanticmodel_takeover.png)
- Taken over the semantic model    
    ![takenover](/images/Semanticmodel_newtakeover.png)
- Enable PQ in web editing mode    
    ![pq1l](/images/Semanticmodel_editing.png)
