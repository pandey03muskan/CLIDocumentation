---
sidebar_position: 05
title: "Custom Domain"
description: ""
---

# Custom Domain
    When you deploy your application, you'll receive a unique URL for each environment (test, staging, production). By using custom domain, you can replace these default URLs with your own, personalized URL for your application.

- ### Create custom domain
    Use command :
    ```txt title="Using appid"
    initz create customdomain --appid=<appid> --test=<test> --stg=<stg> --prod=<prod>
    ```

    ```txt title="Using app name"
    initz create customdomain --appname=<appname> --test=<test> --stg=<stg>
    ```

- ### Get custom domain 
     Use command :
     ```txt title="Using appid"
     initz get customdomain --appid=<appid>
     ```

     ```txt title="Using app name"
     initz get customdomain --appname=<appname>
     ```

  