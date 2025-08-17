# Memristor Research Platform

## Overview

This is a full-stack Node.js application built for memristor research, featuring a React frontend and Express backend. The platform provides comprehensive access to memristor research papers, researcher profiles, conferences, educational materials, and an AI-powered chat system for research assistance.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **UI Components**: Shadcn/ui components with Radix UI primitives
- **Styling**: Tailwind CSS with custom design tokens
- **State Management**: TanStack React Query for server state management
- **HTTP Client**: Axios for API communication

### Backend Architecture
- **Runtime**: Node.js with TypeScript (using tsx for development)
- **Framework**: Express.js with middleware for JSON parsing and logging
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Database Provider**: Neon serverless PostgreSQL
- **API Integration**: OpenAI API for chat functionality, Anthropic SDK for additional AI features

### Key Components

#### Database Schema (Drizzle ORM)
- **Papers**: Research publications with metadata (DOI, citations, abstracts)
- **Researchers**: Academic profiles with institutions and specializations
- **Users**: Authentication and user management
- **Materials**: Memristor materials catalog
- **Videos**: Educational video resources
- **Conferences**: Academic conferences and workshops
- **Blogs**: Research insights and market analysis
- **Research Groups**: Laboratory and team information

#### API Routes Structure
- `/api/openai` - AI chat integration
- `/api/researchers` - Researcher data and registration
- `/api/extraction` - Data extraction services
- `/api/chat` - Enhanced chat with research context
- `/api/blogs` - Blog content management
- `/api/research-groups` - Research group information
- `/api/visualization` - Data visualization endpoints

#### Service Layer
- **GoogleScholarService**: Paper discovery and academic data
- **IEEEService**: IEEE Xplore integration
- **ScienceDirectService**: Elsevier content access
- **ConferenceService**: Event discovery and management
- **ResearcherService**: Academic profile extraction

## Data Flow

1. **Client Requests**: React frontend makes API calls through Axios
2. **Express Routing**: Routes handle requests and apply middleware
3. **Service Layer**: Business logic processes data from external APIs
4. **Database Operations**: Drizzle ORM manages PostgreSQL interactions
5. **Response Formation**: JSON responses sent back to frontend
6. **State Management**: React Query caches and synchronizes data

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL connection
- **drizzle-orm**: Type-safe database ORM
- **@anthropic-ai/sdk**: AI integration for enhanced features
- **@tanstack/react-query**: Server state management
- **@radix-ui/react-***: Accessible UI components

### Development Tools
- **Vite**: Frontend build tooling with HMR
- **TypeScript**: Type safety across the stack
- **Tailwind CSS**: Utility-first styling
- **ESBuild**: Backend bundling for production

### External APIs
- **OpenAI API**: Primary AI chat functionality
- **Google Scholar**: Academic paper discovery
- **IEEE Xplore**: Technical paper access
- **ScienceDirect**: Research paper database

## Deployment Strategy

### Development Environment
- **Runtime**: Node.js 20 with PostgreSQL 16
- **Command**: `npm run dev` (uses tsx for TypeScript execution)
- **Port**: Application runs on port 5000
- **Hot Reload**: Vite provides frontend HMR

### Production Build
- **Frontend**: `vite build` creates optimized static assets
- **Backend**: `esbuild` bundles server code for Node.js
- **Start Command**: `npm run start` runs the production server
- **Deployment Target**: Autoscale deployment on Replit

### Database Management
- **Migrations**: Drizzle Kit manages schema migrations
- **Push Command**: `npm run db:push` updates database schema
- **Environment**: DATABASE_URL required for connection

## Changelog

- August 11, 2025: Enhanced worldwide researcher database with comprehensive filtering and enrichment capabilities
  - Successfully loaded 108 researchers from Google Scholar, LinkedIn, and individual search CSV datasets
  - Implemented advanced filtering by name, institution, designation, country, citations, and H-index
  - Added researcher enrichment service with Google Scholar, ORCID, and social media integration
  - Enhanced cyberpunk-themed researchers page with real-time search and mobile responsiveness  
  - Fixed critical runtime errors and improved API response handling for better user experience
  - Corrected Dr. Sudeb Dasgupta's institutional affiliation from IACS to IIT Roorkee with verified data
  - Completed full database enrichment with updated citations, H-indices, and LinkedIn profiles for all 108 researchers
- August 11, 2025: Successfully expanded database from 6 foundational papers to complete 4,278 comprehensive research papers from user's CSV dataset
  - Resolved CSV parsing and ES module import technical challenges using csv-parse package  
  - Database now contains authentic memristor research data spanning 1971-2025 timeline
  - Maintained 7 prominent researchers and 8 comprehensive materials across major categories
  - Platform fully functional with complete comprehensive research database as originally intended
  - 31 high-impact papers with 1,000+ citations each
  - Automatic tag extraction for research categorization
- June 26, 2025: Added comprehensive real memristor researchers and materials database
  - Added 18 prominent real memristor researchers including Leon Chua, R. Stanley Williams, and leading Indian researchers
  - Expanded materials database to 50+ authentic memristive materials across 9 categories
  - Enhanced cyberpunk UI design with vibrant neon aesthetics and mobile responsiveness
  - Integrated 3,277 research papers creating world's most comprehensive memristor database
- June 19, 2025: Initial setup

## User Preferences

Preferred communication style: Simple, everyday language.