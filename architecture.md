# WanderLust Architecture Overview

## 🏗 Architecture Pattern

The application follows the MVC (Model-View-Controller) architecture.

```text
Client Request
      ↓
Routes
      ↓
Controllers
      ↓
Models (MongoDB)
      ↓
Views (EJS Templates)
```

---

# 📂 Components

## 1. Routes Layer
Handles application endpoints and API routing.

Examples:
- `/listings`
- `/login`
- `/signup`
- `/reviews`

---

## 2. Controllers Layer
Contains application business logic.

Responsibilities:
- CRUD operations
- Authentication handling
- Review management
- Error handling

---

## 3. Models Layer
MongoDB schemas using Mongoose.

Main Models:
- User
- Listing
- Review

---

## 4. Views Layer
Dynamic frontend rendering using EJS templates.

Includes:
- Navbar
- Flash Messages
- Listing Cards
- Forms

---

## ☁ External Services

### MongoDB Atlas
Used for cloud-hosted database storage.

### Cloudinary
Used for storing uploaded property images.

### Render
Used for cloud deployment.

---

## 🔐 Authentication Flow

```text
User Login
    ↓
Passport.js Authentication
    ↓
Session Creation
    ↓
Cookie Storage
    ↓
Protected Routes Access
```

---

## 📦 Deployment Workflow

```text
GitHub Repository
       ↓
Render Deployment
       ↓
MongoDB Atlas Connection
       ↓
Live Production Application
```