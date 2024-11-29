# Hotel Reservation System

A simple console-based **Hotel Reservation System** built in **Java** using **JDBC** for database connectivity and **MySQL** as the backend database. The system allows users to reserve rooms, view and update reservations, retrieve room numbers, and delete reservations.

## Features

- **Reserve a Room**: Allows users to book a room by entering their name, room number, and contact details.
- **View Reservations**: Displays all current reservations with relevant details.
- **Get Room Number**: Retrieves the room number based on the reservation ID and guest name.
- **Update Reservation**: Enables users to update guest details for an existing reservation.
- **Delete Reservation**: Allows users to delete a reservation based on its ID.
- **Exit System**: Gracefully exits the application.

## Technologies Used

- **Java**: Core logic implementation
- **JDBC**: Database connectivity
- **MySQL**: Database management system
- **Scanner**: Input handling

## Prerequisites

- **Java 8** or higher
- **MySQL Server**
- **MySQL JDBC Driver** (included in the project)

## Database Setup

1. Create the `reservations` table:

   ```sql
   CREATE TABLE reservations (
       reservation_id INT PRIMARY KEY AUTO_INCREMENT,
       guest_name VARCHAR(50),
       room_number INT,
       contact_number VARCHAR(15),
       reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );
 2. Update the database credentials in the code:

    ```sql
    private static final String url = "your_database_url";
    private static final String username = "your_username";
    private static final String password = "your_password";

