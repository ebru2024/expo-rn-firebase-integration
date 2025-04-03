# Expo React Native Firebase Integration

A React Native project using Expo and Firebase integration with authentication capabilities.

## 🚀 Features

- Firebase Authentication
- Expo Router for navigation
- iOS and Android support
- TypeScript support

## 📋 Prerequisites

- Node.js (v14 or higher)
- Expo CLI
- Firebase account
- Xcode (for iOS development)
- Android Studio (for Android development)

## 🛠️ Installation

1. Clone the repository:

   ```bash
   git clone <your-repo-url>
   cd expo-rn-firebase-integration
   ```

2. Install dependencies:
   ```bash
   npm install
   expo install @react-native-firebase/app @react-native-firebase/auth expo-build-properties
   ```

## ⚙️ Configuration

1. Configure `app.json` with required plugins:

   ```json
   {
     "plugins": [
       "expo-router",
       "@react-native-firebase/app",
       "@react-native-firebase/auth",
       [
         "expo-build-properties",
         {
           "ios": {
             "useFrameworks": "static"
           }
         }
       ]
     ]
   }
   ```

2. Firebase Setup:

   - Go to [Firebase Console](https://console.firebase.google.com/)
   - Create a new project or select existing one
   - Add iOS and Android apps to your Firebase project
   - Download configuration files:
     - `google-services.json` for Android
     - `GoogleService-Info.plist` for iOS
   - Place these files in the root directory of your project

3. Update `app.json` with your app configuration:
   ```json
   {
     "ios": {
       "supportsTablet": true,
       "bundleIdentifier": "your.bundle.identifier",
       "googleServicesFile": "./GoogleService-Info.plist"
     },
     "android": {
       "package": "your.package.name",
       "googleServicesFile": "./google-services.json"
     }
   }
   ```

## 🏃‍♂️ Running the App

1. Generate native code:

   ```bash
   expo prebuild
   ```

2. Run on iOS:

   ```bash
   npm run ios
   ```

3. Run on Android:
   ```bash
   npm run android
   ```

## 📝 Important Notes

- Add the following files to `.gitignore`:
  ```
  google-services.json
  GoogleService-Info.plist
  ```

## 🔒 Security

- Never commit Firebase configuration files to version control
- Keep your Firebase API keys and secrets secure
- Follow Firebase security best practices

## 📚 Additional Resources

- [Expo Documentation](https://docs.expo.dev)
- [Firebase Documentation](https://firebase.google.com/docs)
- [React Native Firebase Documentation](https://rnfirebase.io)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
