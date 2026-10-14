# RideShield — Secure Ride Sharing Application

A responsive front-end prototype built with **HTML, custom CSS, and vanilla JavaScript**.

## Features
- **Rider access:** search by pickup, destination, date, and passenger count (1–6); book and cancel sample rides.
- **Driver access:** inspect sample listings and publish ride offers with seats, departure time, and price per seat.
- **Administrator console:** manage sample listings, inspect local activity, and export demo data as JSON.
- **Optional device location:** browser permission is requested only when the rider clicks “Use my current location”; manual entry is always available.
- **Responsive, custom visual design:** graphite surfaces, mint route accents, map-inspired art, and mobile layouts.
- **Booking validation and local demo activity trail.**

## Run locally
1. Extract the ZIP.
2. Open `index.html` in a modern browser.
3. For geolocation, use `http://localhost` or HTTPS. Browsers may block location access for a `file://` page; the rest of the app works without it.

Optional local server:
```bash
python -m http.server 8000
```
Then visit `http://localhost:8000`.

## Demo roles
Use the **View as** selector at the top-right to switch between Rider, Driver, and Administrator. This simulates role-specific screens; it is **not authentication**. Data is held in memory and resets when the page refreshes.

## Security note
This is an educational front-end prototype. It has no backend, database, real identity verification, live driver tracking, or payment processing. Role access is simulated in client-side JavaScript and must not be treated as secure authorization. GPS coordinates are used only to fill the pickup field and are not sent to a server by this demo. Do not enter real personal, payment, or travel information.

For production, add server-side authentication and authorization, validated APIs, encrypted transport, secure storage, audit logging, rate limiting, consent/retention controls, and a vetted maps provider. Enforce every role permission on the server.

## Files
- `index.html` — application structure
- `style.css` — custom responsive styling
- `app.js` — sample rides, role simulation, location permission, bookings, and activity
- `README.md` — setup and security notes

For learning and demonstration. Add an appropriate license before public redistribution.
