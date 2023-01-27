Hello Everyone!

This website is a hotel renting system that allows multiple sellers and buyers to register and create their profiles. The platform is built using Spring Framework, which is a popular Java-based framework for building enterprise-level applications. This allows for a robust and scalable structure for the website, as well as easy integration with other Java-based tools and technologies.

Sellers can view their profile, post properties for renting with all the required details, and update or delete properties at any time. They also have the ability to log out, which invalidates their session for added security.

Buyers can also view their profile, add posted hotels to their list, remove already added hotels from their list, and log out when they are finished.

We also added a search functionality, which allows users to search for specific keywords in the database. This feature is available to both buyers and sellers, and if the keyword matches any field in the database, the corresponding data will be displayed.

For the database, we have used MySQL, which is a widely used and popular open-source relational database management system. This allows for efficient data storage and retrieval, as well as easy integration with the Spring Framework.


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





