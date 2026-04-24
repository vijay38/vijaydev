---
title: Emmanuel Ministries Mobile App
tags:
  - mobile
  - react-native
  - church-app
  - expo
---

# Emmanuel Ministries Mobile App

A complete mobile application for Emmanuel Ministries church believers.

## Tech Stack
- **Framework**: React Native with React Native CLI
- **Language**: TypeScript
- **Navigation**: React Navigation (Bottom Tabs)
- **Storage**: AsyncStorage

## Features
- WhatsApp OTP Login
- Attendance Tracking (Personal + Family)
- YouTube Sermon Videos
- Push Notifications (Firebase)
- Parking Vehicle Request
- Online Offerings
- Church Locations
- Profile with Family Linking

## Build Commands
```bash
# Development
npx react-native start
npx react-native run-android

# Build APK
npx react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res
cd android && gradlew.bat assembleDebug
```

## API Endpoints
Base: `http://192.168.0.192:5000/api`

| Endpoint | Method | Description |
|----------|--------|------------|
| /mobile/sendOtp | POST | Send OTP |
| /mobile/verifyOtp | POST | Verify OTP |
| /mobile/attendance | GET | Get Attendance |
| /mobile/vehicle | GET/POST | Vehicle Status |

## Status: ✅ Active