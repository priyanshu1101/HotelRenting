# Hotel Renting - Spring Framework
### Project Description :
#### _Tech Stack: Java · Spring Framework · CSS · MySQL · HTML_
This website is a hotel renting system that allows multiple sellers and buyers to register and create their profiles. The platform is built using Spring Framework, which is a popular Java-based framework for building enterprise-level applications. This allows for a robust and scalable structure for the website, as well as easy integration with other Java-based tools and technologies.

Sellers can view their profiles, post properties for renting with all the required details, and update or delete properties at any time. They also have the ability to log out, which invalidates their session for added security.

Buyers can also view their profile, add posted hotels to their list, remove already added hotels from their list, and log out when they are finished.

We also added search functionality, which allows users to search for specific keywords in the database. This feature is available to both buyers and sellers and if the keyword matches any field in the database, the corresponding data will be displayed.

For the database, we have used MySQL, which is a widely used and popular open-source relational database management system. This allows for efficient data storage and retrieval, as well as easy integration with the Spring Framework.


## Screenshots:

### Login Page
![Login](https://github.com/priyanshu1101/HotelRenting/assets/77241116/058bfd10-b590-4328-8eac-444b14498d04)
### Register Page
![Register](https://github.com/priyanshu1101/HotelRenting/assets/77241116/a7a967cc-ed0c-4b2d-9813-78add0311dea)

### Buyers Perspective:
#### List of hotels booked by buyer
![Hotel List Shown to Buyer](https://github.com/priyanshu1101/HotelRenting/assets/77241116/26f96740-cbf8-41af-af44-e2c80678a5f6)

### Seller's Perspective:
#### List of hotels added by the seller
![Modify and Delete Hotel](https://github.com/priyanshu1101/HotelRenting/assets/77241116/c1082abb-7f60-4f0b-80c7-8765d4cbc64c)
#### Post new Hotel 
![Insert Hotel](https://github.com/priyanshu1101/HotelRenting/assets/77241116/2c8ac15f-327a-49ca-87dc-5e23d949b4fe)
#### Search Hotel based on any keyword
![Search Functionality](https://github.com/priyanshu1101/HotelRenting/assets/77241116/9ac85d6b-2473-44cb-85fd-e4b0e12c2e79)


## How to run this project:

Step 1: Clone the Repository Using Git

![image](https://github.com/priyanshu1101/HotelRenting/assets/77241116/0a289c17-f100-40d8-8f5f-3deb167f5d6c)

Step 2: Open with Eclipse For Java Developers (Install Eclipse - https://www.eclipse.org/downloads/packages/ )

![image](https://github.com/priyanshu1101/HotelRenting/assets/77241116/5e66c342-b22e-4f3e-9cbf-e927495e8c8d)

Step 3: Form DataBase
  
  1. Create a database with the name `travel_booking_application` 
  
  Using create statement : 
  
  > CREATE DATABASE `travel_booking_application` /*!40100 DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci */ /*!80016 DEFAULT ENCRYPTION='N' */;
  
  2. Create 3 tables:
  
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
      
      
   
Step 4- Add Apache Tomcat server to your eclipse, for which follow this documentation: https://www.eclipse.org/webtools/jst/components/ws/1.5/tutorials/InstallTomcat/InstallTomcat.html#:~:text=Installing%20server%20runtime&text=Start%20the%20Eclipse%20WTP%20workbench,0%20in%20this%20example)%3A

Step 4: Run the project on the server.

![image](https://github.com/priyanshu1101/HotelRenting/assets/77241116/995cbb2e-b1ea-41a8-8f61-4390c12791b8)

### Let's work together to make this project even better! Feel free to reach out to me at [Linkedin](https://www.linkedin.com/in/priyanshu1101/) if you have any questions or need assistance.






