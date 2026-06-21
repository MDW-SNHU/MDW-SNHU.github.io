---
layout: default
title: Milestone 3 – Enhancement 2: Algorithms and Data Structures
---

# **Milestone 3: Enhancement 2  
Algorithms and Data Structures Narrative**

## **About This Artifact**
This enhancement builds on the work completed in Milestone 2 by adding a SQL to MongoDB translation engine. The goal is to let users enter familiar SQL commands and have them translated into equivalent MongoDB operations. This enhancement highlights my abilities in algorithms, data structures, and practical problem solving. It also ties directly into the full stack environment created in the previous milestone, allowing users to test SQL commands through the Swagger UI and see how they map to MongoDB queries.

---

## **Background and Origin**
The idea for this enhancement goes back to the work I did in CS340, where I created a simple CRUD module for MongoDB. After that course, I continued using MongoDB in my professional work and noticed that some operations could be made easier for casual or new users. SQL is familiar to many people who work with relational databases, so the idea of translating SQL commands into MongoDB operations seemed like a natural next step.

When choosing artifacts for the capstone, the CRUD module from CS340 stood out as a solid foundation. It became the basis for all three enhancements in this project. This enhancement, the second of the three, focuses on algorithms and data structures by implementing a translation routine that accepts SQL input and produces MongoDB commands that achieve the same effect.

---

## **What the Algorithm Does**
At its core, this enhancement is a single, complex algorithm. It takes a SQL command as input, breaks it into meaningful components, identifies the intended operation, and constructs the appropriate MongoDB command. The goal is not to support every possible SQL feature, but to provide a functional and understandable translation for the most common operations: SELECT, INSERT, UPDATE, and DELETE.

The algorithm acts like a recipe. It accepts input, processes it step by step, and produces a predictable output. As Wikipedia puts it, an algorithm is a finite, step by step set of defined instructions designed to solve a specific problem or perform a task (Algorithm, 2026). This enhancement fits that definition perfectly.

---

## **How the Algorithm Works**
The translation process follows a clear sequence.

### **1. Input Parsing**
The SQL command is accepted as a raw string. Before anything else can happen, the text is cleaned and normalized. Quoted strings and identifiers are preserved so they are not accidentally altered during processing.

### **2. Tokenization**
The command is broken into pieces. These pieces include:

- The primary SQL command  
- Keywords that modify behavior  
- Field names and values  
- Conditions and filters  

This step turns a long SQL statement into manageable parts.

### **3. Keyword Detection**
The algorithm identifies the important keywords that define the operation. For example:

- SELECT  
- FROM  
- WHERE  
- INSERT INTO  
- UPDATE  
- DELETE  

Each keyword helps determine what the final MongoDB command should look like.

### **4. Command Routing**
Once the primary command is known, the algorithm routes the input to the appropriate handler. Each SQL command type has its own routine designed specifically for that operation.

### **5. Output Construction**
The final step is assembling the MongoDB command. This includes:

- Selecting the correct collection  
- Building filters  
- Creating update or insert structures  
- Formatting the output for display in Swagger  

The result is shown directly in the Swagger UI so users can see exactly what the translation produced.

---

## **Data Structures Used**
This enhancement makes heavy use of Python data structures. Some examples include:

- **Dictionaries** to store parsed components and build MongoDB commands  
- **Lists** to hold tokens, keywords, and intermediate values  
- **JSON like structures** for MongoDB operations  
- **Returned objects** from FastAPI for consistent output formatting  

Throughout the enhancement, data is accepted, manipulated, and returned in multiple forms, making data structure management a central part of the work.

---

## **Integration with Previous Enhancements**
This enhancement depends on the work completed in Milestone 2. The SQL translation routine requires:

- A connected MongoDB database  
- A selected collection  
- The MongoManager class and its methods  
- The Swagger UI interface  

All of these pieces must work together. Without a connected database or an active collection, the SQL translation cannot function. Integrating this enhancement helped clarify how the components of the project interact and depend on one another.

---

## **Alignment with CS499 Outcomes**

### **Professional communication**
This narrative and the accompanying audio explanation demonstrate clear communication of the design, purpose, and function of the enhancement. The Swagger UI also communicates visually by documenting each endpoint and showing the results of each operation.

### **Algorithmic principles and design choices**
The enhancement is built around a complex algorithm that parses, interprets, and translates SQL commands. The design required careful consideration of trade offs, especially when deciding how to break down SQL statements and how to map them to MongoDB operations.

### **Use of well founded and innovative techniques**
The enhancement uses established tools like FastAPI, Pydantic, and the MongoDB driver. The innovation comes from how these tools are combined with custom logic to create a functional SQL to MongoDB translator.

### **Collaborative environments**
By allowing SQL users to explore MongoDB through familiar commands, the enhancement supports collaborative learning. It helps bridge the gap between relational and non relational database users and provides a shared environment for experimentation.

---

## **Lessons Learned During Development**
The first approach I took was to treat the SQL command as a whole and break it down piece by piece as I encountered each part. This quickly became complicated and slowed progress. Eventually, I stepped back and realized that treating the SQL command as a set of components would be much easier.

Once I separated operators, modifiers, and data elements, the process became much clearer. After finishing the SELECT translation, the INSERT, UPDATE, and DELETE commands came together quickly because many of the same components were reused.

Integrating this enhancement with the previous one also helped me understand how the pieces of the project fit together. The SQL translator relies on the database connection, the selected collection, and the underlying CRUD operations. Without all of these working in harmony, nothing functions correctly.

---

## **How to Use the Enhancement**
A full setup guide is available in the project repository, but the basic workflow is simple.

1. Start the Swagger UI.  
2. Authenticate using the function in the Authentication section.  
3. Create or select a database and collection.  
4. Load test data if needed.  
5. Use the `/sql/execute` function in the SQL Helper section to enter SQL commands.  
6. View the translated MongoDB output and results.

For testing, I used a modified version of the Billboard Top 100 dataset (Hollingshead, 2026). Once the data is loaded, SQL commands can be executed and translated through the interface.

---

## **Conclusion**
This enhancement represents a significant step forward in the project. It demonstrates my ability to design and implement a complex algorithm, manage data structures effectively, and integrate multiple components into a cohesive system. It also provides a practical tool for exploring MongoDB through familiar SQL commands. There is still room for refinement, but the foundation is solid and functional.

---

## **References**
Algorithm. (2026, May 15). In Wikipedia. https://wikipedia.org/wiki/Algorithm

Hollingshead, M. (2026). billboard hot 100 [Source code]. GitHub. https://github.com/mhollingshead/billboard-hot-100

