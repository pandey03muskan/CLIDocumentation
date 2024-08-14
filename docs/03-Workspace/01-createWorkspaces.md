---
sidebar_position: 01
title: "Create Workspace"
description: ""
---

# Workspace

 ## Create Workspace
     
     

   - ### Create workspace using arguments
     ```
     initz create workspace --name=<name> --desc=<desc> --prod-cluster=<prod-cluster> --non-prod-cluster=<non-prod-cluster> --registry=<registry>
     ```
    
     :::info
     - 'desc' stands for: Description (workspace description).
     - 'prod-cluster' stands for: Production cluster.
     - 'non-prod-cluster' stands for: Non-production cluster (used for test or stage environments).
     :::

   - ### Create workspace using file
     
     ```
     initz create workspace -f <file-path>
     ```
     
     *Example template :*

     ```json title="workspace.json"
     {
     "workspace_name": "example",
     "description": "just for example purpose",
     "prod_run_cluster": "initializ-prod-eks-cluster",
     "non_prod_run_cluster": "initializ-np-eks-cluster",
     "docker_registry": "DockerConfig",
     "supply_chain_template_id": "initializ-secure-cicd"
     }
     ```
    
     *Example template :*

     ```json title="workspace.yaml"
     workspace_name: example
     description: just for example purpose
     prod_run_cluster: initializ-prod-eks-cluster
     non_prod_run_cluster: initializ-np-eks-cluster
     docker_registry: DockerConfig
     supply_chain_template_id: initializ-secure-cicd
     ```

     You can either use the configuration provided in the file above to create the workspace or generate your own example configuration to do so.

     - To generate json configuration :
     ```
     initz create workspace --name="example" --desc="just for example purpose" --prod-cluster="example_prod_cluster" --non-prod-cluster="example_non_prod_cluster" --registry="example_registry" -e json
     ```
     
     - To generate yaml configuration :
     ```
     initz create workspace --name="example" --desc="just for example purpose" --prod-cluster="example_prod_cluster" --non-prod-cluster="example_non_prod_cluster" --registry="example_registry" -e yaml
     ```
      


     To create a workspace in an organization other than the current one, you need to include an additional flag `orgid=< organizationID >` or you can set that particular organization.\
     Use command :

     To add orgid=< organizationID > :
     ```
     initz create workspace --name=<name> --desc=<desc> --prod-cluster=<prod-cluster> --non-prod-cluster=<non-prod-cluster> --registry=<registry> --orgid=<organization ID>
     ```

     To set the organization :

     ```
     initz set org --orgid=<organization ID>
     ```
     **How can you use your own prod-cluster and non-prod-cluster**

     You can use your own cluster instead of the default cluster provided by Initializ.ai. For more information, refer [(Bring your own clusters)](http://localhost:3000/docs/Environment/clusters).

     **How can you use your own registry**

     To use your own registry refer [(Bring your own registry)](http://localhost:3000/docs/Environment/registry)


    :::note
     - The workspace name is mandatory, while all other arguments are optional. By default, 'prod-cluster,' 'non-prod-cluster,' and 'registry' are assigned, provided by Initializ.ai.
     - For more information, you can use command :
        ```
        initz create workspace -h
        ```
    :::