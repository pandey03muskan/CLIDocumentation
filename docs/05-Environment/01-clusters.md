---
sidebar_position: 01
title: "Cluster"
description: ""
---

# Bring your own cluster
  
  - ### Import cluster using arguments
    Use command :
    ```
    initz import cluster --name <cluster-name> --mode <cluster-mode> --provider <provider> --url <cluster-url>
    ```

  - ### Import cluster using file
    Use command :
    ```
    initz import cluster -f <file path>
    ```

    Example template :
    ```json title="cluster.json"
     {
     "name": "example",
     "cluster_url": "https://www.example.com",
     "provider": "AWS",
      "mode": "prod"
     }
    ```
    Example template :
    ```json title="cluster.yaml"
     name: example
     cluster_url: https://www.example.com
     provider: AWS
     mode: prod
    ```

    You can either use the configuration provided in the file above to import the cluster or generate your own example configuration to do so.
    - To generate json configuration :
    ```
    initz import cluster --name <cluster-name> --mode <cluster-mode> --provider <provider> --url <cluster-url> -e json
    ```

    - To generate yaml configuration :
    ```
    initz import cluster --name <cluster-name> --mode <cluster-mode> --provider <provider> --url <cluster-url> -e yaml
    ```
    :::note 
    - While importing the cluster, you will have the option to download the cluster configuration. After downloading, you will receive two files: one named crdtemplate.yaml and the second named deployment configuration file (your_cluster_name.yaml). Download the configuration and apply it to your cluster.
    - After applying the configuration file to your cluster, validate it.
    :::

  - ### Download cluster-config
    Use command :
    ```
    initz download cluster-config --name <cluster-name>
    ```

   - ### Delete cluster 
     Use command :
     ```
     initz delete cluster --name <cluster-name>
     ```

   - ### How to get list of clusters
     Use command :
     ```
     initz get cluster
     ```
     In order to get information about specific cluster, Use command :
     ```
     initz get cluster <cluster-name>
     ```

   - ### Check cluster name
      To check cluster name is available or not, use command :
      ```
      initz check cluster --name <cluster-name>
      ```


:::important
 - Mode can be prod/Non-prod only.
 - Only AWS/Azure/Civo providers are available.
:::