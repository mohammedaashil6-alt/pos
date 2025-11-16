# POS ASI - Setup Guide

## Prerequisites

- Node.js 18+ and npm
- A Supabase account (free tier works)
- Modern web browser with PWA support

## Step 1: Install Dependencies

```bash
cd pos-asi
npm install
```

## Step 2: Set Up Supabase

1. Go to [supabase.com](https://supabase.com) and create a new project
2. Wait for the project to be fully provisioned
3. Go to **Settings** > **API** to get your project URL and anon key
4. Copy the `.env.example` file to `.env`:
   ```bash
   cp .env.example .env
   ```
5. Update `.env` with your Supabase credentials:
   ```
   VITE_SUPABASE_URL=https://your-project.supabase.co
   VITE_SUPABASE_ANON_KEY=your-anon-key-here
   ```

## Step 3: Set Up Database

1. In your Supabase project, go to **SQL Editor**
2. Open the `database-schema.sql` file from this project
3. Copy and paste the entire SQL script into the SQL Editor
4. Click **Run** to execute the schema
5. Verify tables were created by going to **Table Editor**

## Step 4: Configure Authentication

1. In Supabase, go to **Authentication** > **Providers**
2. Enable **Email** provider (already enabled by default)
3. Optionally configure other providers as needed
4. Go to **Authentication** > **Users** to create your first user:
   - Click **Add user** > **Create new user**
   - Enter email and password
   - Save the credentials for login

## Step 5: Run the Application

```bash
npm run dev
```

The application will start on `http://localhost:3000`

## Step 6: Install as PWA (Optional)

1. Open the app in a mobile browser (Chrome, Safari, Edge)
2. Look for the "Add to Home Screen" prompt
3. Or use the browser menu: **Menu** > **Add to Home Screen**

## Features Overview

### ✅ Implemented Features

- User Authentication (Login/Logout)
- Dashboard with sales summary
- Point of Sale interface
- Product Management (CRUD)
- Inventory Management
- Invoice Scanner (camera integration)
- Sales Reports with charts
- Customer Management
- Transaction History
- Settings page
- PWA support with offline capability
- Responsive mobile-first design

### 🔧 Configuration Needed

1. **Barcode Scanner**: Integrate Web Bluetooth API for hardware scanners
2. **Image Upload**: Configure Supabase Storage bucket for product images
3. **Receipt Printing**: Configure print API integration
4. **Push Notifications**: Set up service worker for low-stock alerts
5. **Multi-location**: Configure location management if needed

## Troubleshooting

### Database Connection Issues

- Verify your Supabase URL and anon key in `.env`
- Check that the database schema was created successfully
- Ensure Row Level Security policies are set correctly

### Authentication Issues

- Verify email provider is enabled in Supabase
- Check that user exists in Supabase Auth
- Clear browser cache and try again

### PWA Installation Issues

- Ensure you're using HTTPS (required for PWA)
- Check browser console for service worker errors
- Verify manifest.json is being served correctly

## Development

### Project Structure

```
pos-asi/
├── src/
│   ├── components/     # Reusable UI components
│   ├── pages/          # Page components
│   ├── contexts/       # React contexts (Auth)
│   ├── services/       # API services
│   ├── App.jsx         # Main app component
│   └── main.jsx        # Entry point
├── public/             # Static assets
├── database-schema.sql # Database setup
└── package.json        # Dependencies
```

### Building for Production

```bash
npm run build
```

The built files will be in the `dist/` directory, ready for deployment.

## Support

For issues or questions, please contact the ASI Group development team.

