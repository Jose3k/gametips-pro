# Analytics Dashboard Application

## Overview

This is a full-stack analytics dashboard application built for product management insights. It features natural language to SQL query translation, customizable dashboard widgets, and real-time data visualization. The application is designed to help product teams analyze user behavior, feature adoption, and key metrics through an intuitive interface.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for client-side routing
- **State Management**: TanStack Query (React Query) for server state
- **UI Framework**: Shadcn/ui components with Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming
- **Build Tool**: Vite for development and production builds
- **Charts**: Recharts for data visualization

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ESM modules
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **API Design**: RESTful API endpoints
- **Development**: Hot module replacement with Vite integration

### Database Layer
- **ORM**: Drizzle ORM for type-safe database operations
- **Schema**: Centralized schema definitions in `shared/schema.ts`
- **Migrations**: Drizzle Kit for database migrations
- **Tables**: Users, dashboards, queries, product analytics data

## Key Components

### Natural Language Query System
- **AI Integration**: OpenAI GPT-4o for SQL translation
- **Query Translation**: Converts natural language to PostgreSQL queries
- **Smart Suggestions**: Automatic chart type recommendations
- **Query Validation**: Schema-aware query generation

### Dashboard Builder
- **Widget System**: Modular chart components (bar, line, pie, tables, metrics)
- **Layout Engine**: Grid-based dashboard layout
- **Real-time Updates**: Live data refresh capabilities
- **Export Features**: Dashboard and data export functionality

### Data Visualization
- **Chart Types**: Bar charts, line charts, pie charts, data tables, metric cards
- **Interactive Elements**: Hover states, tooltips, responsive design
- **Theme Support**: Light/dark mode with CSS custom properties

### Query Management
- **SQL Editor**: Syntax-highlighted SQL editor
- **Query History**: Saved queries with metadata
- **Result Caching**: Query result caching for performance
- **Query Execution**: Safe query execution with result limiting

## Data Flow

1. **User Input**: Natural language queries or direct SQL input
2. **AI Processing**: OpenAI translates natural language to SQL
3. **Query Execution**: Validated queries run against PostgreSQL database
4. **Data Processing**: Results formatted for visualization components
5. **UI Rendering**: Charts and tables rendered with real-time updates
6. **State Management**: TanStack Query handles caching and synchronization

## External Dependencies

### Core Dependencies
- **OpenAI API**: Natural language processing and SQL generation
- **Neon Database**: Serverless PostgreSQL hosting
- **Radix UI**: Accessible component primitives
- **Recharts**: Chart rendering library
- **React Hook Form**: Form state management
- **Zod**: Runtime type validation

### Development Tools
- **Vite**: Build tool and development server
- **TypeScript**: Type safety and enhanced DX
- **Tailwind CSS**: Utility-first CSS framework
- **ESBuild**: Fast JavaScript bundling
- **Drizzle Kit**: Database migration tool

## Deployment Strategy

### Platform
- **Hosting**: Replit with autoscale deployment
- **Build Process**: `npm run build` creates production bundles
- **Server Bundle**: ESBuild bundles server code for Node.js
- **Client Bundle**: Vite builds optimized React application

### Environment Configuration
- **Database**: PostgreSQL connection via `DATABASE_URL`
- **AI Services**: OpenAI API key for natural language processing
- **Port Configuration**: Express server on port 5000 (mapped to 80 externally)

### Production Optimizations
- **Static Assets**: Vite handles asset optimization and bundling
- **Code Splitting**: Automatic route-based code splitting
- **Caching**: Query result caching and static asset caching
- **Error Handling**: Comprehensive error boundaries and API error handling

## Changelog

```
Changelog:
- June 27, 2025. Initial setup
```

## User Preferences

```
Preferred communication style: Simple, everyday language.
```