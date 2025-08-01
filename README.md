# NAP - React Native App

A React Native Android application with Google authentication using Supabase.

## Features

- Google Sign-In authentication
- Account creation functionality
- Welcome home screen
- Supabase integration

## Setup

1. **Configure Supabase:**
   - Update `src/config/supabase.js` with your Supabase URL and anon key

2. **Google Sign-In Configuration:**
   - Already configured with provided credentials
   - Package name: `com.napnetworks.app`
   - Client ID: `183050748282-5oakepmh0cvdc0riltmui6n6bcifhhac.apps.googleusercontent.com`

## Building with Codemagic

This project includes a `codemagic.yaml` configuration file for automated building.

### Steps:

1. **Connect Repository:**
   - Sign up at [codemagic.io](https://codemagic.io)
   - Connect this GitHub repository

2. **Configure Build:**
   - Codemagic will automatically detect the React Native project
   - The `codemagic.yaml` file contains the build configuration

3. **Start Build:**
   - Trigger a build from the Codemagic dashboard
   - Download the generated APK from the artifacts

## Local Development

```bash
# Install dependencies
npm install

# Run on Android
npx react-native run-android
```

## Project Structure

```
src/
├── config/
│   ├── supabase.js          # Supabase configuration
│   └── googleSignIn.js      # Google Sign-In setup
├── screens/
│   ├── AuthScreen.js        # Authentication screen
│   └── HomeScreen.js        # Home screen with welcome message
└── App.js                   # Main app component
```

## Configuration Required

Before building, make sure to:

1. **Update Supabase credentials** in `src/config/supabase.js`
2. **Verify Google Sign-In setup** in your Google Cloud Console
3. **Configure Codemagic** with any required signing certificates

## Build Output

The APK will be generated at:
`android/app/build/outputs/apk/release/app-release.apk`

