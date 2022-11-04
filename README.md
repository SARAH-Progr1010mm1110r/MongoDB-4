# MongoDB-4
## Using MongoDB to create pipelines, views, dashboards, and indexes

# **Part I (volcanoes_of_earth.csv)**

## **Pipelines/views**
   * Create a new database and a new collection and upload the CSV file to a new collection (you can use MongoDB Compass or Atlas)
   * Connect to MongoDB Atlas.
   * Create aggregation pipelines and create views based on your pipelines. Once you do this, views will appear in MongoDB Atlas or in MongoDB Compass.

### **Pipelines/Views to be Created:**
* Get all volcanoes that located in Japan, with the fields "Volcano_Name", "Volcano_Type", "Country", "Last_Eruption", "Lat", "Lon"
   
* Get all volcanoes where population within 5 km more that 5 thousand people, with the fields "Volcano_Name", "Volcano_Type", "Country", "Last_Eruption", "Lat", "Lon", "population_within_5km"
    
* Get volcanoes per country per volcano type where the population is more than 100,000 people within 10km
     
   * Hint: you can use $group stages and $push keyword

* Retrieve all volcanoes that erupted before the common era (BCE), and get the name, location (country, lon, lat), and elevation. Sort by elevation level from highest to lowest (some of them underwater)
     
* Get volcanoes with the highest and lowest elevation by volcano types.

# **Part II (h_and_m.csv)**

## **Functions/Indexes**

   1- Create a new database and collection, upload the second dataset in the collection

   2- Create indexes and functions and execute them in the Jupyter Notebook

### **Indexes to be Created**
   * Create a Compound Index for the product type name and color.

   * Create another index to improve performance for the query to retrieve product type, color, and price

      * Create a Text Index based on all text fields in the collection.

      * Hint: Instead of mentioning all the text fields one by one, there is a wildcard “$**” which includes all the string fields -> ("$**", pymongo.TEXT)

      * All indexes have to be created in Jupyter Notebook

      * Before creating each index, run explain() on any query of your choice to show the query statistics. The “explain()” function works on the collection connected to your MongoDB Atlas (not Realm).

      * After each index is created, run explain() again to check the performance of the query. Also, to see the list of your indexes to make sure it was created you can use db.collection.list_indexes() or db.collection.index_information() methods.


### **Functions to be created:**
   * In MongoDB Realm create a new app for H&M products (or any other name of your choice)

   * Create a function that returns all the red or orange t-shirts.

   * Create a function that takes two arguments for index_group_name and colour_group_name and returns all documents which correspond to the parameters given. Make sure that arguments are case insensitive (“Red”/”red”/”RED” will work)

xes
