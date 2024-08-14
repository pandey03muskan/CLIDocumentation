---
sidebar_position: 01
title: "Introduction"
description: "This will guide to the quick start apps on the Initializ  Workspaces."
---

# Introduction 

   ## Initializ CLI

      The Initializ Command Line Interface (CLI) is a comprehensive tool that offers a consistent interface for interfacing all the features of Initializ.ai. The CLI documentation includes detailed guidance for each feature, providing descriptions, syntax, and usage examples to help you effectively use the CLI.

   ### Syntax
     
   ```
   initz [ COMMAND ] [ TYPE ] [ flags ]   
   ```

      _Use the following syntax to run initz commands from your terminal window._

      Where COMMAND, TYPE and FLAGS are:

   - command : Indicates the action you wish to execute on one or more resources.

      
      
      >**Example :** create, get, delete
      

   - type : Indicates the resource type.

      > initz get cluster  \
      > initz get workspace

   - flag : Indicates the flags.

       > **Example :** --file, --name

   ### Getting started


   - First, set the URL. To do this, simply copy the command below and paste it into the command prompt as it is.
     ```
     initz set url -u "api.initializ.ai" 
     ```
   - Use **initz** to get all the commands.

     ```
     initz
     ```
   - Use **-h or --help** to get information of specific command.
    
     **Syntax :**
     ```
     initz < COMMAND > -h 
     ```

     Let’s look at an example to clarify.

     > **Example :**
     >
     > initz create -h \
     > initz edit -h

     To get information for specific command for specific resource, use :
      
     > **Example :**
     >
     > initz create workspace -h \
     > initz create database -h


:::important
- Do not proceed with other commands without setting the URL.
:::