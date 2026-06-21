---
layout: default
title: Milestone 4 – Enhancement 3: Databases
---

# **Milestone 4: Enhancement 3  
Databases Narrative**

## **About This Artifact**
This enhancement is the database backbone of the entire project. It expands the original CRUD module from CS340 into a full featured MongoDB management layer, complete with authentication, database and collection operations, document handling, indexing, aggregations, backups, and support for the SQL translation engine introduced in Milestone 3. This enhancement demonstrates my abilities in database design, database tooling, and practical data management using MongoDB.

---

## **Background and Origin**
The foundation for this enhancement began in CS340, where I created a simple Python module to perform CRUD operations on a MongoDB database. After that course, I continued using MongoDB in my professional work and realized that many operations could be made easier for casual users. When selecting artifacts for the capstone, the CRUD module stood out as a strong base to build on.

This enhancement is the third of the three, but it is also the one that had to be functional before the others could be developed. The SQL translation engine and the Swagger UI interface both depend on this database layer. Because of that, much of the work for this enhancement was completed early in the project, then refined and expanded as the other enhancements took shape.

---

## **What This Enhancement Does**
This enhancement transforms the original CRUD module into a comprehensive MongoDB management class. It provides a wide range of capabilities, all exposed through the Swagger UI interface created in Milestone 2.

### **Database Operations**
- Authenticate to a MongoDB instance  
- List databases  
- Create new databases  
- Select a database to work with  
- Drop databases  

### **Collection Operations**
- List collections  
- Create collections  
- Drop collections  
- Rename collections  
- Set the active collection  

### **Document Operations**
- Create, read, update, and delete documents  
- Insert multiple documents at once  
- Insert documents from a JSON file  
- Query documents with filters  
- Return results in structured JSON format  

### **Indexes and Aggregations**
- Create and list indexes  
- Perform MongoDB aggregation pipelines  

### **Backup and Restore**
- Export data to JSON  
- Restore data from JSON  

### **SQL Helper Integration**
This enhancement also includes the support routines required by the SQL to MongoDB translation engine from Milestone 3. Without the database layer, the SQL helper would have nothing to operate on.

---

## **How the Enhancement Works**
The enhancement is implemented as a Python class that acts as the central interface to MongoDB. It uses well established modules such as `pymongo`, `pydantic`, and `fastapi` to provide reliable and predictable behavior. The class is imported and used by the Swagger UI script, which exposes each method as an interactive endpoint.

The design focuses on clarity and modularity. Each operation, whether it is creating a database or inserting a document, has its own method. This makes the class easy to maintain and easy to extend. It also makes the Swagger UI interface intuitive, since each method maps directly to a visible function on the screen.

---

## **Integration with the Swagger UI**
The MongoManager class is not a standalone application. It is integrated into the `MongoManager_SwaggerUI.py` script, which provides the web based interface used in Milestone 2 and Milestone 3. Through this interface, users can:

- Authenticate  
- Select databases and collections  
- Run CRUD operations  
- Load data  
- Execute aggregations  
- Perform backups  
- Use the SQL helper  

This integration turns the class into a full stack tool for exploring and managing MongoDB.

---

## **Alignment with CS499 Outcomes**

### **Professional communication**
This narrative, along with the audio explanation, demonstrates clear communication of the design and purpose of the enhancement. The Swagger UI also provides visual communication by documenting each endpoint and showing results in real time.

### **Algorithmic principles and design choices**
Although this enhancement is more database focused, it still involves algorithmic thinking. Decisions about how to structure operations, how to handle errors, and how to manage data flow all required careful design and trade offs.

### **Use of well founded and innovative techniques**
The enhancement uses established tools like MongoDB, FastAPI, and Pydantic. The innovation comes from how these tools are combined into a cohesive system that supports both teaching and practical database management.

### **Collaborative environments**
By providing a tool that can be used by beginners and experienced users alike, this enhancement supports collaborative learning. It allows users to explore MongoDB, test operations, and work with real data in a shared environment.

---

## **Lessons Learned**
Building this enhancement taught me a lot about how MongoDB works behind the scenes and how to design a tool that interacts with it cleanly. I learned how important it is to structure operations in a way that is predictable and easy to follow. I also learned how the different parts of the project depend on one another. The SQL helper, the Swagger UI, and the MongoManager class all have to work together for the system to function.

Adding HTTPS support was another learning experience. The ability to run the interface securely required integrating certificate handling directly into the script, which helped me better understand how secure connections are established in web applications.

---

## **Technical Requirements**
This enhancement relies on several Python modules, including `pymongo`, `fastapi`, `pydantic`, `bson`, and others. A full list of requirements, along with installation and usage instructions, is available in the project repository’s README file.

---

## **Conclusion**
This enhancement is the core of the entire project. It provides the database functionality that the other enhancements rely on and demonstrates my ability to design and implement a complete database management layer. It is flexible, functional, and capable of supporting both teaching and practical use cases. With this enhancement in place, the project becomes a full stack environment for exploring MongoDB and understanding how database operations work.

---

## **References**
Hollingshead, M. (2026). billboard hot 100 [Source code]. GitHub. https://github.com/mhollingshead/billboard-hot-100

