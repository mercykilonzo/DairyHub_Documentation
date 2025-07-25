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


