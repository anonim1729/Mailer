# Email Sending API using Node.js and Nodemailer

## Overview
This is a simple Node.js application that provides an API endpoint to send emails using Gmail's SMTP server.

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```
2. Install dependencies:
   ```sh
   npm install
   ```

## Configuration
1. Enable **Two-Step Verification** on your Gmail account.
2. Generate an **App Password** in Google Account settings.
3. Replace the credentials in the `auth` object inside `nodemailer.createTransport`:
   ```javascript
   auth: {
       user: "your-email@gmail.com", 
       pass: "your-app-password"
   }
   ```

## Running the Server
```sh
node server.js
```

## API Usage
**Endpoint:**
```http
POST /send-email
```
**Request Body (JSON):**
```json
{
    "to": "recipient@example.com",
    "subject": "Test Email",
    "text": "Hello, this is a test email."
}
```

**Response:**
- Success: `{ "message": "Email sent successfully!" }`
- Error: `{ "error": "Failed to send email" }`

## Technologies Used
- Node.js
- Express.js
- Nodemailer

