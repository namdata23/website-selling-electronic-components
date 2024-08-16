# Electronic Components Selling Website

![Banner](https://png.pngtree.com/png-clipart/20220627/original/pngtree-colored-isolated-semiconductor-electronic-components-isometric-icon-set-with-motherboard-chips-png-image_8207768.png)

## Introduction

**Electronic Components Selling Website** is a project aimed at providing an online shopping platform for electronic components. This website allows users to search, view details, and purchase electronic components easily and quickly.

## Features

- Search products by category and keyword
- View product details
- Add products to the cart
- Online payment
- Manage users, product categories, product types, permissions, and view statistics

## Technologies Used

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: ASP.NET
- **Database**: SQL Server

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/namdata23/website-selling-electronic-components.git
    ```

2. Navigate to the project directory:
    ```bash
    cd website-selling-electronic-components/WebsiteBanLinhKienDienTu15
    ```

3. Open the project with Visual Studio and start the project.

## Customer Usage

1. Access the homepage of the website.
2. Search and select the products you want to buy.
3. Add products to the cart.
4. Proceed to checkout.

## Administration Usage

Manage:
1. Users.
2. Products.
3. Product details.
4. Order details for customers.
5. User permissions.
6. View statistics.

## Authors

- **Michael Nam** - [namdata23](https://github.com/namdata23)
- **MiNhan** -  [nhanbuimy](https://github.com/nhanbuimy)

## Contact

If you have any questions or suggestions, please contact via email: namitwork23@gmail.com

---
When you want to run my project: 
--- Steps to set up and run the program:
	+ In the Solution Explorer, find the file named "appsettings.json" and locate the "ConnectionStrings" configuration section.
	+ There are two values you need to focus on: "Server=...." and "Database=....".
	+ By default, these values are pointing to the server and database on my machine, so you need to change them to run on your device.
	+ Open SSMS on your machine and copy the "Server name", then paste it into the "Server=...." field.
	+ For the "Database=...." value, you can enter any name. If the database already exists on the server you specified, the application will connect to it; otherwise, it will create a new database on that server.
	+ At this step, it's best to select Build => Rebuild solution (or Ctrl + Alt + F7) to rebuild the solution.
	+ After editing the two values and rebuilding the solution, run the application (F5 / Ctrl + F5).

--- When running the application for the first time (no database yet):
	+ The application will automatically create two default roles: Admin and User (you can see these roles in the AspNetRoles table).
	+ The application will automatically create a default user with the Admin role (you can see this user in the AspNetUsers table).
	+ In the Program and LinhKienDienTuContext files, you can change the username and password as you wish before running the appsettings.js file to initialize the database.

-- Check if the program is running correctly:
	+ When the application runs, you will access a localhost page. Currently, since there is no product data in the database, you will not see anything on the homepage except for three buttons: "ShopElec" (home button), "Register", and "Login".
	+ Log in to the admin account and check the admin tabs.
	+ In SSMS, log in to your server and find the database with the name you set earlier (both the server and database names are the ones you set in the ConnectionStrings section).
	+ You can select a few tables to check; all tables will be empty except for the AspNetUsers table (containing 1 user, which is Admin), the AspNetRoles table (containing 2 roles: User and Admin), and the AspNetUserRoles table (to record the assignment of the Admin user to the Admin role).
	+ At this step, you can open the SQL script I attached (Data.sql), modify the server name in the "USE ......" section to match the database name, and run it to prepopulate data in the Category, SpecialTag, and Product tables.

From subsequent runs, if you don't change the "Database" value, the application will continue to connect to the created database. If you change the value, a new database with the new name will be created, while the old database will remain intact. If you change the name back to the old one, you can still connect to it.
---------------------
Thank you for using and contributing to our project!
