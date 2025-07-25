# DairyHub_Documentation
Introduction DairyHub is a digital platform in Rwanda designed to connect dairy farmers with trusted agricultural suppliers, streamlining the entire supply and communication process. The platform aims to enhance operational efficiency, transparency, and access to quality resources within the dairy value chain, benefiting all stakeholders by fostering better coordination and timely service delivery. Farmers interact with DairyHub through a mobile app that allows them to access services, manage orders, and receive important updates. Suppliers manage their side of the business via a web dashboard, which facilitates purchase and communications. Additionally, there is an informational website that educates and guides users to maximize platform benefits and improve knowledge.

**Target Users**


| **User Type** | **Platform** | **Need**                                                |
|---------------|--------------|---------------------------------------------------------|
| Farmers       | MobileApp    | Purchase inputs, get product information, track orders  |
| Supplier      | Dashboard    | Upload product info, manage inventory/orders            |
| Admin         | Django       | Monitor activity, manage users & systems                | 



Design And Prototype

All DairyHub designs were created in Figma to ensure a clear, consistent, and user-friendly experience across the platform. These designs include comprehensive mockups for our mobile app, supplier dashboard, and informational website.

You can explore all the detailed mockups and UI flows directly from the following Figma link:

View All Mockups Here Diary Hub mockups


**Mobile App (Farmers)**
  - Mobile application for dairy farmers
  - Browse inputs, access AI product info, track orders, payments, reviews
  - Users: Smallholder and medium-scale farmers
  - Technologies: Android

**Supplier Dashboard**
  - Web dashboard for agricultural suppliers
  - Inventory management, order processing, sales insights
  - Users: Input suppliers.
  - Technologies: React, REST APIs, Data analytics

 **Informational Website**
  - Public website providing educational content and platform guidance.
  - Educate users, FAQ, announcements
  - Users: Farmers, suppliers, public
  - Technologies:  HTML/CSS/JS

 **Order Management System**
  - Central system managing farm input orders, milk collections, and delivery coordination
  - Process orders,  update statuses
  - Users: Farmers, suppliers
  - Technologies: Backend APIs, Databases SQL

**Payment & Transaction Module**
  - Handles m payments, confirms payments, and manages transaction records
  - Track payments, confirm payments.
  - Users: Farmers and suppliers.
  - Technologies: Secure payment gateways(MPESA)

