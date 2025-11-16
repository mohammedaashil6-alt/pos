# POS ASI - Point of Sale System

A comprehensive Progressive Web Application (PWA) designed for ASI Group of Companies to streamline point-of-sale operations, inventory management, and daily sales tracking.

## Features

- 🛍️ Product Management System
- 📦 Real-time Inventory Tracking
- 💰 Point of Sale Interface
- 📷 Barcode Scanner Integration
- 🧾 Invoice Processing
- 📊 Sales Reporting & Analytics
- 👥 Customer Management
- 🔐 Secure Authentication
- 📱 Offline Capability
- 🏪 Multi-location Support

## Tech Stack

- **Frontend**: React 18, Tailwind CSS, Vite
- **Backend**: Supabase (PostgreSQL, Auth, Storage, Real-time)
- **PWA**: Service Worker, Web App Manifest
- **APIs**: Web Bluetooth, Camera, Share, Print APIs

## Getting Started

### Prerequisites

- Node.js 18+ and npm
- Supabase account and project

### Installation

1. Install dependencies:
```bash
npm install
```

2. Create a `.env` file in the root directory:
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

3. Start the development server:
```bash
npm run dev
```

4. Build for production:
```bash
npm run build
```

## Project Structure

```
src/
├── components/     # Reusable UI components
├── pages/          # Page components
├── hooks/          # Custom React hooks
├── services/       # API services (Supabase)
├── utils/          # Utility functions
├── contexts/       # React contexts
├── styles/         # Global styles
└── assets/         # Static assets
```

## License

Proprietary - ASI Group of Companies

