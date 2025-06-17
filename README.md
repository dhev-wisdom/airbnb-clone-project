# Airbnb Clone Project

A full-scale clone of the core systems powering Airbnb. This project is designed to mimic the architecture, functionality, and features of the Airbnb platform — including property listings, bookings, reservations, payments, reviews, likes/favorites, user authentication, and more.

## 🚀 Project Overview

This Airbnb Clone is a comprehensive, production-ready project built to simulate real-world systems. It is intended for learning, experimentation, and potential extension into a deployable product. The backend is built primarily with **Django**, and leverages modern tools such as **GraphQL**, **PostgreSQL**, **Docker**, and **Kubernetes** for performance, scalability, and modularity.

## 🧰 Tech Stack

### Backend
- **Django**: Core backend framework
- **Django REST Framework (DRF)**: For REST APIs (where needed)
- **GraphQL (Graphene-Django)**: Primary API layer
- **PostgreSQL**: Relational database
- **Redis**: Caching & background tasks (via Celery)
- **Celery**: Task queue for asynchronous operations
- **Docker**: Containerized development & deployment
- **Kubernetes**: Container orchestration & scalability

### DevOps / Tooling
- **Docker Compose**: Development environment orchestration
- **Kubernetes YAML Configs**: Production-grade deployment
- **GitHub Actions** *(planned)*: CI/CD integration

### (Optional / In Progress) Frontend
- **React.js or Next.js**
- **Tailwind CSS**
- **Apollo Client** (for consuming GraphQL APIs)

## 🔧 Features (Implemented / In Progress)

### ✅ User Features
- User registration & login (JWT authentication)
- User profiles
- Host & guest roles

### 🏡 Property Listings
- Create, update, delete property listings
- Search and filter properties
- Upload property images

### 📅 Bookings & Reservations
- Book properties
- Reservation calendar
- Cancelations, refunds

### 💳 Payments
- Integration with payment gateways (e.g. Stripe)
- Transaction history
- Booking invoice generation

### ⭐ Reviews & Ratings
- Submit reviews
- Rate properties
- View average ratings

### ❤️ Likes / Favorites
- Favorite a property
- View saved properties

### 🔄 System Architecture
- Caching with Redis
- Background jobs for emails, notifications, cleanup
- Scalable microservice-like structure using Django apps
- GraphQL API schema for flexibility in frontend consumption

## 🧪 Testing

- Pytest/Django built-in testing suite
- Coverage reports
- Test cases for critical components (auth, bookings, payments)

## 🛠️ Setup & Installation

### Prerequisites
- Docker & Docker Compose
- Python 3.10+
- PostgreSQL
- Redis

### Development Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/airbnb-clone.git
cd airbnb-clone

# Build and run Docker containers
docker-compose up --build

# Run migrations
docker-compose exec web python manage.py migrate

# Create a superuser
docker-compose exec web python manage.py createsuperuser

# Access the app at
http://localhost:8000
