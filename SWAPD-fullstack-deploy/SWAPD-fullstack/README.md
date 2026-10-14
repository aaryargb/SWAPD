# SWAPD — Full-stack student marketplace

Node.js 22.13+ app, SQLite database, secure password hashing (scrypt), HttpOnly session cookies, server-side input validation, listings and seller inquiries.

## Local setup

```bash
npm start
```

Open http://localhost:3000. Accounts, listings and inquiries are persisted in `swapd.sqlite`.

## Deploy on Render

1. Upload this folder to a private GitHub repository (do not commit `.sqlite` files).
2. In Render choose **New > Blueprint**, connect the repository and apply `render.yaml`.
3. Confirm the **Starter plan and persistent disk charges** before deploying.
4. Visit the Render URL after the deployment completes. `NODE_ENV=production` enables secure session cookies over HTTPS.

**Important:** SQLite requires a persistent disk for reliable data retention. Do not deploy this app on ephemeral storage if you need user accounts and listings to survive restarts. Render's persistent disks are paid. For a production launch, add verified college email, rate limits, moderation, CSRF defenses, image uploads, password resets, monitoring, backups, and a scalable database. No payment processing is implemented; 5% platform fees and ₹29 premium listings in the concept deck are not charged by this prototype.

Sample listings are seeded once and have no real seller, so their contact option is disabled. New user listings support real inquiry submission and seller inbox viewing.
