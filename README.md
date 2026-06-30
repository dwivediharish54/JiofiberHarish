# Jio WiFi Booking

Simple Jio WiFi booking website with secure admin login and appointment management.

## Features

- Public booking form for customers
- Saves booking requests to `bookings.json`
- Admin login at `/admin/login`
- Admin appointments page at `/admin/appointments.html`

## Local setup

1. Install dependencies:
   ```bash
   npm install
   ```
2. Create a `.env` file from `.env.example`:
   ```bash
   copy .env.example .env
   ```
3. Start the server:
   ```bash
   npm start
   ```
4. Open in browser:
   ```
   http://localhost:8000
   ```

## Admin login

- `http://localhost:8000/admin/login`
- Default user: `admin`
- Default password: `JioAdmin@1234`

> Change `ADMIN_PASSWORD` and `SESSION_SECRET` in `.env` before deploying.

## Environment variables

Use `.env` to set:

- `ADMIN_USER` (default: `admin`)
- `ADMIN_PASSWORD`
- `SESSION_SECRET`
- `PORT` (optional)
- `HOST` (optional)

## Deploying to Render

Render is a simple option for this Node app.

1. Push the repo to GitHub.
2. Create a new Web Service on Render.
3. Connect the GitHub repository.
4. Set the publish branch.
5. Set the build command:
   ```bash
   npm install
   ```
6. Set the start command:
   ```bash
   npm start
   ```
7. Add environment variables on Render:
   - `ADMIN_USER`
   - `ADMIN_PASSWORD`
   - `SESSION_SECRET`
   - `PORT` (optional)

After deploy, open the Render URL and go to `/admin/login` for admin access.

## Static-only GitHub Pages note

This project currently uses a backend API and sessions, so it cannot run fully on GitHub Pages without removing the server-side features.

If you want a static-only version, keep only `index.html`, `styles.css`, `script.js`, and remove `/api/bookings` plus admin pages.
