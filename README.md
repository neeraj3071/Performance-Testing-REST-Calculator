# Performance Testing of REST Calculator

## Overview
This repository contains JMeter test cases for performance testing of a simple calculator REST API built with Java 11 and Spring Boot. The test cases are designed to evaluate the API's response under load and verify its correctness.

## Requirements
- Java 11 JDK ([Download Here](https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html))
- Apache JMeter ([Download Here](https://jmeter.apache.org/download_jmeter.cgi))
- Maven (included in the provided project)

## Running the REST Application
1. Extract the provided `rest-calculator.zip` file.
2. Navigate to the project directory in the terminal.
3. Run the following command based on your OS:
   - **Linux/macOS:** `./mvnw spring-boot:run`
   - **Windows:** `mvnw spring-boot:run`
4. The application will start and can be accessed at:
   - Base URL: `http://localhost:8080/calculator`
   - API Documentation: `http://localhost:8080/calculator/swagger-ui.html`

## Performance Testing with JMeter
### Test Plan Setup
Each test case includes the following components:
- **Thread Group:** Simulating a minimum of 100 users with a maximum ramp-up time of 5 seconds.
- **Samplers:** HTTP requests to test API endpoints.
- **Listeners:** Capturing performance metrics.
- **Assertions:** Validating API response correctness.

### Running JMeter Test Cases
1. Open Apache JMeter.
2. Load the provided `.jmx` test plan file.
3. Configure the server IP and port if necessary.
4. Click **Start** to execute the performance test.
5. Analyze results using the built-in JMeter listeners.

## Repository Structure
```
📦 Performance-Testing-REST-Calculator
 ┣ 📂 jmeter-test-cases    # JMeter .jmx files
 ┣ 📂 rest-calculator      # Extracted REST API project
 ┣ 📜 README.md           # Project documentation
 ┗ 📜 .gitignore          # Git ignore rules
```

## License
This project is for educational purposes only. Feel free to modify and extend as needed.
