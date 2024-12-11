# Ticketing System

## Introduction
The Ticketing System is a Java-based application that simulates a ticket vending and purchasing system using WebSockets. Vendors release tickets at a specified rate, and consumers purchase tickets at a specified rate. The system uses Spring Boot for the backend and can be tested using Postman or any WebSocket client.

## Setup Instructions

### Prerequisites
- Java 17 or higher
- Maven 3.6 or higher

### How to Build and Run the Application
1. **Clone the repository**:
   ```sh
   git clone https://github.com/sasindri-siriwardene/TicketingPlatform-Java.git
   cd TicketingPlatform-Java
   ```
2.**Build the application**:
mvn clean install
Run the application:  
mvn spring-boot:run
Usage Instructions
How to Configure and Start the System
Configuration:  
Ensure the config.json file is present in the src/main/resources directory with the necessary configuration parameters (e.g., ticket release rate, customer retrieval rate, total tickets, max ticket capacity).
Start the System:  
Start the Spring Boot application as described in the setup instructions.
Explanation of UI Controls
WebSocket Endpoint:  
Connect to the WebSocket endpoint using a client like Postman.
URL: ws://localhost:8080/gettickets
Messages:  
Send a message to get the current ticket status:
/gettickets
Send a message to close the connection:
close
Postman Configuration:
Open Postman and create a new WebSocket request.
Enter the WebSocket URL and connect.
Use the message field to send commands and view responses in the messages section.
