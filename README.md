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
graph TD
    subgraph L1 [Layer 1: Auth Layer]
        Clerk["Clerk Auth (Expo v3)"]
    end

    subgraph L2 [Layer 2: Data Layer]
        DB[(Supabase DB)]
        Storage[Supabase Storage]
    end

    subgraph L3 [Layer 3: State Layer]
        Zustand[Zustand Stores]
    end

    subgraph L4 [Layer 4: UI Layer]
        Screens[Expo Router Screens]
    end

    Clerk --> L2
    L2 --> L3
    L3 --> L4
    
    style L1 fill:#f96,stroke:#333
    style L2 fill:#6f9,stroke:#333
    style L3 fill:#96f,stroke:#333
    style L4 fill:#6cf,stroke:#333

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
