# Event-booking-cloud-demo— AWS-Ready Architecture (Demo Version)

A full-stack event booking platform built with Node.js and Express, designed to simulate a cloud-integrated flow using AWS services.  
While AWS services are not actively connected in this version, the entire backend logic, triggers, and architecture are implemented and ready for deployment.


---

## ☁️ AWS Services Simulated (Code-Ready)

| Service      | Purpose |
|--------------|---------|
| **SNS**      | Send OTP to user's phone number |
| **Lambda**   | Triggered on OTP verification and ticket generation |
| **DynamoDB** | Store OTPs and user booking details |
| **API Gateway** | Route user requests to Lambda functions |
| **S3**       | Store downloadable ticket files |

> ⚠️ All AWS logic is implemented but inactive in this demo version.  
> Code is structured for seamless future integration.

---

## 🧭 Booking Flow Overview

1. **Homepage**: User selects event type (Movie, Music, Comedy)
2. **Phone Verification**:  
   - User enters phone number  
   - `Send OTP` → triggers SNS logic (mocked)
3. **OTP Submission**:  
   - User enters OTP  
   - Lambda logic checks OTP against DynamoDB
4. **User Details Form**:  
   - Name, Email, Ticket Count  
   - On `Book`, data is stored in DynamoDB
5. **Payment Page**:  
   - User selects payment method  
   - On success, Lambda triggers ticket generation
6. **Ticket Delivery**:  
   - Ticket stored in S3 (mocked)  
   - Email sent with download link (simulated)

---

## 🧰 Tech Stack

| Layer        | Tools Used                          |
|--------------|-------------------------------------|
| Backend      | Node.js, Express.js, MongoDB (for local dev) |
| Cloud Logic  | AWS SNS, Lambda, DynamoDB, S3, API Gateway (mocked) |
| Frontend     | EJS, Bootstrap                      |
| Deployment   | Render (Live), GitHub (Codebase)    |


