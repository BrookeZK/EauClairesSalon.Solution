# Eau Claire's Salon: Stylist-Client Database

#### _Code Review for Week 11 - 3/20/2020_

#### _By Jonathan Carlos_

## **Description**

_This C# codebase will build a user-friendly application for Eau Claire's Salon, allowing her to manage and keep track of her stylists, their specialties, and the client relationships that they carry._

## Preview


## **Behavior Driven Development**

| Behavior | Input | Output |
|----------|:-----:|--------|
| Pierre enters vendor name. | "Suzie's Cafe" | newVendor.name == "Suzie's Cafe" |
| Pierre enters vendor description. | "Newest cafe in town." | newVendor.description == ""Newest cafe in town."|
| Pierre adds an order title to a vendor. | "Croissants." | newVendor.order.title == "Croissants." |
| Pierre adds an order description to a vendor. | "Cream filled croissants." | newVendor.order.title == "Cream filled croissants."
| Pierre adds an order price to a vendor. | "20" | newVendor.order.price == 20 |
| Pierre adds an order date to a vendor.| "05/01/2020" | newVendor.order.date == "05/01/2020" |
| Pierre is greeted with a welcome splash page. | localhost:5000/ | route == "/" |
| Pierre clicks on a link that sends him to a form where he can add a vendor. | "click" | route == /form |
| Pierre clicks on a vendor's name and it goes to a page that displays all of that vendor's orders. | "click" | route == /vendors/orders/ |
| Pierre clicks on a link that presents a form for a new order for a particular vendor. | "click" | route == /vendors/1/orders/new |


## **Minimum Viable Product (MVP)**

The MVP of this project is to allow Eau Claire to add new stylists, new clients to a specific stylist (this will not be available if no stylists have been added), and be able to select a stylist, see their details, and a list of clients that belong to that stylist.

Stretch goals include:

* Adding a form where employees may search for a stylist by name and display a list of all results.
* Adding a form where employees may also search for a client by name. Display a list of all results.
* Adding a feature for adding an appointment to a client.
* Adding a feature for adding an appointment to a stylist.
* Adding a feature for keeping track of how much each stylist was paid for each appointment.

## **Setup/Installation**

*Installing .NET Core* 

1. Download the .NET Core SDK [Software Development Kit](https://dotnet.microsoft.com/download).
2. Open the .Net Core SDK file and install.
3. Confirm the installation was successful by runnning the `$ dotnet --version` command in your terminal (You should see something like this in the response: `2.2.105`).
4. Install the dotnet script REPL tool by running the `$ dotnet tool install -g dotnet-script` command in your terminal.
5. Restart your terminal to complete the installation.

*Installing MySQL | MacOS:*

1. Download the MySQL Community Server DMG File from [MySQL Community Server](https://dev.mysql.com/downloads/file/?id=484914)
2. You can exit the mysql program by entering `exit`.
3. Download the MySQL Workbench DMG File from [MySQL Workbench](https://dev.mysql.com/downloads/file/?id=484391). (Use the No thanks, just start my download link.)
4. Install MySQL Workbench to Applications folder.
5. Open MySQL Workbench and select the `Local instance 3306 server`. You will need to enter the password you set. (We used `epicodus`.) If it connects, you're all set.

*Installing MySQL | Windows 10:*

1. Download the MySQL Web Installer from [MySQL Downloads](https://dev.mysql.com/downloads/file/?id=484919) (Use the No thanks, just start my download link.).
2. Choose `Custom` setup type.
3. When prompted to `Select Products and Features`, make sure you select both `MySQL Server` (Under MySQL Servers), and `MySQL Workbench` (Under applications).
4. When you reach `Configuration`, set `High Availability` to `Standalone`. Defaults are OK under `Type and Networking`. Set `Authentication Method` to `Use Legacy Authenticationn Method`. Lastly, set your password and complete the installation process.
5. You can exit the mysql program by entering `exit`
6. Add the MySQL environment variable to the System PATH. We must include MySQL in the System Environment Path Variable. This is its own multi-step process. Instructions here are for Windows 10:
  a. Open the Control Panel and visit System > Advanced System Settings > Environment Variables...
  b. Then select PATH..., click Edit..., then Add.
  c. Add the exact location of your MySQL installation, and click OK. (This location is likely `C:\Program Files\MySQL\MySQL Server 8.0\bin`, but may differ depending on your specific installation.)
7. Open MySQL Workbench and select the `Local instance 3306` server (it may have a different name). You will need to enter the password you set (We used `epicodus`). If it connects, you're all set.

*MySQL Workbench Database Setup:*

1. Open your terminal.
2. Enter the command `mysql start` to run the MySQL server.
3. Enter the command `mysql -u{server-name-goes-here} -p{password-goes-here}` to acces MySQL.
4. Enter `CREATE DATABASE Jonathan_Carlos;` to create a database.
5. Enter `USE Jonathan_Carlos`; to connect to the database. You can confirm that you have connected to your new database by executing the `SELECT DATABASE();`
6. Enter `CREATE TABLE stylists (StylistId PRIMARY KEY, Name VARCHAR(255), Specialty VARCHAR(255));` to create a `stylists` table with columns titled `StylistId`, `Name`, and `Specialty`.
7. Enter `CREATE TABLE clients (ClientId PRIMARY KEY, Name VARCHAR(255), Description VARCHAR(255), StylistId INT));` to create a `clients` table with columns titled `ClientId`, `Name`, `Description`, and `StylistId`.

*Cloning this repository:*

1. Open your terminal.
2. Navigate to the desired directory in which you want to clone this repository.
3. Use the command `git clone https://github.com/jonathancarlos21/Eau-Claires-Salon` to clone this repository.
4. Open this repository from within your terminal and navigate to `HairSalon/`.
5. Run the command `dotnet restore`.
6. Run the command `dotnet build`.
7. If build is successful, run the command `dotnet run`. If build failed, make necessary updates and repeat `dotnet restore` followed by `dotnet build`.
8. Use `dotnet run` to generate a local server.
9. Copy and paste the given `localhost:5000` onto your URL.

*Downloading this repository:*

1. On the top right of this page, click the "Clone or download" button.
2. Click on "Download ZIP."
3. Click the downloaded file to unzip and extract this repository to your desired directory.
4. Open this repository from within your terminal and navigate to `HairSalon/`.
5. Run the command `dotnet restore`.
6. Run the command `dotnet build`.
7. If build is successful, run the command `dotnet run`. If build failed, make necessary updates and repeat `dotnet restore` followed by `dotnet build`.
8. Use `dotnet run` to generate a local server.
9. Copy and paste the given `localhost:5000` onto your URL or use.

## **Known Bugs**

There are no known bugs at this time.

## **Support and contact details**

If you have any questions, comments, or concerns, please feel free to contact the content creator at examplemail@company.net 

## **Technologies used**

* _Git 2.23.0_

* _C# language_

* _.NET Core 2.2.106_

* _dotnet script 0.50.1_

* _Visual Studio Code 1.43.1_

* _Model-View-Controller(MVC) framework_

* _MySQL 8.0.15_

* _MySQL Workbench 8.0.15_

* _Entity Framework Core 2.2.4_

* _Language-Integrated Query (LINQ)_

* _ASP.NET Razor_

* GitBash

## **License**

Copyright (c) 2020 **_Eau Claire's Salon: Stylist-Client Database_**

This software is licensed under the MIT license.