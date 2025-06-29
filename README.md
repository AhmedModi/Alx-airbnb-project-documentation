# Airbnb Clone Backend Documentation

## 📌 Project Overview
This repository documents the backend architecture for an Airbnb-like booking platform, covering core features, database design, and API specifications.

## 🌟 Key Features
| Feature Area          | Key Capabilities                                                                 |
|-----------------------|----------------------------------------------------------------------------------|
| **User System**       | JWT auth, OAuth2 login, role-based access (guest/host/admin)                    |
| **Property Listings** | Geolocation search, dynamic pricing, availability calendar                       |
| **Booking Engine**    | Date conflict prevention, cancellation policies, automated notifications         |
| **Payment Processing**| Stripe integration, multi-currency support, host payout automation               |
| **Review System**     | Verified reviews (booking-required), host responses, average rating calculations |

## 🗄 Database Schema
![ER Diagram](/features-and-functionalities/airbnb-erd.png)

Key Tables:
- `users` (Guests/Hosts)
- `properties` (Listings with geospatial data)
- `bookings` (Reservations with status tracking)
- `payments` (Transaction records)

## 🔌 API Endpoints (Sample)
```http
POST /api/auth/login
GET /api/properties?location=Paris&max_price=100
POST /api/bookings {property_id, dates, guest_count}
