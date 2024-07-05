Blog Content Backend Application

## Project Overview
This project is a Spring Boot application for managing blog content for our client's engineering blog.
It provides APIs for listing, creating, updating, and deleting blog posts.

## Features
- List all blog contents
- Get individual blog content
- Post, update, and delete blog content (authentication required)
- Admin approval for blog content from non-employees



### Prerequisites
- Java 11
- Maven 3.6+
- MySQL
- Docker (for deployment)


1. **Clone the repository:**
   ```bash
  
Navigate to the project directory:
bash
Copy code
cd repo
Install dependencies:
bash
Copy code
mvn install
Run the application:
bash
Copy code
mvn spring-boot:run
Configuration
Update application.properties with your MySQL database credentials:

properties
Copy code
spring.datasource.url=jdbc:mysql://localhost:3306/mydb
spring.datasource.username=root
spring.datasource.password=secret
Usage
API Endpoints
SERVER PORT:8085
Public Endpoints
GET /api/v2/unsecure: List all blog contents
GET /api/v2/unsecure/{id}: Get individual blog content
Authenticated Endpoints
POST /api/v1/blogs: Create a new blog post
PUT /api/v1/blogs/{id}: Update an existing blog post
DELETE /api/v1/blogs/{id}: Delete a blog post

SCALING STRATEGIES
Horizontal Scaling: Add more EC2 instances to handle increased traffic.
Vertical Scaling: Increase the size of EC2 instances to provide more compute power.
Database Read Replicas: Use read replicas to offload read operations from the primary database.
Caching: Implement caching with Redis or









