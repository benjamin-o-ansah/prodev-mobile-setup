# Expo Go Setup Documentation

## Overview

This document records the steps followed to install and configure **Expo Go** for React Native development, along with any challenges encountered during setup.

## Installation Steps

1. **Access Expo Go Homepage**
   Navigated to the official Expo Go page: [https://expo.dev/go](https://expo.dev/go).

2. **Select SDK Version**
   Reviewed the available SDKs and confirmed the latest stable SDK version recommended by Expo.

3. **Install Expo Go**

   * **Android**: Opened the Google Play Store and installed *Expo Go*.
   * **iOS**: Opened the Apple App Store and installed *Expo Go*.

4. **Launch the Application**
   Opened the Expo Go app after installation completed successfully.

5. **Account Setup**
   Logged in using an existing Expo account. (Alternatively, a new account can be created directly within the app.)

## Verification

* Confirmed successful login.
* Verified that the app can scan QR codes and connect to Expo development servers.

## Challenges Encountered

* **Network Restrictions**: Initial difficulty connecting to the development server due to firewall or network configuration. Resolved by switching to a stable Wi-Fi connection.
* **SDK Compatibility Awareness**: Ensured that the local Expo CLI version matched the SDK version supported by Expo Go.

## Project Scaffolding Steps

1. **Initialize Expo Project**
   Executed the following command in the project root to scaffold a new Expo application using the latest Expo Router template:

   ```bash
   npx create-expo-app@latest .
   ```

2. **Select Template**
   Chose the **Expo Router** template when prompted. This generated a project structure with routing support under the `app/` directory.

3. **Modify Home Screen**

   * Opened `app/(tabs)/index.tsx`.
   * Located the default text **Welcome!**.
   * Updated the text to **First App Created**.

4. **Run the Application**
   Started the Expo development server using:

   ```bash
   npx expo start
   ```

5. **Test on Physical Device**

   * **iOS**: Scanned the QR code using the device Camera app.
   * **Android**: Scanned the QR code using the Expo Go app.

## Reset Project Command Observations

Executed the reset command:

```bash
npm run reset-project
```

### Observed Effects

* The command removed generated and cached files created during development.
* Application state, temporary build artifacts, and development caches were cleared.
* The project was returned to a clean state similar to a freshly scaffolded setup, while core source files remained intact.
* On the next start, the Expo development server rebuilt the project from scratch.

## Conclusion

The Expo project was successfully scaffolded using the latest Expo Router template. The home screen modification rendered correctly across devices, and the `reset-project` command effectively restored the project to a clean baseline suitable for troubleshooting or fresh development.
