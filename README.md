# Slack User Status Update via Postman

This repository provides a step-by-step guide and Postman collection for updating Slack user status profiles using the Slack API.

It is designed for IT admins, support teams, and managers who need to update user statuses (e.g., maternity leave, PTO, sick leave) in a consistent and automated way.

---

## 🚀 Key Features

* 🔐 Slack API setup with required scopes
* ⚙️ Postman configuration for quick testing
* 🧪 Sample request payloads
* 📘 Clear documentation and best practices
* 🔑 Secure token handling guidance

---

## 📌 Example Use Case

Update a user’s Slack status to:

> **“Jessica on maternity leave until Aug 1” 🌴**

---

## 🚀 Quick Start

1. Create a Slack App
   👉 https://api.slack.com/apps

2. Add OAuth Scopes:

   * `users.profile:write`

3. Install the app to your workspace

4. Copy your **User OAuth Token (xoxp)**

5. Open Postman and configure:

   * **Method:** POST
   * **URL:** https://slack.com/api/users.profile.set

6. Add Headers:

   ```
   Authorization: Bearer xoxp-your-token
   Content-Type: application/json
   ```

7. Use the request body below and click **Send**

---

## 📡 API Request Example

### Endpoint

```
POST https://slack.com/api/users.profile.set
```

### Headers

```
Authorization: Bearer xoxp-your-token
Content-Type: application/json
```

### Body

```json
{
  "user": "U12345678",
  "profile": {
    "status_text": "Jessica on maternity leave until Aug 1",
    "status_emoji": ":palm_tree:",
    "status_expiration": 0
  }
}
```

---

## 📁 Project Structure

```
Slack-User-Status-Update-via-Postman/
│
├── README.md
├── LICENSE
│
├── docs/
│   └── slack-status-update-guide.md
│
├── postman/
│   └── collection.json
│
└── examples/
    └── sample-request.json
```
