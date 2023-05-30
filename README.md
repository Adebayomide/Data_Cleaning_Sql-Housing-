# Nashville Housing Dataset Cleaning




This project involved cleaning and standardizing the Nashville Housing dataset. The dataset contained information about property sales in Nashville, including details such as sale date, property address, owner information, and sale price. The goal of the project was to clean and transform the dataset to make it more organized and consistent for further analysis.


# Dataset and Files

The dataset can be found in this repository as Nashville Housing Data for Data Cleaning(Excel file) while the sql file is named named Nashville Cleaning


# Steps Taken for Dataset Cleaning



**Standardize Date Format:** The first step was to standardize the date format in the dataset. The saledate column was converted to the appropriate date format using the CONVERT function.

**Populate Property Address Data:** The next step was to populate missing property address data. A query was used to identify rows with missing property addresses and sort them by the parcelid.

**Property Address Data Extraction:** The property address data was then extracted into individual columns for better organization. The propertyaddress column was split into separate columns for the address, city, and state using string manipulation functions such as SUBSTRING, CHARINDEX, and LEN.

**Owner Address Data Extraction:** Similar to the property address, the owner address data was also extracted into individual columns. The owneraddress column was split into separate columns for the address, city, and state using string manipulation functions like PARSENAME and REPLACE.

**Standardize 'Sold as Vacant' Column:** The 'soldasvacant' column values were standardized to have consistent values. The column was updated using a CASE statement to replace 'y' with 'n' and 'n' with 'no'.

**Remove Duplicates:** Duplicate records in the dataset were identified based on specific columns such as parcelid, propertyaddress, saleprice, saledate, and legalreference. Using a common table expression (CTE), rows with duplicate values were assigned row numbers. Rows with a row number greater than 1 were considered duplicates and were selected for removal.

**Delete Unused Columns:** Finally, unnecessary columns such as owneraddress, taxdistrict, propertyaddress, and saledateconverted were removed from the dataset using the ALTER TABLE statement.

# Conclusion


This project successfully cleaned and transformed the Nashville Housing dataset. The dataset was standardized by converting date formats, populating missing property address data, and extracting address components into separate columns. Owner address data was also split into individual address, city, and state columns. In addition, inconsistencies in the 'soldasvacant' column were resolved, duplicate records were identified and removed, and unnecessary columns were deleted from the dataset. The cleaned dataset is now ready for further analysis and exploration.