---
title: Emmanuel Parking Tracker
tags:
  - nextjs
  - parking
  - admin-dashboard
---

# Emmanuel Ministries - Parking Tracker

An internal Next.js application for managing church parking services and driver operations.

## 🎯 Purpose
Internal tool for church parking team to manage:
- Vehicle requests from church members
- Driver assignments
- Parking logs tracking

## 🔧 Features

### For Drivers
- Driver login and authentication
- View assigned vehicles
- Accept/reject parking requests
- Update vehicle delivery status
- Activity logs

### Admin Functions
- Add/manage vehicles
- Assign drivers to vehicles  
- View all parking requests
- Track delivery status
- View activity logs

## 📱 WhatsApp Integration
WhatsApp-powered parking service: message **Hi** to **+91 9440137776**

Members can:
1. Send "Hi" to get parking menu
2. Request vehicle
3. Request pickup location
4. Get delivery confirmation

### WhatsApp Message Flow
1. User sends "Hi"
2. System shows options:
   - 🅿️ Request Vehicle
   - 📍 My Location
   - ℹ️ Info
3. User selects option
4. System processes and notifies driver
5. Driver delivers and sends confirmation

## 🛠 Technical Details
- **Framework**: Next.js 16
- **Language**: TypeScript  
- **UI**: Radix UI + Tailwind
- **Database**: MongoDB via AttendanceManagement API
- **WhatsApp**: Meta Business API

## 👨‍💻 Developer
**Vijay** - Full Stack Developer

Created this internal parking management system with WhatsApp integration for seamless vehicle coordination.

## Note
This is an **internal application** - not for general church members. Only authorized parking team members and drivers should access it.

---
*Building internal solutions for church operations!*