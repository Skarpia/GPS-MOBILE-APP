# GPS-MOBILE-APP
This is a GPS attendance monitoring class app
# GPS-Based Student Attendance System

A secure mobile application that ensures students can only mark attendance when physically present within a designated classroom location, preventing proxy or fraudulent sign-ins.

## Technology Stack

### Frontend (Mobile App)
- **Flutter** - Cross-platform development (Android/iOS)
- **Dart** - Programming language
- **Provider** - State management
- **Geolocator** - GPS location services
- **Local Auth** - Biometric authentication
- **Camera** - Selfie capture for verification

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **JWT** - Authentication tokens
- **bcrypt** - Password encryption
- **Socket.io** - Real-time notifications

### Key Features
- GPS geofencing for location verification
- Secure authentication with biometrics
- Anti-proxy mechanisms
- Real-time attendance tracking
- Comprehensive reporting and analytics
- Push notifications

## Project Structure

```
class-attendance-app/
|-- backend/                 # Node.js API server
|   |-- src/
|   |   |-- controllers/     # Route controllers
|   |   |-- middleware/      # Express middleware
|   |   |-- models/          # Database models
|   |   |-- routes/          # API routes
|   |   |-- services/        # Business logic
|   |   |-- utils/           # Helper functions
|   |   |-- config/          # Configuration files
|   |   |-- app.js           # Express app setup
|   |   |-- server.js        # Server entry point
|   |-- package.json
|   |-- .env
|
|-- frontend/                # Flutter mobile app
|   |-- lib/
|   |   |-- screens/         # UI screens
|   |   |-- widgets/         # Reusable widgets
|   |   |-- services/        # API services
|   |   |-- models/          # Data models
|   |   |-- utils/           # Helper utilities
|   |   |-- main.dart        # App entry point
|   |-- pubspec.yaml
|   |-- android/
|   |-- ios/
|
|-- docs/                    # Documentation
|-- README.md
```

## Getting Started

### Prerequisites
- Flutter SDK
- Node.js
- MongoDB
- Android Studio / Xcode

### Installation
1. Clone the repository
2. Set up the backend:
   ```bash
   cd backend
   npm install
   npm run dev
   ```
3. Set up the Flutter app:
   ```bash
   cd frontend
   flutter pub get
   flutter run
   ```

## Security Features
- GPS spoofing detection
- Device integrity checks
- Biometric authentication
- JWT token management
- HTTPS encryption
- Rate limiting

## API Endpoints
- `POST /api/auth/login` - User authentication
- `POST /api/attendance/mark` - Mark attendance
- `GET /api/attendance/reports` - Get attendance reports
- `GET /api/classes` - Get class information
- `POST /api/location/verify` - Verify GPS location

## Database Schema
- **Students**: ID, name, email, device info, biometric data
- **Classes**: Class ID, location coordinates, schedule
- **Attendance**: Student ID, class ID, timestamp, GPS coordinates
- **Reports**: Aggregated attendance data and analytics
