## MALX TECH APPSTORE

# About this project

This is a web project that will be built for mobile app developers, where they can upload their 
apps. This in turn will allow the developers to share their apps with friends, family, clients and employers.
The website will be responsible for:
1. authenticating developers (register and login)
2. display a main page to showcase all apps on 
3. building a dynamically generated page to show info about the click on app
4. building a dynamically generated page to show each developer's app inventory along with his/her name
5. allowing downloads to happen only if a mobile android phone is accessing it
6. generating a url that is specfic to each developer's profile 

# Entities and data fields
1. Developer
    - developer_ID int auto increment Primary Key
    - first_name not null varchar(40)
    - last_name not null varchar(50)
    - username not null varchar(20)
    - email not null varchar(60)
    - password not null varchar(30)
    - developer_url not null varchar(110)

2. Product (App)
    - product_ID int auto increment Primary Key
    - developer_ID not null int
    - app_name not null varchar(40)
    - app_size not null varchar(30)
    - number_of_downloads not null int
    - description not null long text
    - date_published not null date (auto_generated)
    - likes not null int
    - dislikes not null int
    - app_icon not null varchar(40)
    - apk_url not null varchar(40)


3. App_images
    - image_ID int auto increment Primary Key
    - product_ID not null int
    - image_url not null varchar(40)


