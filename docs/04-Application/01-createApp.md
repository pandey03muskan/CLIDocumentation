---
sidebar_position: 01
title: "Create App"
description: ""
---

# Create App

  - ### Create App using arguments

    Use command :
    ``` 
    initz create app --name=<appname> --user=<user> --repo=<repo> --branch=<branch> --setAppSetting=<true/false> --setEnv=<true/false>
    ```
    :::important
     Here, the 'repo' argument is mandatory, while all other arguments are optional. By default, values such as the port will be configured as 8080, the app instance size to 'Default' with 2Gi RAM and 1000m vCPU, auto-scaling is false, and the minimum and maximum number of instances are both configured as 1. The remaining values are extracted from the provided repo.
    :::

  - ### Create App using file

     Use command :

        ```
        initz create app -f <file path> 
        ```

       Example template

        ```json title="app.json"
        {
        "application_name": "example",
        "git_user": "git_user",
        "git_repo": "git_user/repo_name",
        "git_branch": "main",
        "port": 8080,
        "http_path": "",
        "instance_details": {
        "instance_type": "Default",
        "max": 1,
        "min": 1,
        "vertical_auto_scale": false,
        "ram": "2Gi",
        "vcpu": "1000m"
        },
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
        "workspace_id": "669ddebbbc8c54a247229e78"
        }
        ```

      Example template

        ```json title="app.yaml"
        application_name: example
        git_user: git_user
        git_repo: git_user/repo_name
        git_branch: main
        port: 8080
        http_path: ""
        instance_details:
            instance_type: Default
            max: 1
            min: 1
            vertical_auto_scale: false
            ram: 2Gi
            vcpu: 1000m
        env_variables:
            prod:
                - key: PORT
                type: env
                value: "8080"
            stg:
                - key: PORT
                type: env
                value: "8080"
            test:
                - key: PORT
                type: env
                value: "8080"
        workspace_id: 669ddebbbc8c54a247229e78
         ```

    You can either use the configuration provided in the file above to create the application or generate your own example configuration to do so.

    - To generate json configuration :
      ```
      initz create app --name=< appname > --user=< user > --repo=<  repo > --branch=< branch >  --setAppSetting=< true/false > --setEnv=< true/false > -e json 
      ```

    - To generate yaml configuration
      ```
      initz create app --name=< appname > --user=< user > --repo=< repo > --branch=< branch > --setAppSetting=< true/false > --setEnv=< true/false > -e yaml
      ```

    To create an "App" in a workspace other than the current one, you need to include an additional flag `workspaceid=< workspaceID >` or you can set that particular workspace, Use command :

       To add workspaceid=< workspaceID > :
       ```
       initz create app --name=< name > --user=< user > --repo=< repo > --branch=< branch > --port=< port > --workspaceid=< workspaceID >
       ```

       To set the organization :

       ```
       initz set workspace --workspaceid=< workspaceID >
       ```


    


