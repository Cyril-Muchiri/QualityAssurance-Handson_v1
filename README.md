# Automated Test Scripts for Booking Update API

This repository contains automated test scripts written in Postman for testing the [Booking Update API endpoint](https://restful-booker.herokuapp.com/apidoc/index.html#api-Booking-UpdateBooking).

## Setup

1. Ensure you have Postman installed on your machine. If not, download and install it from [Postman's official website](https://www.postman.com/downloads/).
2. Clone this repository to your local machine.

## Execution

1. Open Postman.
2. Import the collection `BookingUpdateAPITests.postman_collection.json` located in the `root` directory.
3. Set up all the environment variables in Postman.
4. Run the collection. All test cases will be executed automatically.

# Test Scenarios

### Valid Update
**Description**: Existing booking with valid ID.  
**Steps**:
1. Send a PUT request to update an existing booking with valid data.
2. Check if the booking details are successfully updated as per the provided data.

### Invalid Update - Invalid Booking ID
**Description**: Attempt to update a booking with an invalid ID.  
**Steps**:
1. Send a PUT request to update a booking with an invalid ID.
2. Verify that the response indicates an error due to an invalid booking ID.

### Invalid Update - Invalid Data
**Description**: Attempt to update a booking with invalid data.  
**Steps**:
1. Send a PUT request to update an existing booking with invalid data.
2. Verify that the response indicates an error due to invalid data provided.

### Unauthorized Update
**Description**: Attempt to update a booking without proper authorization.  
**Steps**:
1. Send a PUT request to update an existing booking without providing proper authorization.
2. Verify that the response indicates an unauthorized access error.

### Error Handling - Server Timeout
**Description**: Simulate a server timeout during the update process.  
**Steps**:
1. Send a PUT request to update an existing booking.
2. Simulate a server timeout.
3. Verify that the response indicates a server error due to a timeout.

### Update with Missing Fields
**Description**: Attempt to update a booking with missing fields.  
**Steps**:
1. Send a PUT request to update an existing booking with missing fields.
2. Verify that the response indicates an error due to missing fields.

### Update with Invalid Data
**Description**: Attempt to update a booking with invalid data.  
**Steps**:
1. Send a PUT request to update an existing booking with invalid data.
2. Verify that the response indicates an error due to invalid data provided.

### Update with Expired Session
**Description**: Attempt to update a booking with an expired session token.  
**Steps**:
1. Send a PUT request to update an existing booking with an expired session token.
2. Verify that the response indicates a session expired error.

### Duplicate Booking Update
**Description**: Attempt to update a booking with the same data as an existing booking.  
**Steps**:
1. Send a PUT request to update an existing booking with the same data as another booking.
2. Verify that the response indicates a conflict error due to duplicate data.

### Update with Large Data Payload
**Description**: Attempt to update a booking with a large data payload.  
**Steps**:
1. Send a PUT request to update an existing booking with a large data payload.
2. Verify that the response indicates an error due to exceeding payload size limits.

### Update Conflict
**Description**: Simulate a conflict during the update process.  
**Steps**:
1. Send a PUT request to update an existing booking.
2. Simulate a conflict with the dummy data provided in the export.
3. Verify that the response indicates a conflict error.

