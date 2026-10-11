# Aushadhi Pharma Wholesale Web App

Beginner-friendly Node.js starter for an online wholesale ordering app.

## Features
- Admin and retailer login
- Product catalogue with brand, salt/composition, category, pack, MRP, wholesale price, MOQ, stock and offers
- Search by brand, salt or category
- Cart and order placement
- WhatsApp order link
- Admin product/price/stock/offer management
- JSON file storage for a simple demo

## Run locally
1. Install Node.js 20 or later.
2. In this folder run `npm install`.
3. Copy `.env.example` to `.env` and set a strong `ADMIN_PASSWORD` and `SESSION_SECRET`.
4. Run `npm start`.
5. Open `http://localhost:3000`.

This starter uses JSON files and is suitable for testing only. For production, use PostgreSQL and durable image storage, add retailer verification, backups, rate limits, audit logs, and have legal/GST/drug-licence requirements reviewed. Do not put real customer data or production orders into a demo deployment.

## Deploy with Render
1. Create a GitHub repository and upload the CONTENTS of this folder (not the ZIP itself) to the repository root.
2. In Render choose **New → Blueprint** and connect the repository. `render.yaml` provides service settings.
3. Add `ADMIN_USERNAME`, `ADMIN_PASSWORD`, and `WHATSAPP_NUMBER` when prompted. Render generates `SESSION_SECRET`.
4. Deploy. Open the `onrender.com` URL and log in as admin.
5. IMPORTANT: Render free web service storage may be ephemeral. This demo's JSON data may reset on redeploy/restart. Use a managed database before taking real orders.

## Demo retailer account
Register from the app's login screen. Retailer registration does not verify a store's licence. Admin must verify retailers independently before fulfilling regulated medicine orders.

## Product data
Sample product is a draft placeholder. Verify prices, stock, composition, pack sizes, and regulatory details before publishing. Do not treat sample data as real rates.


## Installable app (PWA)
This updated package includes a web app manifest, service worker and SVG app icons. After the app is deployed on an HTTPS domain:
- Android: open the site in Chrome, open the browser menu, then choose **Install app** or **Add to Home screen** if offered.
- Windows: open the site in Microsoft Edge or Chrome and use the browser's **Install app** option if offered.
- Mac: open the site in a supported browser and use its install/add-to-dock option if available.

This is an installable web app (PWA), not a native APK/EXE/DMG installer. The service worker caches the app shell only; API requests and orders require an internet connection.

## Important before real business use
This package is still a starter, not a production-ready wholesale platform. It stores products/users/orders in local JSON files and sessions in server memory. Hosting providers may erase local data on redeploy/restart, and the current login/session implementation is not sufficient for production. Do not use it for real customer accounts or live orders until it has been upgraded to a managed persistent database, durable storage, stronger production authentication/security, backups and retailer licence verification. Sample product data and prices are placeholders and must be verified.
