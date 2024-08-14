---
sidebar_position: 04
title: "Additional Commands"
description: ""
---


- ### How to get list of apps within a workspace
  To obtain a list of 'Apps', including each app's ID, name, current environment, last deployment timestamp, live app URL, and current app status.\
  Use command :
  ```
  initz get app 
  ```

   To obtain information about a specific app.\
   Use command :
   ```
   initz get app <appname>
   ```
  
- ### Activities of App
   To get the activities performed for the particular app, including timestamps, details of each activity, and the users who carried out those activities.\
   Use command :
   ```
   initz get activity --appid=<appid>
   ```

- ### Check App metric
    To check CPU, Network & Memory Usage, use command :
    ```
      initz check metrics --appname <appname> --runtype <runtype>
    ```
- ### Logs of App 
    To get the logs of the app for each environment (test/staging/production), Use command:

    - Get logs using appid
    ```
    initz logs app --appid=<appid> --env=<env>
    ```

    - Get logs using appname
    ```
    initz logs app --appname=<appname> --env=<env>
    ```

   :::info 
   - --env id is short for 'environment.' The possible values for environment can be 'test,' 'stg,' or 'prod'.
   :::
- ### Logs for a supply chain step
    Get logs for a supply chain step using run id.
    Use command :
    ```
    initz logs supplychainstep --runid=<runid> --stage=<stage>
    ```

- ### Refresh supply chain data
     To refresh the supply chain data of an app, use command :
     ```
     initz refreshapp <appname>
     ```

- ### Check App name 
     To check app name is already used or not, use command :
     ```
     initz check appname <appname>
     ```