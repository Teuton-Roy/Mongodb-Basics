# Mongodb-Basics
A repo where I'm going to create a README.MD file which is basically about MongoDB

# How to Download MongoDB 🤔🤔
# Search [Download MongoDB Community Server] for download mongodb.

# After download mongodb you need a shell. So, Search Download mongodb shell.
   # In platform,if you are a windows user then search [Windows 64bit(8.1+)(MSI)] version and download.

#--------------------------------------------------------------------------------------------------------------------------------------------------------#

# A. What is Mongodb 🤔? 
    1. MongoDB is a document database designed for ease of development and scaling.
    2. It is intuitive and easy to use NoSQL database.
    3. It's community edition itself is very powerful
   
   
# B. Difference between Mongo and MongoD 🤷‍♂️?
    * "Mongo" is command-line shell that connects to a specific instance of MongoD. // Simply we can say, Mongo where we issue the command or like a program.
    * "MongoD" is the "Mongo Daemon" it's basically the host process for the database. // Simply we can say, MongoD is a type of compiler not exactly a complier.
   
# C. Comprarission of MongoDB with MySql ?
   ![cp](https://user-images.githubusercontent.com/70527737/211202330-2c216f05-634e-4866-89e5-e4e23a0220e5.png)
   
# --------------------------------------------------------------------------------------------------------------------------------------------------- #


# Basic Codes...😁

# we can write code on "MongoDB Compass" GUI as well as on "Mongodb shell" also known as Mongosh.

## All MongoDB Commands 🖊️##

# In this repo, we will see a comprehensive list of all the MongoDB commands you will ever need as a MongoDB beginner. This list covers almost all the most used commands in MongoDB.
# I will assume that we are working inside a collection named 'Your_Collection_name' on a MongoDB database of your choice.



# 1. Database Commands
   # View All Databases : 
     show dbs
   
   # Create a new or switch databases :
      use dbname {your_databasename}
   
   # View current Database :
      db
      
   # Delete Database :
      db.dropDatabase()

# 2. Collection Commands
   # Show Collections
      show collections
   
   # Create a collection named ('As-your-wish')
      db.createCollection["your-collection-name"]
   
   # Drop your named collection
      db.(your-collection-name).drop()
    
# 3. Row(Document) Commands
   
   # Show all Rows in a Collection
      db.(your-collection-name).find()
   
   # Find the first row matching the object
      db.(your-collection-name).find({"name" : "Teuton Roy"})
   
  # Suppose [Student_info] is my Collection name..
   # Insert One Row
     db.Student_info.insert({
    "name": "Teuton Roy",
    "Registration_no.": '2021PGCACA070',
    "DOB" : "2000-03-18"
 })
 
   # Insert many Rows
       db.Student_info.insert([{
    "name": "Teuton Roy",
    "Registration_no.": '2021PGCACA070',
    "DOB" : "2000-03-18"
    },
    {
     "name": "Debasish Biswas",
    "Registration_no.": '2021PGCACA057',
    "DOB" : "1999-08-29"
    },
    {
     "name": "Pragna Biswas",
    "Registration_no.": '2021PGCACA050',
    "DOB" : "2001-03-21"
    }
 }])
 
   # Search in a MongoDb Database
      db.Student_info.find({"name" : "Teuton Roy"})
   
   # Limit the number of rows in output
      db.Student_info.find().limit(2)
     
   # Count the number of rows in the output
      db.Student_info.find().count()
      
   # Find only one row
      db.Student_info.findOne()


   # Update a row 
      Using updateOne, updateMany, or bulkWrite(https://www.mongodb.com/docs/manual/core/bulk-write-operations/).
     
      db.Student_info.updateOne({"name" : "Pragna Biswas"},
                                 {$set: {"Registration_no" : "2021PGCACA050"}}, {upsert: true})
                                 
         upsert : If we want to make a new object in case, no object match in updation.
         
         Syntax : {upsert: <boolean>}
         
   
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
