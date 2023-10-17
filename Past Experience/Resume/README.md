# Resume

### E-Bridge

* Java, Spring Boot, REST API, Microservices, MyBatis, MySQL, MongoDB, Git, Docker, Maven, AWS Cognito

1. Developed and maintained a SaaS platform for merchants to design and publish their own e-vouchers and e-coupons
2. Integrated Nacos into the system for service discovery and OpenFeign for HTTP requests between services
3. Set up Amazon Cognito user pool for user registration and authentication, wrote APIs to manage Cognito user attributes
4. Greatly improved system's query performance by caching data into Redis
5. Undertook the DevOps work by deploying microservices into Amazon EC2 through Docker

### OTT Pocket

* Java, Spring Boot, REST API, JPA, Hibernate, MySQL, Git, Maven

1. Developed and maintained OTT Pocket, a B2C platform that sells e-gift cards and e-vouchers
2. Largely protected the platform from money laundering by verifying customer's identity (KYC) with Trulioo
3. Enabled credit card payments by integrating Authorize.Net (a payment gateway that is able to connect to Chase Payment Solutions) into the system
4. Developed services to send push notifications into clients' phones using OneSignal
5. Applied design pattern (factory method) to process cards from different providers (e.g. Esso, InComm, Oxford etc.), including creating new cards, getting balance, getting transaction history etc.

### Yonyou

* Java, Spring Boot, REST API, MyBatis, Oracle, Git, Maven, Tomcat

1. Developed ERP systems for several companies, fixed issues reported by clients
2. Collaborated with product manager to analyze and design new features
3. Undertook the DevOps work by deploying projects into Tomcat

### Research Assistant

* Java, Spring Boot, REST API, JPA, Hibernate, MySQL, Git, Maven, Java Mail Library, WebSocket

1. Built a ridesharing back-end system from scratch, implemented user-related features like user registration, email verification, profile modification etc. 
2. Enabled authentication and authorization by integrating Spring Security into the system
3. Utilized Java Mail Library for sending verification code to users
4. Applied WebSocket to fetch vehicle's real-time GPS from MongoDB at regular intervals

### Cyber Black Friday

* Java, Spring Boot, MyBatis, MySQL, Redis, Lua, JavaScript

1. Emulated the scene that thousands of people buy the same product at the same time on Cyber Black Friday, developed two methods (pessimistic locking and Redis) to prevent a mock shopping system from generating excess orders
2. Sent a large number of XMLHttpRequests in a short time to create an explosion of orders
3. Proved that the Redis method is much more efficient, costing only 16 seconds to generate 20,000 orders while the other method had to spend several minutes
