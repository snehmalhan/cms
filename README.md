# Crowd Management System - Frontend

A real-time crowd management dashboard built with Angular, featuring live occupancy tracking, entry/exit monitoring, and analytics visualization.

## Live Demo

**Production URL**: [https://cms-frontend-seven-gamma.vercel.app/]

## Features

- **Real-Time Updates** via Socket.IO
  - Live occupancy metrics
  - Entry/exit notifications
  - Dynamic chart updates

- **Dashboard Analytics**
  - Live occupancy tracking
  - Today's footfall statistics
  - Average dwell time analysis
  - Demographics breakdown
  - Interactive charts

- **Entry/Exit Management**
  - Paginated visitor records
  - Real-time list updates
  - Data filtering

- **Notifications**
  - Real-time alert panel
  - Entry/exit notifications with avatars

## Tech Stack

- Angular
- Socket.IO Client
- SCSS
- Vercel (SSR Deployment)

## Installation

### Prerequisites
- Node.js 
- npm 
- Angular CLI 

### Setup Steps

```bash
# Step 1: Clone the repository
git clone https://github.com/snehmalhan/cms.git

# Step 2: Install dependencies
npm install

# Step 3: Start development server
ng serve
```

Navigate to `http://localhost:4200/`

## Running the Application

### Development
```bash
npm start          # Start dev server
ng serve -o        # Start and open browser
```

### Production Build
```bash
npm run build                    # Build for production
ng build --configuration production
```

### SSR Build
```bash
npm run build:ssr    # Build with SSR
npm run serve:ssr    # Serve SSR build
```

## Deployment
 Vercel

## Key Services

- **AuthService** - Authentication & token management
- **SocketService** - Socket.IO connection & events
- **AnalyticsService** - API calls for analytics
- **NotificationService** - Alerts & notifications

## API Integration

**Base URL**: `https://hiring-dev.internal.kloudspot.com`

### REST Endpoints
- `POST /api/auth/login` - Authentication
- `GET /api/sites` - Fetch sites
- `POST /api/analytics/footfall` - Footfall data
- `POST /api/analytics/dwell-time` - Dwell time
- `POST /api/analytics/occupancy` - Occupancy data
- `POST /api/analytics/demographics` - Demographics
- `POST /api/analytics/entry-exit` - Entry/exit records

### Socket.IO Events
**Listen**: `live_occupancy`, `occupancy`, `alert`  
**Emit**: `join`, `leave`