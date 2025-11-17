## Scenario

Business users want to extend existing enterprise semantic models.
Business user want to use PowerQuery and other capability to augment models.
Enterprise data do not want to give control of models to business users.


### Outline Solution

Assumptions: Direct Lake on OneLake is a viable option.

In user Fabric workspace (on capacity) create a new lakehouse to host shortcuts to source data.
Use the UI or notebook to create shortcuts to relevant data. [Example Notebook - schema enabled lakehouses](/notebooks/CreateShortcuts_blaster.ipynb)
Use a notebook to copy the relevant semantic model to the user workspace, rebind, refresh it.
Ensure business user has appropriate workspace permissions (contributor). User takes ownership of semantic model.

### Set up a lakehouse with shortcuts in another workspace via notebook; with semantic model

Create shortcuts in another workspace from a schema enabled lakehouse [notebook](/notebooks/CreateShortcuts_blaster.ipynb)
Copy a semantic model to another workspace, rebind it and refresh [notebook](/notebooks/01%20Direct%20Lake%20-%20Semantic%20Model%20and%20Report%20Deployment.ipynb)
