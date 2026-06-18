# 🛒 Next.js E-Commerce Platform

![Next.js](https://img.shields.io/badge/Next.js-14+-black?style=for-the-badge&logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-3982CE?style=for-the-badge&logo=Prisma&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)

A full-stack, production-ready E-commerce platform built with modern web technologies. This project demonstrates a scalable architecture separating the client-side Next.js application from a robust Node.js/Express backend.

## ✨ Key Features

- 🛍️ **Complete Shopping Flow**: Browsing, Cart management, and Checkout.
- ⚡ **Flash Sales**: Timed promotional campaigns with dedicated inventory tracking.
- 🎟️ **Coupons & Loyalty Points**: Discount system and user reward points.
- 💳 **Payment Integration**: Support for PayOS (VietQR) and Casso.
- 🔐 **Authentication**: Secure JWT-based auth & Google OAuth integration.
- 🚀 **High Performance**: 
  - **Redis Caching** for products and flash sales.
  - **BullMQ** for background job processing (e.g., sending emails).
- 🛡️ **Security**: Rate limiting, Helmet, CORS, and Sentry Error Tracking.
- 📊 **Admin Dashboard**: Comprehensive management for Products, Orders, Users, Banners, and Settings.

## 🏗️ Architecture & Tech Stack

### Frontend (`/client`)
- **Framework**: Next.js (App Router)
- **UI/Styling**: Tailwind CSS v4, shadcn/ui, Base UI, Framer Motion
- **State Management**: Zustand
- **Data Fetching**: Axios

### Backend (`/server`)
- **Runtime**: Node.js & Express
- **Language**: TypeScript
- **Database**: PostgreSQL with Prisma ORM
- **Caching & Queues**: Redis & BullMQ
- **Error Tracking**: Sentry
- **API Documentation**: Swagger UI (`/api-docs`)

## 🗄️ Database Schema
The database is highly normalized and typed via Prisma, including the following core models:
`User`, `Product`, `Category`, `Order`, `OrderItem`, `Coupon`, `Review`, `FlashSale`, `Banner`, and `Setting`.

## 🚀 Getting Started

### Prerequisites
- Node.js (v18+)
- PostgreSQL
- Redis
- pnpm (recommended)

### 1. Clone the repository
```bash
git clone https://github.com/taidev1499-bit/Demo_ecomerce.git
cd Demo_ecomerce
```

### 2. Setup Backend
```bash
cd server
pnpm install

# Setup environment variables
cp .env.example .env
# Fill in your DATABASE_URL, REDIS_URL, SENTRY_DSN, etc. in .env

# Run database migrations
pnpm run db:migrate

# Start the server
pnpm run dev
```

### 3. Setup Frontend
```bash
cd ../client
pnpm install

# Setup environment variables
cp .env.example .env.local
# Fill in your NEXT_PUBLIC_API_URL

# Start the frontend
pnpm run dev
```

## 📜 License
This project is open-source and available under the [MIT License](LICENSE).
