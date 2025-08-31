# 🏡 Airbnb Clone Project

## Overview
The **Airbnb Clone Project** is a full-stack application that simulates the development of a modern booking platform similar to Airbnb.  
This project provides hands-on experience in building scalable web applications while exploring key areas of **backend systems, database design, API development, security, and deployment pipelines**.  

It not only focuses on technical implementation but also emphasizes **collaboration, documentation, and real-world workflows**, preparing learners for industry-grade software development.  

---

## 🎯 Project Goals
- Master **collaborative team workflows** using GitHub.  
- Deepen understanding of **backend architecture** and **relational database design**.  
- Implement **API security measures** to safeguard data and transactions.  
- Build and manage **CI/CD pipelines** for efficient deployment.  
- Document and plan complex software projects effectively.  
- Gain practical experience in integrating **Django, MySQL, GraphQL, and Docker** into a unified ecosystem.  

---

## 🛠️ Technology Stack

This project leverages modern technologies to build a scalable and secure booking platform.  
Below is a breakdown of each technology and its role in the project:  

- **Django**: A high-level Python web framework used to build the backend, handle business logic, and expose RESTful APIs.  
- **MySQL**: A relational database system used to store and manage structured data such as users, bookings, and listings.  
- **GraphQL**: A query language for APIs that enables efficient data fetching and allows clients to request exactly the data they need.  
- **Docker**: A containerization platform that ensures consistent application environments across development, testing, and production.  
- **Git & GitHub**: Version control and collaboration tools for managing project code, team workflows, and documentation.  
- **GitHub Actions**: A CI/CD tool for automating testing, building, and deployment pipelines.  

Each of these technologies contributes to creating a robust, secure, and collaborative development environment, mirroring real-world industry practices.
 

---

## 📌 Key Highlights
- Hands-on GitHub repository setup & management  
- Clear documentation of team roles and responsibilities  
- Database design with real-world entity relationships  
- Feature-driven development approach  
- Secure API implementation  
- CI/CD pipeline integration for automated deployment  

---

## 🗄️ Database Design

The database is designed using a **relational model** to represent users, properties, bookings, reviews, and payments.  
This structure ensures scalability, data integrity, and efficient queries.  

### Key Entities

1. **Users**
   - `id` (Primary Key)
   - `name`
   - `email`
   - `password`
   - `role` (e.g., host, guest)
   - **Relationships**:  
     - A user can list multiple properties.  
     - A user can make multiple bookings.  
     - A user can leave multiple reviews.  

2. **Properties**
   - `id` (Primary Key)
   - `title`
   - `description`
   - `location`
   - `price_per_night`
   - `host_id` (Foreign Key → Users)  
   - **Relationships**:  
     - A property belongs to a host (user).  
     - A property can have multiple bookings.  
     - A property can have multiple reviews.  

3. **Bookings**
   - `id` (Primary Key)
   - `property_id` (Foreign Key → Properties)  
   - `user_id` (Foreign Key → Users)  
   - `check_in_date`
   - `check_out_date`
   - `status` (e.g., pending, confirmed, canceled)  
   - **Relationships**:  
     - A booking belongs to a property.  
     - A booking is made by a user.  
     - A booking is associated with a payment.  

4. **Reviews**
   - `id` (Primary Key)
   - `property_id` (Foreign Key → Properties)  
   - `user_id` (Foreign Key → Users)  
   - `rating` (1–5 stars)
   - `comment`
   - **Relationships**:  
     - A review belongs to a property.  
     - A review is written by a user.  

5. **Payments**
   - `id` (Primary Key)
   - `booking_id` (Foreign Key → Bookings)  
   - `amount`
   - `payment_method` (e.g., card, PayPal, M-Pesa)
   - `status` (e.g., pending, completed, failed)  
   - **Relationships**:  
     - A payment is linked to a booking.  

---

### Entity Relationships Summary
- A **User** can be a host (owning properties) or a guest (making bookings).  
- A **Property** belongs to a host and can receive multiple bookings and reviews.  
- A **Booking** is made by a user for a property and is tied to a payment.  
- A **Review** links a user to a property with feedback.  
- A **Payment** ensures financial transactions are recorded for bookings.  



🚀 *This project is designed to help learners strengthen technical expertise, embrace teamwork, and deliver software solutions with care, clarity, and scalability.*  