**Backend Servers & Databases**
  - Servers hosting APIs, databases storing user info, orders, payments, product catalogories,payment,orderItem
  - Data processing, secure storage, API delivery
  - Users:  developers

 **AI Product Info Engine**
  - AI-driven recommendations and product info
  - Users: Farmers
  - Technologies: AI/ML models, NLP APIs

 **Below is the system artitechture Diagram:**

  [System Artitechture Diagram](https://lucid.app/lucidspark/9b59d1dc-17bc-44e3-b2df-b68e3f14539d/edit?existing=1&docId=9b59d1dc-17bc-44e3-b2df-b68e3f14539d&shared=true&page=0_0#)


**Product Features**

**For Farmers:**

* **Browse farm inputs & equipment**: Farmers can easily explore and access a variety of agricultural inputs such as feed, medicines, and farming equipment needed for better dairy farming operations.

* **In-app product info using AI**: The app leverages AI technology to provide detailed and personalized information about products to help farmers make informed purchasing decisions.

* **Order tracking**: Farmers can track their orders to check order status , enabling them to know the status of their purchases from ordering to delivery.

* **Payment and transaction management (added)**: Farmers can view payment statements, track payments from milk sales, and manage transactions securely within the app, ensuring transparency and timely receipt of funds.


**For Supplier:**

 * **Inventory management:** Suppliers can monitor stocks  to avoid stockouts or overstocking, ensuring the right products are always available for farmers.

* **Order processing:** The system streamlines order receipt, confirmation, packing, and dispatch, helping suppliers fulfill orders efficiently and coordinate pickups.

* **Sales insights:** Suppliers receive detailed analytics and reports on sales , popular products, and customer behavior, aiding smarter decisions about inventory, marketing, and business growth.


**AI Integration**

**AI-Powered Product Query and Explanation**
Objective:
Enable farmers to ask natural language questions about any product within the mobile app and receive clear, AI-generated, context-aware responses covering usage, benefits, risks, and other relevant information.

**Components & How They Work Together**


# Product System Components and Their Roles

- **Natural Language Processing (NLP) Model**  
  - Processes farmer’s queries  
  - Understands intent and key entities  
  - Generates informative, contextually relevant answers using product metadata and training data  

- **Embedded Chat Style UI in Mobile App**  
  - Provides conversational interface for farmers  
  - Allows typing or speaking queries  
  - Delivers AI-generated responses in real-time  

- **Product Database with Structured Meta Data**  
  - Stores detailed and well-organized product data  
  - Includes descriptions, usage, benefits, and risks  
  - Serves as the knowledge base for AI-generated responses  

- **Backend API Layer**  
  - Manages communication between the mobile app and NLP model  
  - Retrieves product metadata efficiently  
  - Handles user session security  


 

 ### Interaction Flow for AI-powered Product Query in DairyHub

- **User Input:**  
  The farmer enters a query (typed or voice) via the mobile app’s chat-style interface.

- **Query Transmission:**  
  The app sends the input query securely to the backend API.

 **NLP Processing:**  
  The backend forwards the query to the Natural Language Processing (NLP) model, which interprets the query’s intent, extracts key information such as product names or concerns, and determines what information the farmer seeks.

 **Metadata Retrieval:**  
  Based on the extracted keywords/entities, the backend queries the product database to fetch structured metadata pertaining to the relevant product(s).

 **Answer Generation:**  
  The NLP model combines the retrieved metadata and natural language generation techniques to produce a clear, contextually appropriate, and informative response.

 **Response Delivery:**  
  The generated answer is sent back to the mobile app through the API and displayed in the conversational UI.

**Follow-up Handling:**  
  The system maintains conversational context to support follow-up queries, allowing the farmer to ask related questions without needing to repeat context.

### Implementation Considerations

 **NLP Model:**  
  Use a domain-adapted language model specialized in dairy/agriculture terminology.  
  Ensure it can perform intent recognition, entity extraction, and natural language generation grounded in structured product data.

**Database Design:**  
  Maintain a comprehensive, up-to-date product metadata database with fields such as:  
  - Product name  
  - Description  
  - Usage instructions  
  - Benefits  
  - Risks  
  Use indexes and flexible querying to ensure rapid data retrieval.

 **Mobile UI:**  
  Design a simple and intuitive chat-style interface for natural language input (text and possibly voice).  
  Display AI responses clearly, supporting multi-turn conversations and follow-ups.

 **Backend Infrastructure:**  
  Provide scalable, secure RESTful or GraphQL APIs connecting the mobile app to the NLP service and database.  
  Implement caching mechanisms for frequently asked questions to improve response time.  
  Enforce authentication, authorization, and data privacy best practices.

  # System Components

## Frontend

- **Kotlin App:**  
  An Android-based mobile application designed to be intuitive and easy to use for low-tech farmers. It serves as the primary interface for farmers to interact with DairyHub's features.

- **React Dashboard:**  
  A responsive web dashboard with role-based access control. It provides suppliers,  with tailored views and management tools based on their roles.

- **Website:**  
  An informational website that offers an introduction to DairyHub, detailed product information, and user guides to help farmers and stakeholders understand and use the platform effectively.

## Backend

- **Django Framework:**  
  The core backend framework responsible for handling all API requests, managing business logic, and providing secure authentication services to the platform.

- **PostgreSQL:**  
  A robust relational database used for storing all transactional data, including user information, orders, payments, and product metadata.

- **AI Microservice:**  
  An AI-powered service, either hosted externally or in-house, accessible via a REST API. It powers features such as natural language processing for product queries and generates intelligent responses for farmers.


### Visual Architecture Overview

![DairyHub Infromational website](https://dairyhub.netlify.app/)

# Testing Strategies
To ensure DairyHub’s reliability and quality, we follow a comprehensive testing approach covering multiple levels:

**Types of Testing**

**Unit Testing:**

Tests individual components such as Django model validations and React components to ensure they work correctly in isolation.

**Integration Testing:**

Validates the interaction between modules, including API endpoints and data flow among React, Kotlin, and Django parts.

**Tools Used**

Django TestCase: For backend testing.

React Testing Library / Jest: For frontend component testing.

Postman: For manual and automated API testing.

**Test Coverage Highlights**

User login and authentication

Product search functionality

Complete order lifecycle

AI query endpoint accuracy


**DairyHub Project Overview & Release Notes**

**Project Details**

- **Start Date:** May 2025  
- **Deployment:** Hosted on **Heroku**  
- **Frontend Stack:** React (for Supplier Dashboard & Farmer App)  
- **Backend Stack:** Django REST Framework  
- **Mobile App:** Kotlin (Android)  
- **Design:** Figma (UI/UX Prototypes, Responsive & Mobile-Friendly)  
- **Project Management:** JIRA (Agile, Sprint-Based)  
- **Testing:** Unit & Integration Tests using React Testing Library, Jest, Pytest, and Django Test Client  
- **Research Period:** 2 Weeks Desk Research + 2 Weeks Secondary Research  
- **AI Component:** Smart Product Assistant (Planned in upcoming versions)


**Core Features**

- **Information Website:** Static informational pages about DairyHub and platform overview.

- **Supplier Dashboard:**  
  - Dashboard Overview with revenue percentages, graphs, and circle stats for quick insights.  
  - **Orders Management:** View and manage incoming and past orders.  
  - **Product Management:**  
    - Add, Edit, Delete products via modal pop-ups.  
    - Search and filter products by category (Equipment, Feed).  
    - Pagination support and clear error feedback when no results are found.  
  - **Payment Management:**  
    - Filter payments by status: Paid or Pending.  
    - Search functionality with feedback for no matches.  
    - Display data in a table grid with 4+ columns and pagination.

- **Farmer Mobile App:**  
  - Browse and order products, integrated with the supplier API .

- **API:**  
  - Built with Django REST Framework.  
  - Hosted on Heroku.  
  - Consumed by both the React dashboard and Kotlin mobile app.

- **Testing:**  
  - Unit testing for individual components.  
  - Integration testing across features in both React frontend and Django backend.

- **Design:** All UI mockups and workflows designed in Figma, ensuring responsive design and seamless user experience across devices.

- **AI Feature (Planned):**  
  - Smart Product Assistant to provide explanations about product use and benefits to buyers.


**Upcoming Release**

**Planned Enhancements**

- Integration of AI assistant with chat and voice capabilities.
- Implementation of a rating and review system.
- Enhanced reporting features including PDF exports.



## Testing Summary

- Comprehensive unit and integration tests cover all critical modules.  
- Key functionalities tested include data fetching, user input validation, search capabilities, modals handling (add/edit/delete), and error display.  
- Testing tools include React Testing Library, Jest, Pytest, and Django’s test runner.


## Notes

- Versioning follows **Semantic Versioning** format: **MAJOR.MINOR.PATCH**  
- This initial release creates a solid foundation for DairyHub’s mission to empower farmers and suppliers through streamlined digital tools.









