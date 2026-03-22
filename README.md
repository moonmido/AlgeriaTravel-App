# 🇩🇿 DzTravel — Algeria Travel App

A mobile travel guide application for exploring Algeria, built with **React Native (Expo)** and powered by **Firebase**. Discover destinations, plan trips, and explore the beauty of Algeria right from your phone.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
  - [1. Clone the Repository](#1-clone-the-repository)
  - [2. Install Dependencies](#2-install-dependencies)
  - [3. Configure Firebase](#3-configure-firebase)
  - [4. Run the App](#4-run-the-app)
- [Project Structure](#project-structure)
- [Firebase Setup](#firebase-setup)
- [Build & Deployment](#build--deployment)
- [Contributing](#contributing)
- [License](#license)

---

## 🧾 Overview

**DzTravel** is a cross-platform mobile app (Android & iOS) that helps users discover and explore travel destinations across Algeria. It features a clean, intuitive UI with smooth navigation, tabbed browsing, and real-time data powered by Firebase.

---

## ✨ Features

- 🗺️ Browse Algerian travel destinations and attractions
- 🔥 Real-time data powered by Firebase Firestore
- 🔐 User authentication (Firebase Auth)
- 📱 Cross-platform: Android & iOS support
- 🗂️ Tab-based navigation for easy browsing
- 📄 Paginated views for destination listings
- 💾 Offline data persistence with AsyncStorage
- ✅ Interactive checkbox selections (e.g., trip checklists)

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **React Native 0.74** | Core mobile framework |
| **Expo ~51** | Development toolchain & build system |
| **Firebase 10** | Backend (Auth + Firestore database) |
| **React Navigation 6** | Screen navigation (Stack + Native Stack) |
| **React Native Tab View** | Tabbed UI components |
| **React Native Pager View** | Swipeable page views |
| **AsyncStorage** | Local data persistence |
| **Expo EAS** | Cloud builds & deployment |

---

## ✅ Prerequisites

Make sure you have the following installed:

- **Node.js 18+**
- **npm** or **yarn**
- **Expo CLI**
  ```bash
  npm install -g expo-cli
  ```
- **Expo Go** app on your Android/iOS device (for testing)
- A **Firebase** project (see [Firebase Setup](#firebase-setup))

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/moonmido/AlgeriaTravel-App.git
cd AlgeriaTravel-App
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Firebase

Create your Firebase project and add your config to the `firebase/` folder. See [Firebase Setup](#firebase-setup) for details.

### 4. Run the App

```bash
# Start the Expo development server
npm start

# Run on Android
npm run android

# Run on iOS
npm run ios

# Run on Web (experimental)
npm run web
```

Scan the QR code with the **Expo Go** app on your phone to preview the app instantly.

---

## 📁 Project Structure

```
AlgeriaTravel-App/
│
├── Screens/                  # All app screens (React Native components)
│   ├── HomeScreen.js         # Main landing/home screen
│   ├── DestinationScreen.js  # Destination detail view
│   └── ...                   # Other screens
│
├── assets/                   # Images, icons, splash screen
│   ├── icon.png
│   ├── splash.png
│   ├── adaptive-icon.png
│   └── favicon.png
│
├── firebase/                 # Firebase configuration & utilities
│   └── firebaseConfig.js     # Firebase app initialization
│
├── App.js                    # Root component & navigation setup
├── app.json                  # Expo app configuration
├── eas.json                  # EAS build configuration
├── babel.config.js           # Babel configuration
├── package.json              # Dependencies & scripts
└── .gitignore
```

---

## 🔥 Firebase Setup

1. Go to [Firebase Console](https://console.firebase.google.com/) and create a new project.
2. Enable **Authentication** (Email/Password or preferred provider).
3. Enable **Firestore Database** and create your collections.
4. Copy your Firebase config and create `firebase/firebaseConfig.js`:

```js
import { initializeApp } from "firebase/app";
import { getAuth } from "firebase/auth";
import { getFirestore } from "firebase/firestore";

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID",
};

const app = initializeApp(firebaseConfig);
export const auth = getAuth(app);
export const db = getFirestore(app);
```

> ⚠️ Never commit your Firebase API keys to version control. Use environment variables or `.env` files.

---

## 📦 Build & Deployment

This project uses **Expo EAS** (Expo Application Services) for cloud builds.

### Build for Android

```bash
eas build --platform android
```

### Build for iOS

```bash
eas build --platform ios
```

### Build for Both

```bash
eas build --platform all
```

> Make sure you have an [Expo account](https://expo.dev/) and are logged in via `eas login`.

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push and open a Pull Request

---

## 📄 License

This project is open-source. Feel free to use, modify, and distribute it.

---

## 👤 Author

**Boutmedjet Abd elmoudjib (moonmido)**
- GitHub: [@moonmido](https://github.com/moonmido)

---

> ⭐ If you like this project, give it a star on GitHub!
