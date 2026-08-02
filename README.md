# Dokanee - E-Commerce (MERN)

Just a full-stack e-commerce app I built with the MERN stack. Has auth, payments with Stripe, real-time order updates, and a pretty solid admin panel.

Live Demo: [dokane.onrender.com](https://dokane.onrender.com/)
Source Code: [GitHub Repo](https://github.com/MohammedYazji/dokane-ecommerce-mern)

## What it does

- Login and register with JWT + Redis
- Browse, search, filter and sort products
- Star ratings and reviews, verified purchases get a badge
- Wishlist and cart support
- Switch between USD, EUR or GBP
- Stock tracking, sold out items can't be added
- Stripe checkout with shipping address
- Order history with a live tracking timeline
- Confirmation and shipping email notifications
- Admin dashboard for products, orders, customers, subscribers and settings
- New orders pop up on the dashboard in real time via Socket.io

## Tech stack

- **Frontend:** React, TailwindCSS, Zustand
- **Backend:** Node.js, Express, MongoDB
- **Realtime:** Socket.io
- **Other:** Redis, Stripe, Cloudinary, Nodemailer

## Running it locally

```bash
npm install
npm install --prefix client

# copy .env.example to .env and fill in your keys
cp .env.example .env

# start the server and client
npm run dev
npm run dev --prefix client
```

For Stripe webhooks in dev:

```bash
stripe listen --forward-to localhost:3000/api/v1/payments/webhook
```

Then grab the `whsec_...` it prints and put it in `STRIPE_WEBHOOK_SECRET`.

## Admin access

Use this to log in and check the dashboard:

Email: admin@dokane.io
Password: 123456
