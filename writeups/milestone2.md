---
layout: default
title: Milestone 2 – Enhancement 1: Software Design and Engineering
---

# **Milestone 2: Enhancement 1  
Software Design and Engineering Narrative**

## **About This Artifact**
This enhancement is the first major step in expanding the original CRUD class I created in CS340 into a more complete and interactive system. It introduces a web based Swagger UI built with FastAPI that connects directly to a MongoDB backend. The goal is to provide a hands on environment where database operations can be tested, explored, and understood in real time. This artifact sets the stage for the next enhancements, which will add more advanced functionality and tie the entire project together.

---

## **Narrative**

This artifact is a new creation rather than something pulled directly from earlier coursework, but it is rooted in the work I did in CS340, Client and Server Development. Back in that course, I built a Python class called `AAC_CRUD_Operations.py` that handled basic create, read, update, and delete operations for a MongoDB database. That original artifact has since gone through a major overhaul for Milestone 4 of this capstone, and those updates were necessary before this enhancement could really take shape. I did build an early version of this enhancement just to show off the limited methods in the original CRUD class, but what you are seeing here is the more complete, evolved version of that idea. That is where the artifact came from.

The purpose of this enhancement is straightforward. I wanted a full stack interface that exposes the methods in the updated CRUD class in a way that is both functional and easy to experiment with. The result is a web based Swagger UI powered by FastAPI, backed by MongoDB, and cobbled together, in the best possible way, from a mix of Python modules and my own logic. It is meant to be hands on. You can poke at the database, run operations, see results instantly, and treat it like a safe sandbox for learning and testing. The next enhancement will add a SQL to Mongo translation layer, and once all three pieces are in place, the whole thing becomes a flexible environment for exploring MongoDB from multiple angles.

As for how this enhancement fits into the CS499 outcomes, here is how I see it.

### **Collaborative environments**
Even though this is a solo project, the final application is designed to support collaborative learning. Anyone, regardless of their experience level, can use the interface to explore MongoDB operations, compare them to SQL, and experiment in real time. It encourages shared understanding, even if the development itself was not a group effort.

### **Professional communication**
This narrative is part of that, but the artifact itself also communicates. The Swagger UI automatically documents every endpoint, every parameter, and every expected response. It is clean, visual, and easy to follow, which is exactly what you want when presenting technical work to a mixed audience.

### **Algorithmic principles and design choices**
The heavy algorithmic lifting will show up more in the next enhancement, but this one still reflects thoughtful design. I had to decide how to structure the API, how to expose the CRUD methods, how to handle errors, and how to make the interface intuitive. Those choices all involve trade offs, and the final design reflects what I felt was the best balance between simplicity and capability.

### **Use of well founded and innovative techniques**
This enhancement leans on solid, well established tools like FastAPI, Uvicorn, and the MongoDB Python driver because there is no point reinventing the wheel. The innovation comes from how the pieces are assembled into a cohesive application that supports the goals of the capstone. It is practical engineering, not theoretical.

### **Security mindset**
Security is part of the design, even if not every feature is fully implemented yet. The application uses a runtime agent to restart on unexpected failures, and the final version will include authentication and more robust access controls. Even now, the API structure and error handling reflect an awareness of how exposed endpoints can be misused and how to mitigate that.

---

## **Conclusion**
Overall, this enhancement represents a significant step forward in the project. It shows how my skills have grown over the course of my studies and how I have learned to take an idea from concept to something functional, testable, and genuinely useful. There is still more to build, but this piece lays the groundwork for everything that comes next.


