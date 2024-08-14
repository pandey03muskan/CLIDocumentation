---
sidebar_position: 08
title: "Profile"
description: ""
---

# Manage Your Profile

- ### Get profile
  Use command :
  ```
  initz get userprofile
  ```

- ### Update your profile
  Use command :
  ```
  initz edit userprofile -f <file path>
  ```

  Example template
  ```json title="userprofile.json"
    {
    "user_info": {
    "first_name": "Jhon",
    "last_name": "Doe",
    "phone_number": "202 55 0111",
    "address": {
    "city": "city",
    "state": "state",
    "country": "country",
    "zip_code": 0,
    "street_address": ""
            }
        }
    }
  ```

  Example template 
  ```json title="userprofile.yaml"
  userinfo:
    firstname: Jhon
    lastname: Doe
    phonenumber: "202 55 0111"
    address:
        city: city
        state: state
        country: country
        zipcode: 0
        streetaddress: ""
  ```

  You can either use the configuration provided in the file above to edit your profile or generate your own example configuration to do so.

  - To generate json configuration
  ```
  initz edit userprofile -e json
  ```

  - To generate yaml configuration
  ```
  initz edit userprofile -e yaml
  ```

 - ### Get credits
    To get the credits for your organization, Use command :
    ```
    initz get credits
    ```

 - ### Describe Organization
     To see details of organization, use command :
     ```
     initz describe org
     ```

  - ### Deactivate your account 
    Are you sure you want to delete your account? Once you delete your account, there is no going back. Please be certain.
    Use command :
    ```
    initz delete account
    ```
    :::danger
    - Once your account is deactivated, you will not be able to register again with the same email.
    :::