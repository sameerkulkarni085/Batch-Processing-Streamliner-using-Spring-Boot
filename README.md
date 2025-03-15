# Spring Boot Batch Processing Using Multithreading

## Introduction

This Spring Boot application streamlines batch processing for retail by efficiently applying discounts to product IDs based on specific criteria, updating product details in the database, and publishing changes to a Kafka topic for real-time event handling.

## Project Description

In e-commerce and retail, dynamically adjusting product prices to reflect promotions, seasonal discounts, or stock availability is a frequent requirement. However, this process becomes challenging and resource-intensive when dealing with vast numbers of products. Manually updating prices increases the risk of errors and inconsistencies across platforms. This application addresses the complexity by automating the discount application process. It ensures that discounts are applied efficiently based on predefined criteria, updates the pricing information directly in the product database, and synchronizes changes across all connected systems. This automation guarantees accurate, real-time price adjustments, maintaining consistency across platforms while significantly reducing manual effort and errors.

### Use Case
Imagine a grocery delivery service preparing for a festive season sale. They plan to offer a 15% discount on all perishable goods like fruits and vegetables that expire within three days and a 10% discount on products expiring within a week. Managing these discounts manually for hundreds of thousands of items could result in errors and delayed updates.

This application automates the process by receiving a list of product IDs, checking the expiration dates of each item, applying the appropriate discount, updating the prices in the database, and publishing the changes to a Kafka topic. This ensures that all downstream systems, including the e-commerce website and mobile app, reflect the price updates in real time, ensuring accurate and seamless discounts for customers during peak sale periods.

### Process Behind
The application uses three methods to handle batch updates:  
1. **Streams**: Processes product IDs one by one in a sequential manner.  
2. **Parallel Streams**: Uses multiple processor cores to speed up processing.  
3. **CompletableFuture**: Splits product IDs into batches and processes them in parallel threads, ideal for handling tasks with heavy I/O operations.


### Objective
The main objective of this project is to showcase the application of various Java concurrency models to real-world batch processing scenarios in a Spring Boot application. It serves as a practical demonstration of leveraging modern Java features to enhance the performance and scalability of backend systems in retail and e-commerce.

## Technologies used
- Java Spring Boot 3 
- Kafka  
- MySQL  
- Spring Data JPA  
- Spring Kafka 

## Dependencies

- **`Spring Boot Starter Actuator`**: Facilitates application monitoring and management.  
- **`Spring Boot Starter Data JPA`**: Simplifies interaction with databases using Spring Data JPA repositories.  
- **`Spring Boot Starter Web`**: Offers the necessary setup for developing web applications with ease.  
- **`Spring Kafka`**: Provides tools to enable seamless communication with Kafka brokers.  
- **`MySQL Connector Java`**: Ensures connectivity between the application and a MySQL database.  
- **`Lombok`**: Reduces boilerplate code by auto-generating common methods like getters, setters, and constructors.  
- **`Spring Boot Starter Test & Spring Kafka Test`**: Includes tools for effectively testing Spring Boot applications, including Kafka integration tests.  
