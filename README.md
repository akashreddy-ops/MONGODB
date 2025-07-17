# MONGODB
✅ Step-by-Step Guide for MongoDB Setup and Usage (for MERN Stack)

📌 1. Introduction
This repository helps beginners understand how to set up and use MongoDB with examples and integration in a MERN stack project.

🧰 2. Prerequisites
  - Before getting started, make sure you have:

  - Node.js installed

  - Git installed

  - Code editor (like VS Code)

  - Internet connection

🔽 3. Download and Install MongoDB

   1. Go to https://www.mongodb.com/cloud/atlas
   2. Sign up for a free account.
   3. Create a new project and cluster.
   4. Add a user and set up a password.
   5. Click “Connect” > Choose “Connect your application”.
   6. Copy the connection string (something like: mongodb+srv://<username>:<password>@cluster.mongodb.net/?retryWrites=true&w=majority).

Option 2: Install Locally
  1. Visit https://www.mongodb.com/try/download/community
  2. Choose your OS and download the MongoDB Community Server.
  3. Install it and make sure to also install MongoDB Compass (GUI tool).
  4. Open Terminal and type:

           mongod


🖥️ 4. Using MongoDB in Your Project
    Basic Commands : - 

              # Create a new database
                      use myDatabase;
                              
              # Show all databases
                      show dbs;
                              
              # Create collection
                      db.users.insertOne({ name: "Akash", age: 22 });
                              
              # Find all documents
                      db.users.find();
                              
              # Delete a document
                      db.users.deleteOne({ name: "Akash" });


⚙️ 5. Connect MongoDB to a MERN Stack App
    Backend (Node.js + Express)
        1. Install dependencies:
        
                  npm install mongoose express cors

  2. Example server.js:

         const express = require('express');
          const mongoose = require('mongoose');
          const cors = require('cors');
          
          const app = express();
          app.use(cors());
          app.use(express.json());
          
          mongoose.connect('your-mongo-connection-string-here', {
            useNewUrlParser: true,
            useUnifiedTopology: true
          });
          
          app.listen(5000, () => {
            console.log('Server is running on port 5000');
          });


🌐 6. Websites Built with MongoDB
You can also include example websites you’ve built like:

- Elite Edge Fitness

- Money Tracker

- Food Delivery App

- And any other MERN stack apps

              
