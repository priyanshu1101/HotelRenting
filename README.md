Hello Everyone!
This project is based on hotel renting system.It support multiple sellers and multiple users.Every new user can register themself on the website and create there profile.Now having Login ID and password,they can log in and post there hotel to rent or rent one.Once logged in, a unique session is created which remains valid until the user log out.

Seller side features:
1.View profile
2.Post property for renting with all the required details
3.Once a property is added,seller can later delete or update the infomation added,if required.
4.Logout functionality to invalidate the session to ensure security.

Buyer side features:
1.View profile
2.Add posted hotels to there list.
3.Remove already added hotels from there list.
4.Logout functionality to invalidate the session to ensure security.

Key Features: Added a search functionality under which if the searched keyword matches any field in the database then that data gets displayed.This feature is added both on the buyer and seller side.


How to Install:

Step1: Install mysql.(Database for our project)

  Once Installed:
  
  1.Create a database with a name `travel_booking_application` 
  
  Using create statement : CREATE DATABASE `travel_booking_application` /*!40100 DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci */ /*!80016 DEFAULT ENCRYPTION='N' */;
  
  2.Create 3 tables:
  
    1.Table Name: buyerregister 
      Using create statement:
      CREATE TABLE `buyerregister` (
      `BuyerID` int NOT NULL AUTO_INCREMENT,
      `BuyerName` varchar(45) NOT NULL,
      `Email` varchar(45) NOT NULL,
      `Password` varchar(45) NOT NULL,
      PRIMARY KEY (`BuyerID`),
      UNIQUE KEY `BuyerID_UNIQUE` (`BuyerID`),
      UNIQUE KEY `Email_UNIQUE` (`Email`)
      ) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
      
    2.Table Name: hotelinfo
      Using create statement:
      CREATE TABLE `hotelinfo` (
      `HotelId` int NOT NULL AUTO_INCREMENT,
      `HotelName` varchar(45) NOT NULL,
      `HotelLocation` varchar(50) NOT NULL,
      `Price` int NOT NULL,
      `Duration` int NOT NULL,
      `Rating` int NOT NULL,
      `SellerId` int NOT NULL,
      `BuyerId` int DEFAULT NULL,
      PRIMARY KEY (`HotelId`),
      UNIQUE KEY `TourId_UNIQUE` (`HotelId`)
      ) ENGINE=InnoDB AUTO_INCREMENT=26 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
      
    3.Table Name: sellerregister
      Using create statement:
      CREATE TABLE `sellerregister` (
      `SellerID` int NOT NULL AUTO_INCREMENT,
      `SellerName` varchar(45) NOT NULL,
      `Email` varchar(45) NOT NULL,
      `Password` varchar(45) NOT NULL,
      PRIMARY KEY (`SellerID`),
      UNIQUE KEY `Email_UNIQUE` (`Email`),
      UNIQUE KEY `SellerID_UNIQUE` (`SellerID`)
      ) ENGINE=InnoDB AUTO_INCREMENT=9 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
      
      
Step2: Install Eclipse (https://www.eclipse.org/downloads/packages/) 
      
  Once Installed:
   
  1.Add Apache Tomcat server to your eclipse, for which follow this documentation : https://www.eclipse.org/webtools/jst/components/ws/1.5/tutorials/InstallTomcat/InstallTomcat.html#:~:text=Installing%20server%20runtime&text=Start%20the%20Eclipse%20WTP%20workbench,0%20in%20this%20example)%3A
  
  
Step3: Import the project from github to your eclipse workspace.


Step 4: Run project on server.





