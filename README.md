# AttendanceTracker Pro

A secure and efficient attendance tracking application that utilizes biometric authentication for accurate time tracking. The app features a clean loading screen, secure authentication with face recognition or password, and a comprehensive home dashboard for attendance management.

## Style Guide

### Theme and Color Scheme
- **Primary Color**: #2C3E50 (Dark Blue)
- **Secondary Color**: #34495E (Slate Blue)
- **Accent Color**: #3498DB (Bright Blue)
- **Background**: #ECF0F1 (Light Gray)
- **Surface**: #FFFFFF (White)
- **Text**: #2C3E50 (Dark Blue)
- **Text Secondary**: #7F8C8D (Gray)

### Visual Design
- **Border Radius**: rounded-xl for components
- **Padding**: p-4 for content spacing
- **Margin**: m-3 for element separation
- **Style**: Professional and trustworthy
- **Mood**: Reliable and secure
- **Visual Weight**: Medium

## Features

1. **Loading Screen**
   - Animated loading indicator
   - App branding and initialization
   - Automatic transition after 3 seconds

2. **Authentication Screen**
   - Registration for new users
   - Login with email/password
   - Face authentication option
   - Security lockout after 5 failed attempts
   - Progressive timeout (30 seconds then 1 minute)

3. **Home Screen**
   - Real-time clock display
   - Attendance tracking dashboard
   - Check-in/check-out functionality
   - Recent activity log
   - Secure logout

## Technologies Used

- React Native
- NativeWind (Tailwind CSS for React Native)
- Lucide Icons
- React Native Core Components

## Installation Instructions

1. Install dependencies:
   ```bash
   npm install
   ```

2. Install NativeWind and Tailwind CSS:
   ```bash
   npm install nativewind
   npm install -D tailwindcss
   ```

3. Create a `tailwind.config.js` file:
   ```js
   module.exports = {
     content: ["./app/**/*.{js,jsx,ts,tsx}", "./components/**/*.{js,jsx,ts,tsx}"],
     theme: {
       extend: {},
     },
     plugins: [],
   }
   ```

4. Add the following to your `babel.config.js`:
   ```js
   module.exports = function(api) {
     api.cache(true);
     return {
       presets: ['babel-preset-expo'],
       plugins: ["nativewind/babel"],
     };
   };
   ```

## Usage Instructions

The app automatically starts with the loading screen, which transitions to the authentication screen after 3 seconds. New users can register with their details, while existing users can log in using either password or face authentication. After 5 failed attempts, the user will be locked out for 30 seconds, then 1 minute for subsequent failures.

The home screen displays the current date/time, today's attendance status, and recent activity history. Users can check in/out and view their attendance records.
```