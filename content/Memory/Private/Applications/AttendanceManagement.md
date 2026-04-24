---
title: Attendance Management Backend
tags:
  - backend
  - nodejs
  - express
  - mongodb
  - api
---

# Attendance Management Backend

Express.js backend API for Emmanuel Ministries church application.

## Tech Stack
- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB with Mongoose

## Start Backend
```bash
cd C:\repo\AttendanceManagement
node src/app.js
```
Server runs on `http://localhost:5000`

## API Endpoints

### Mobile Auth
| Endpoint | Method |
|----------|--------|
| /mobile/sendOtp | POST |
| /mobile/verifyOtp | POST |
| /mobile/completeRegistration | POST |

### Attendance
| Endpoint | Method |
|----------|--------|
| /attendance/mark | POST |
| /attendance | GET |

### Vehicle
| Endpoint | Method |
|----------|--------|
| /vehicle/request | POST |
| /vehicle/return | POST |

## WhatsApp Integration
- Meta Business API
- Template: `mobile_otp`
- Language: `en_US`

## Firebase
- Service Account: `firebase-service-account.json`
- Project ID: `mobileapp-528e7`

## Status: ✅ Active