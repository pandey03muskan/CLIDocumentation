---
sidebar_position: 06
title: "Database"
description: ""
---

- ### Create database using arguments
  Use command :
  ```
  initz create dataservice --name=<name> --type=<type> mode=<mode> --replicas=<replicas> --size=<size> --storage=<storage>
  ```

  :::important 
   Here, the 'name' and 'type' arguments are mandatory, while all others are optional. By default, the mode will be configured as 'Prod(production)', the size will configured as 'Default' with 2GB RAM and 1 vCPU, the replica will default to 1, and the database storage will default to 20GB.
  :::

- ### Create database using file
  Use command :
  ```
  initz create dataservice -f <file path>
  ```
  Example template
  ```json title="database.json"
    {
    "name": "example",
    "data_service_type": "mongodb",
    "mode": "prod",
    "replicas": 1,
    "size": "Default",
    "storage": 20,
    "workspace_id": "669ddebbbc8c54a247229e78"
    }
  ```

  Example template
  ```json title="database.yaml" 
    name: example
    data_service_type: mongodb
    mode: prod
    replicas: 1
    size: Default
    storage: 20
    workspace_id: 669ddebbbc8c54a247229e78
  ```
  You can either use the configuration provided in the file above to create the database or generate your own example configuration to do so.

  - To generate the json configuration
  ```
  initz create dataservice --name=<database-name> --type=<database-type> -e json
  ```

  - To generate the yaml configuration
  ```
  initz create dataservice --name=<database-name> --type=<database-type> -e yaml
  ```

 - ### Delete database
    Use command :
    ```
    initz delete dataservice --name <name>
    ``` 

 - ### How to get list of databases
    Use command :
    ```
    initz get databases
    ```

 - ### Describe a database
    Use command :
    ```
    initz describe dataservice --name <name>
    ```
 
 - ### Download CA certifiacte for postgresql database
   Use command :
   ```
   initz download cacrt --name <name>
   ```
  - ### Check database name
    To check data service name is available or not, use command :
    ```
    initz check dataservice --name <name>
    ```

:::note
- Only PostgreSQL and MongoDB databases are available.
- Only 1/3/5 replicas are available.
- Only Small/Default/Large sizes are available.
- Storage size can be 20 GB to 500 GB.
:::