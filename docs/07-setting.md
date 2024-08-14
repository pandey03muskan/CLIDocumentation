---
sidebar_position: 06
title: "Settings"
description: ""
---

# Manage Your organization
  
  - ### Add user to the organization
    Use command :
    ```
    initz invite user --email=<email> --role=<role>
    ```
    :::tip
    In order to edit the role of the user you can use tha above command.
    :::

  - ### Remove user from the organization
    Use command :
    ```
    initz remove user --scope=<scope> --userid=<userid>
    ```
    :::tip
    In this case, the scope argument value should be "org".
    :::


:::important 
- Only admins of the organization have access to add users to the organization.
- You can add the user to the organization with the role of Admin, Workspace-admin, or Developer.
:::