---
sidebar_position: 03
title: "Additional Commands"
description: ""
---

- ### How to get workspaces of organization
  To get a list of workspaces, including each workspace's ID, name, and app count, in a particular organization, Use command :
  ```
  initz get workspaces
  ```

- ### Describe workspace
  shows details about a workspace.
  Use command :
  ```
  initz describe workspace --workspaceid <workspaceid>
  ```

- ### How to set a particular workspace
   When you create your account, one workspace is created by default, and this default workspace is initially set. If you want to work in a different workspace, you can set that workspace using command :
   ```
   initz set workspace --workspaceid=<workspaceID>
   ```
- ### Activities of workspace
   To get the activities performed within the workspace, including timestamps, details of each activity, and the users who carried out those activities,\
   Use command :
   ```
   initz get activity
   ```

   You can also view the activities for a specific workspace. \
   Use command :
   ```
   initz get activity --workspaceid=<workspaceID>
   ```

- ### Check workspace name
     To check workspace name is already used or not, use command :
     ```
     initz check workspace <workspace-name>
     ```

   