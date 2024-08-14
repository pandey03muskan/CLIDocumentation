---
sidebar_position: 02
title: "Workspace Settings"
description: ""
---

   - ### Add user to the Workspace
      In order to add a user to a particular workspace, Use command :
      ```
      initz add user --role=<role> --userid=<userid>
      ```
     :::important
      You can only add a user to the workspace if the user exists in the organization.
     :::

   -  ### Remove user from the workspace
      In order to remove a user from a particular workspace, Use command :
    
      ```
      initz remove user --scope=<scope> --userid=<userid>
      ```
      :::tip
      In this case, the scope argument value should be "workspace".
      :::

   - ### Remove workspace from the organization
      To remove the workspace from the organization, Use command :
      
      ```
      initz delete workspace --workspaceid=<workspaceid>
      ```



    :::tip
    In case you face any issue :
   - Check your current workspace.
   - If you are in the target workspace, you can use the command to add the user directly. Otherwise, you need to set the workspace first ([How to set workspace](http://localhost:3000/docs/Workspace/Additional#how-to-set-a-particular-workspace)). 
     :::

    :::note
    - Only admins and workspace-admins will have the ability to delete the workspace.. 
    :::