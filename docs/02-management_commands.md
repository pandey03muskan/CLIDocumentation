---
sidebar_position: 02
title: "Account Management"
description: "This section provides essential commands for managing your account"
---

# Account Management
This section provides essential commands for managing your account. Here’s how you can easily take care of your account :

- ## Register 
    Ready to join us? Use this command to set up a new account quickly.

    ### Register using arguments

    ```
    initz register user --email=<email> --username=<username> --org=<org> --password=<password>
    ```

    ### Register using File

    ```
    initz register -f <file-path>
    ```

    *Example user.json file*
    ```
    {
    "email":"example@gmail.com",
    "username":"example",
    "org":"exampleOrg",
    "password":"example@123"
    } 
    ```

    *Example user.yaml file*
    ``` 
    email:example@gmail.com
    username: example
    org: exampleOrg
    password: example@123
    ```
     
  After registering, you will receive an email at your registered address to verify your email. Once you have verified your email, you will be able to log in to your account.


- ## Login 
    Already a member? Just log in here to access your account.

    use command :
    ```
    initz login --email=<email> --password=<password>
    ```

- ## Forgot Password
   No worries if you’ve forgotten your password—use this command to recover it quickly.

   ```
   initz forgotPassword --email=<email>
   ```
   After running this command, you will receive an email to reset your password. Once you have reset your password, it will be successfully updated.
 

- ## Check email 
    To check user with email is already exists or not, use command :
    ```
    initz check email <email>
    ```

- ## check user name 
    To check username already exists or not, use command :
    ```
    initz check user <username>
    ```
  