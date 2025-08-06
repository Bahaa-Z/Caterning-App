# Damascus Catering Website

## Overview

This is a modern React-based website for Damascus Catering, a Syrian catering business in Stuttgart, Germany. The application features a single-page design showcasing authentic Syrian cuisine and catering services with both German and Arabic language support.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript using Vite as the build tool
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **UI Components**: Shadcn/ui component library built on Radix UI primitives
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) for server state management
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js server
- **Language**: TypeScript with ES modules
- **Development**: Hot reload via Vite middleware integration
- **API**: RESTful endpoints for menu items, specials, and inquiries

### Database & Data Layer
- **ORM**: Drizzle ORM configured for PostgreSQL
- **Database**: PostgreSQL (configured but currently using in-memory storage)
- **Schema**: Shared schema definitions between client and server
- **Validation**: Zod schemas for runtime type checking

## Key Components

### Client-Side Components
- **Header**: Fixed navigation with smooth scrolling
- **Hero**: Full-screen landing section with call-to-action
- **About**: Company story and founders information
- **Services**: Catering service categories (corporate, wedding, private)
- **MenuShowcase**: Dynamic menu display with category filtering
- **WeeklySpecials**: Time-limited promotional items
- **Gallery**: Image showcase of food and events
- **Testimonials**: Customer reviews and ratings
- **BookingForm**: Contact form for catering inquiries
- **Contact**: Business location and contact information
- **Footer**: Site links and social media

### Server-Side Architecture
- **Routes**: RESTful API endpoints (`/api/menu`, `/api/specials`, `/api/inquiries`)
- **Storage**: Abstract storage interface with in-memory implementation
- **Middleware**: Request logging, JSON parsing, error handling
- **Development**: Vite integration for hot module replacement

## Data Flow

1. **Static Content**: Pre-populated menu items and specials in memory storage
2. **Menu Display**: Client fetches menu data via React Query, cached indefinitely
3. **Form Submission**: Inquiry forms validated with Zod, submitted via POST requests
4. **Real-time Updates**: React Query provides optimistic updates and error handling
5. **Responsive Design**: Tailwind breakpoints ensure mobile-first responsiveness

## External Dependencies

### Core Framework Dependencies
- React ecosystem (React, React DOM, React Hook Form)
- Vite for build tooling and development server
- Express.js for backend API
- TypeScript for type safety

### UI and Styling
- Tailwind CSS for utility-first styling
- Radix UI primitives for accessible components
- Lucide React for consistent iconography
- Class Variance Authority for component variants

### Data Management
- TanStack Query for server state management
- Drizzle ORM for database operations
- Zod for schema validation
- Date-fns for date manipulation

### Development Tools
- PostCSS with Autoprefixer
- ESBuild for production builds
- Replit-specific development plugins

## Deployment Strategy

### Build Process
1. **Client Build**: Vite builds React app to `dist/public`
2. **Server Build**: ESBuild bundles server code to `dist/index.js`
3. **Static Assets**: Client build output served by Express in production

### Environment Configuration
- **Development**: Vite dev server with HMR, TSX execution
- **Production**: Express serves built client assets and API routes
- **Database**: PostgreSQL connection via DATABASE_URL environment variable

### Scripts
- `dev`: Development mode with hot reload
- `build`: Production build for both client and server
- `start`: Production server execution
- `db:push`: Database schema migration via Drizzle

### Recent Changes - July 28, 2025
- ✓ Created complete Syrian catering website with authentic branding ("Damaskus Catering")
- ✓ Implemented all core features: hero, about, services, menu showcase, gallery, testimonials, contact form
- ✓ Built production bundle successfully with proper port configuration (0.0.0.0 binding)
- ✓ Verified production build works correctly - ready for deployment
- ✓ Website features German content with Syrian food focus, warm color scheme (burgundy/gold)

### Hosting Considerations
- Single-server deployment serving both API and static assets
- PostgreSQL database required for production
- Environment variables for database connection
- Node.js runtime environment needed
- Production build ready with proper port binding configuration