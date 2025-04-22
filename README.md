[![Powered by Firebase](https://img.shields.io/badge/Backend-Firebase-FFCA28?logo=firebase&logoColor=white&style=for-the-badge)](https://firebase.google.com/)

# SeneMarket App Backend
This repository contains the backend documentation. Both mobile app developed in Flutter and Kotlin use this repository.

SeneMarket application uses _Firebase_ as a Backend-as-a-Service (BaaS) to manage:

- User authentication
- Real-time database
- File storage


All backend services are managed from the Firebase console.

##  Firebase Services Used

| Service | Description |
| - | - |
| Firebase Authentication	| User management: registration and login with email authentication. |
| Cloud Firestore	| Real-time NoSQL database for storing users, products, favorites and session activities. |
| Firebase Cloud Storage | Secure storage of product images. |

## General Structure of Firestore

The application uses the following example of collection structure:

- `/users/{userId}`
  - `name`: string
  - `email`: string
  - `career`: string
  - `semester`: number
  - `notificationsEnabled`: bool
  - `favorites`: array of strings
  - `fcmToken`: string
  - `createdAt`: timestamp
  - `categoryClicks`: map

- `/products/{productId}`
  - `name`: string
  - `description`: string
  - `category`: string
  - `price`: number
  - `sellerName`: string
  - `userId`: string
  - `imageUrls`: array of strings

---

> **Notas importantes**:
> - `users`, `products`, `favorites` and `activities` are core collections.
> - Each document within a collection is identified by its `{documentId}`.
> - Firestore native data types are used: `string`, `number`, `timestamp`, `array`.

## Advantages of using Firebase as a Backend

- Instant deployment without the need to configure servers.
- Automatic scaling to support user growth.
- Direct integration with Flutter, Kotlin, Android and iOS.
- High availability and security managed by Google Cloud.
- Real-time updates for users and products.
- Integrated analytics.
- Google Cloud infrastructure.
