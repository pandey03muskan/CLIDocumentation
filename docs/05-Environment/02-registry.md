---
sidebar_position: 02
title: "Registry"
description: ""
---

# Bring your own registry

- ### Import registry using arguments
  Use command :
  ```
  initz import registry --name <name> --username <username> --password <password> --url <url> --provider <provider> --namespace <namespace>
  ```

- ### Import registry using file 
  Use command :
  ```
  initz import registry -f <file path>
  ```

  Example template
  ```json title="registry.json"
    {
    "name": "example",
    "password": "example@123",
    "registry_url": "https://hub.docker.com",
    "type": "Docker Hub",
    "username": "example@gmail.com",
    "root": "example_namespace"
    }
  ```

  Example template
  ```json title="registry.yaml"
    name: example
    password: example@123
    registry_url: https://hub.docker.com
    type: Docker Hub
    username: example@gmail.com
    root: example_namespace
  ```

  You can either use the configuration provided in the file above to import the registry or generate your own example configuration to do so.

  - To generate json configuration :
  ```
  initz import registry --name <registry-name> --username <username> --password <password> --url <registry url> --provider <provider> --namespace <namespace> -e json
  ```

  - To generate yaml configuration :
  ```
  initz import registry --name <registry-name> --username <username> --password <password> --url <registry url> --provider <provider> --namespace <namespace> -e yaml
  ```

 - ### Update registry 
    Use command :
    ```
    initz edit registry --name <registry--name> --username <username> --password <password> --namespace <namespace>
    ```

    :::important
     In the registry, you can edit the username, password, and namespace.
    :::

  - ### Delete Registry 
    Use command :
    ```
    initz delete registry --name <registry-name>
    ```

  - ### Get the list of registry 
    Use command :
    ```
    initz get registry 
    ```
    In order to get information about specific registry.\
    Use command :
    ```
    initz get registry <registry-name>
    ```
  
  -  ### Check registry name
     To check registry name is available or not, use command :
     ```
     initz check registry --name <registry-name>
     ```

