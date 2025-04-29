
/*

============ 
Create Database and Schemas
============
Script Purpose:
    This script creates a new database named 'DataWarehouse' after checking if it already exits.
	If the database exits, it is dropped and recreated. Additionally the script sets up three schemas
	within the database : 'Bronze' , 'Silver' and 'Gold'

WARNING:
     Running this script will drop the entire 'Datawarehouse' database if it exits.
	 All data in the databases will be permanently deleted. Proceed with caution
	 and ensure you have proper backups before running this script
*/


USE master;

-- Drop  and recreate the 'DataWarehouse' database

IF EXISTS (SELECT 1 FROM sys.databases WHERE name = 'DataWarehouse')
BEGIN 
    ALTER DATABASE DataWarehouse SET SINGLE_USER WITH ROLLBACK IMMEDIATE;
	DROP DATABASE DataWarehouse
END;
GO

-- Create the 'DataWarehouse' database

CREATE DATABASE DataWarehouse;

USE DataWarehouse;

GO
CREATE SCHEMA bronze;
GO
CREATE SCHEMA silver;
GO
CREATE SCHEMA gold;
GO
