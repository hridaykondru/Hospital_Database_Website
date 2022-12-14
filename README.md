# Hospital Database Website
## A hospital database system website that supports multi-branch hospitals 
***
This is a web-based database project for maintaining patient information including patient visits, prescriptions and lab tests for hospitals with multiple branches, departments, and doctors. PHP, MySQL, HTML & JavaScript are the technologies used in this project.
## Installation Instructions
* Install XAMPP control panel, Apache and MySQL.
* Start Apache and MySQL services in the XAMPP control panel
* Create a user with username ‘kondru.1’ and password ‘password’ with all privileges
* Insert the following queries in phpMyAdmin one-by-one
    * CREATE DATABASE IF NOT EXISTS `HOSPITAL_DATABASE`;
    * USE `HOSPITAL_DATABASE`;
    * CREATE TABLE IF NOT EXISTS `HOSPITAL` (`Hospital_ID`int NOT NULL AUTO_INCREMENT PRIMARY KEY,`Hospital_Name` varchar(255) NOT NULL, `Hospital_Location` varchar(255) NOT NULL);
    * CREATE TABLE IF NOT EXISTS `DEPARTMENT` (`Dept_ID`varchar(255) NOT NULL PRIMARY KEY,`Dept_Name` varchar(255) NOT NULL, `Hospital_ID` int NOT NULL, `HOD_ID` int, `Patient_Count` int);
    * CREATE TABLE IF NOT EXISTS `DOCTOR` (`Doctor_ID`int NOT NULL AUTO_INCREMENT PRIMARY KEY, `Doctor_Name` varchar(255) NOT NULL,`Dept_ID` varchar(255) NOT NULL, `Work_Email` varchar(255),`Phone_No` BIGINT,`Doctor_Image` longblob, `Patient_Count` int, `Join_Date` DATE NOT NULL,`Leave_Date` DATE);
    * CREATE TABLE IF NOT EXISTS `PATIENT` (`Patient_ID`int NOT NULL AUTO_INCREMENT PRIMARY KEY,`Patient_Name` varchar(255) NOT NULL, `Phone_No` BIGINT, `Alt_Phone_No` BIGINT, `Patient_Image` longblob,`Register_Date` DATE NOT NULL);
    * CREATE TABLE IF NOT EXISTS `PATIENT_RECORD` (`Record_ID`int NOT NULL AUTO_INCREMENT PRIMARY KEY,`Patient_ID`int NOT NULL,`Doctor_ID`int NOT NULL, `Prescription_IMG` longblob NOT NULL, `Tests_IMG` longblob, `Payment` int,`Consultation_Date` DATE NOT NULL );
    * INSERT INTO hospital VALUES ('Apollo Secunderabad','Pollicetty Towers, St. Johns Road, beside Keyes High School, Secunderabad, Telangana 500003');
    * INSERT INTO hospital VALUES ('Apollo Jubilee Hills','Rd Number 72, opposite Bharatiya Vidya Bhavan School, Film Nagar, Hyderabad, Telangana 500033');
* Download the project files and put them in a folder with name <folder_name>
* Move the folder to the `xampp/htdocs/` folder
* Open the website `http://localhost/<folder_name>/hospital_page.php`
