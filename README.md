# 🏡 Kribb – Real Estate Listings App

A full-stack mobile application for browsing and managing real estate listings, built using modern technologies like React Native and Expo.

## 🚀 Features

* 🔍 Search and filter properties
* ❤️ Save favorite listings
* 👤 User authentication
* ➕ Add property listings (Admin only)
* 📱 Cross-platform support (Android & iOS)

## 🛠️ Tech Stack

* **Frontend:** React Native, Expo
* **Styling:** Tailwind CSS, NativeWind
* **State Management:** Zustand
* **Backend:** Supabase (PostgreSQL)
* **Language:** TypeScript

## 📸 Screenshots

<p align="center">
  <img src="https://github.com/Nikita-Saxena391/Kribb/blob/main/WhatsApp%20Image%202026-05-01%20at%208.19.12%20PM.jpeg" width="250"/>
  <img src="https://github.com/Nikita-Saxena391/Kribb/blob/main/WhatsApp%20Image%202026-05-01%20at%208.19.10%20PM%20(2).jpeg" width="250"/>
 <img src="https://github.com/Nikita-Saxena391/Kribb/blob/main/WhatsApp%20Image%202026-05-01%20at%208.19.10%20PM%20(1).jpeg" width="250"/>
  <img src="https://github.com/Nikita-Saxena391/Kribb/blob/main/WhatsApp%20Image%202026-05-01%20at%208.19.11%20PM%20(1).jpeg" width="250"/>
  <img src="https://github.com/Nikita-Saxena391/Kribb/blob/main/WhatsApp%20Image%202026-05-01%20at%208.19.09%20PM%20(1).jpeg" width="250"/>
</p>

## 🏗️ App Architecture

How every piece of the application connects, from authentication to the UI.
```mermaid
flowchart TB

    %% Layer 1: Auth
    subgraph L1 [Layer 1: Auth Layer]
        A[Clerk @clerk/expo v3]
        A1[Sign In / Sign Up / OTP]
    end

    %% Layer 2: Data
    subgraph L2 [Layer 2: Data Layer]
        B[(Supabase DB - PostgreSQL + RLS)]
        C[Supabase Storage - Property Images]
        D[Two Clients - Clerk JWT]
    end

    %% Layer 3: State
    subgraph L3 [Layer 3: State Layer]
        E[filterStore - Zustand]
        F[userStore - Zustand]
    end

    %% Layer 4: UI
    subgraph L4 [Layer 4: UI Layer]
        G[Home]
        H[Search]
        I[Detail]
        J[Saved]
        K[Profile]
        L[Create - Admin Only]
    end

    %% Connections
    A -- "JWT Token" --> D
    D -- "Data" --> E
    D -- "Data" --> F
    E -- "State" --> G
    F -- "State" --> L

    %% Frameworks
    M[Expo SDK 54] --- L4
    N[NativeWind v4] --- L4
    O[TypeScript] --- L4
```

## ⚙️ Installation

```bash
git clone https://github.com/Nikita-Saxena391/Kribb.git
cd Kribb
npm install
npx expo start
```

## 📦 Build APK

```bash
npx expo eas build
```

## 🎯 Purpose

This project was built as a hands-on learning experience to understand full-stack mobile development, including authentication, database integration, and state management.


## 👩‍💻 Author

Nikita Saxena
