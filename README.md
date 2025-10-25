# AutoParts E-commerce (Next.js + Prisma)

Modern, responsive e-commerce for car parts and accessories with a customer store and admin dashboard.

## Tech Stack
- Next.js 14 (App Router, TypeScript)
- Prisma ORM + PostgreSQL
- Tailwind CSS
- API routes under `src/app/api/*`

## Getting Started
1. Clone the repo
2. Install deps
```bash
pnpm install # or npm i / yarn
```
3. Configure environment
- Copy `.env.example` to `.env`
- Set `DATABASE_URL` and secrets
4. Database
```bash
pnpm prisma:generate
pnpm prisma:migrate
```
5. Run
```bash
pnpm dev
```

## Project Structure
- `src/app` — routes and pages
- `src/components` — UI components
- `src/lib/prisma.ts` — Prisma client
- `prisma/schema.prisma` — data models

## Features Implemented

### ✅ Authentication & Authorization
- JWT-based authentication with HTTP-only cookies
- Role-based access control (Admin, Accountant, Staff, Customer)
- Protected routes with middleware
- Login/Register pages with form validation
- User menu with role-based navigation
- Server-side auth utilities for API routes

### ✅ API Endpoints
- **Auth**: `/api/auth/login`, `/api/auth/register`, `/api/auth/logout`, `/api/auth/me`
- **Cart**: `/api/cart` (GET/POST), `/api/cart/items/[itemId]` (PUT/DELETE)
- **Orders**: `/api/orders` (GET/POST), `/api/orders/[orderId]` (GET/PATCH)
- **Reviews**: `/api/reviews` (GET/POST), `/api/reviews/[reviewId]` (PUT/DELETE)
- **Wishlist**: `/api/wishlist` (GET/POST), `/api/wishlist/[productId]` (DELETE)
- **Admin**: `/api/admin/dashboard` (GET)

### ✅ Database Schema
- Complete Prisma schema with all entities
- User roles, products, orders, cart, reviews, wishlist
- Car compatibility system (Make/Model/Year)
- Address management, payment tracking

## Roadmap (remaining)
- Catalog search/filters + compatibility checker UI
- Checkout with Stripe integration
- Accounting module (invoices/reports)
- i18n and multi-currency support

## License
MIT
