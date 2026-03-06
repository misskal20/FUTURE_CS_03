DummyJSON API Security Risk Analysis
#Overview

This repository contains the API Security Risk Analysis report conducted as part of the Future Interns cybersecurity task. The goal of this project was to analyze the security posture of the DummyJSON API by testing multiple endpoints, inspecting HTTP responses, and identifying potential security risks.

The analysis demonstrates practical API testing techniques commonly used in cybersecurity and penetration testing.

#Objectives

The main objectives of this task were:

Test various API endpoints and observe responses.

Analyze HTTP status codes and response structures.

Inspect response headers for security configurations.

Identify potential security risks.

Provide recommendations to improve API security.

API Used

The API analyzed in this project is DummyJSON, a public mock API designed for developers to practice working with APIs and testing applications.

API base URL:

https://dummyjson.com
Tools Used

Insomnia – For sending and testing API requests

Browser Developer Tools – For inspecting headers and responses

Git & GitHub – For version control and project documentation

Endpoints Tested

Some of the API endpoints analyzed include:

#Endpoint	Method	Description
/products	GET	Retrieves list of products
/products/1	GET	Retrieves a specific product
/products/99999	GET	Tests response for non-existent product
/users	GET	Retrieves list of users
/auth/login	POST	Tests authentication functionality
/carts	GET	Retrieves cart data
#Key Findings

The API returns correct HTTP status codes such as 200 for successful requests and 404 for invalid resources.

Most endpoints are publicly accessible, which is expected since the API is designed for testing purposes.

Responses follow a consistent JSON format, which is good for developers consuming the API.

Some security headers could be improved to better simulate production-level security.

#Security Risks Identified
Risk	Severity	Description
Public access to user data	Medium	Some endpoints expose user data without authentication
No rate limiting	Medium	Could allow abuse or automated attacks
Missing security headers	Low	Security headers such as HSTS could improve protection
#Recommendations

Implement authentication for sensitive endpoints.

Introduce rate limiting to prevent brute-force attacks.

Add important security headers like HSTS and CSP.

Improve input validation for user-provided data.

Monitor and log API requests for suspicious activity.


#Disclaimer

This project analyzes the DummyJSON API strictly for educational purposes.
DummyJSON is a public mock API designed for testing and learning, and it is not intended for production environments. No malicious activity or exploitation was performed during this analysis.
