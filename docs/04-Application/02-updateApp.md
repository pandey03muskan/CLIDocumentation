---
sidebar_position: 02
title: "Update App"
description: ""
---

# Update App

- ## Update app using arguments
  
  Use command (*edit app using appname*):
  ```
  init edit app --appname=<appname> --setEnv=<true/false> --setAppSetting=<true/false>
  ```
  
  Use command (*edit app using appid*):
  ```
  init edit app --appid=<appid> --setEnv=<true/false> --setAppSetting=<true/false> 
  ```

- ## Update app using file

  Use command (*edit app using appname*):
  ```
  initz edit app --appname=<appname> -f <filepath>
  ```

  Use command (*edit app using appid*):
  ```
  initz edit app --appid=<appid> -f <filepath>
  ```

  Example template :

  ```json title="editApp.json"
  {
  "port": 8080,
  "http_path": "",
  "env_variables": {
    "prod": [
    {
      "key": "PORT",
      "type": "env",
      "value": "8080"
    }
    ],
    "stg": [
    {
      "key": "PORT",
      "type": "env",
      "value": "8080"
    }
    ],
    "test": [
    {
      "key": "PORT",
      "type": "env",
      "value": "8080"
    }
    ]
  },
  "instance_details": {
    "instance_type": "Default",
    "max": 1,
    "min": 1,
    "vertical_auto_scale": false,
    "ram": "2Gi",
    "vcpu": "1000m"
  },
  "workspace_id": "669ddebbbc8c54a247229e78"
  }
  ```

  Example template :

  ```json title="editApp.yaml"
  port: 8080
  http_path: ""
  env_variables:
      prod:
          - key: PORT
            type: env
            value: "8080"
      stg:
          - key: PORT
            type: secret
            value: "8080"
      test:
          - key: PORT
            type: env
            value: "8080"
  instance_details:
      instance_type: Default
      max: 1
      min: 1
      vertical_auto_scale: false
      ram: 2Gi
      vcpu: 1000m
  workspace_id: 669ddebbbc8c54a247229e78
  ```

  You can either use the configuration provided in the file above to create the workspace or generate your own example configuration to do so.

  - To generate json configuration :
  ```
  initz edit app --appname=<appname> -e json
  ```
  
  - To generate yaml configuration :
  ```
  initz edit app --appid=<appid> -e yaml
  ```