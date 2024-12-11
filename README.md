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
```sh
mvn clean install
```
3.**Run the application**:  
```sh
mvn spring-boot:run
```
## Usage Instructions

- How to Configure and Start the System

1.**Configuration**:  

- Ensure the config.json file is present in the src/main/resources directory with the necessary configuration parameters (e.g., ticket release rate, customer retrieval rate, total tickets, max ticket capacity).
- Ticket Release Rate: Frequency of ticket availability.
- Customer Retrieval Rate: Speed of customer processing.
- Total Tickets: Number of total  tickets added by a vendor.
- Max Ticket Capacity: Maximum number of tickets allowed in the system at once.

2.**Start the System**:  

- Start the Spring Boot application as described in the setup instructions.

### Explanation of UI Controls

#### WebSocket Endpoint:  
- Connect to the WebSocket endpoint using a client like Postman.

URL: ws://localhost:8080/gettickets

#### Messages:  
- Send a message to get the current ticket status:
```sh
/gettickets
```
- Send a message to close the connection:
```sh
close
```
### Postman Configuration:

- Open Postman and create a new WebSocket request.
- Enter the WebSocket URL and connect.
- Use the message field to send commands and view responses in the messages section.
