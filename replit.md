# Overview

This is a Nike-style e-commerce web application built as a minimum viable product (MVP) for selling shoes, clothing, and collections. The application features a modern React frontend with a comprehensive product catalog, shopping cart functionality, and an admin dashboard for managing products and orders. It's designed to provide a complete online shopping experience with a focus on athletic and fashion products.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
The frontend is built using React with TypeScript and follows a component-based architecture. The application uses Vite as the build tool and development server, providing fast hot module replacement and optimized builds. The UI is implemented using shadcn/ui components built on top of Radix UI primitives, ensuring accessibility and consistent design patterns.

**Key Frontend Decisions:**
- **React with TypeScript**: Provides type safety and better developer experience
- **Wouter for routing**: Lightweight routing solution instead of React Router
- **TanStack Query**: Handles server state management, caching, and data fetching
- **Zustand**: Manages client-side state (shopping cart) with persistence
- **Tailwind CSS**: Utility-first CSS framework for rapid styling
- **shadcn/ui**: Pre-built, accessible component library

## Backend Architecture
The backend follows a REST API pattern built with Express.js and TypeScript. It uses a layered architecture with clear separation between routes, storage logic, and database operations. The storage layer abstracts database operations, making it easier to test and maintain.

**Key Backend Decisions:**
- **Express.js**: Mature, lightweight web framework for Node.js
- **Storage Pattern**: Abstract storage interface for better testability
- **RESTful API design**: Standard HTTP methods and status codes
- **Middleware architecture**: Request logging, error handling, and JSON parsing

## Data Storage
The application uses PostgreSQL as the primary database with Drizzle ORM for type-safe database operations. The database schema supports a comprehensive e-commerce model with products, users, orders, and order items.

**Key Storage Decisions:**
- **PostgreSQL**: Robust relational database for complex queries and transactions
- **Drizzle ORM**: Type-safe SQL query builder with excellent TypeScript integration
- **Schema-first approach**: Database schema defined in TypeScript for consistency
- **Neon Database**: Serverless PostgreSQL for easy deployment and scaling

## Authentication and Authorization
Currently, the application has a basic user system without authentication middleware. The admin functionality is client-side only, which is suitable for an MVP but should be secured for production use.

**Current Limitations:**
- No authentication middleware
- Admin access not protected
- No session management

## Component Organization
The frontend follows a well-organized component structure:
- **Pages**: Top-level route components
- **Layout components**: Navbar, footer, and structural elements
- **UI components**: Reusable shadcn/ui components
- **Modals**: Cart and admin functionality in overlay components
- **Shared types**: TypeScript definitions shared between frontend and backend

# External Dependencies

## Database Services
- **Neon Database**: Serverless PostgreSQL database hosting
- **Drizzle ORM**: Type-safe database toolkit and query builder
- **connect-pg-simple**: PostgreSQL session store for Express

## UI and Styling
- **Tailwind CSS**: Utility-first CSS framework
- **Radix UI**: Unstyled, accessible UI primitives
- **shadcn/ui**: Pre-built component library based on Radix UI
- **Lucide React**: Icon library for consistent iconography

## State Management and Data Fetching
- **TanStack React Query**: Server state management and caching
- **Zustand**: Lightweight state management for client-side state
- **React Hook Form**: Form state management and validation
- **Zod**: Runtime type validation and schema validation

## Development and Build Tools
- **Vite**: Fast build tool and development server
- **TypeScript**: Static type checking
- **ESBuild**: Fast JavaScript/TypeScript bundler
- **PostCSS**: CSS processing with Autoprefixer

## Image and Asset Hosting
- **Unsplash**: External image hosting for product images (development only)
- Note: Production implementation should use a proper CDN or image service

## Deployment and Hosting
- **Replit**: Development and hosting platform
- **Node.js**: Runtime environment for the Express server