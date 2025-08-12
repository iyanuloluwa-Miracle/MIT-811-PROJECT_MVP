## App Routes

| Route                | Description                       |
|----------------------|-----------------------------------|
| `/`                  | Landing page                      |
| `/listings`          | Browse/search listings            |
| `/listings/create`   | Create a new listing              |
| `/auth/signin`       | Sign in (Tenant, Landlord, Agent) |
| `/auth/signup`       | Sign up (Tenant, Landlord, Agent) |
| `/contact`           | Contact form                      |
| `/profile`           | User profile (static)             |

# Peer-to-Peer Housing Platform (MIT-811 School Project)

## Project Overview
This project is a static MVP for a Peer-to-Peer Housing Platform, built as part of the MIT-811 course. The platform allows students and young professionals to find, list, and review housing options in a safe, transparent, and community-driven environment.

## Implementation Summary
- **Framework:** Nuxt.js (Vue 3, static site generation)
- **Styling:** TailwindCSS
- **Architecture:** Modular, component-based
- **Data:** All data is hardcoded (no backend)

## Features Implemented
- Landing page with problem statement and solution
- Modern, responsive navigation bar
- Role-based authentication (static, for demo)
- Create listing form (with dummy data)
- Search/filter listings
- Listing cards with images, reviews, and verification badge
- Contact page (static form)
- User profile page (static)
- Privacy controls and review system (static)
- Consistent, modern UI using slate color palette

## How to Use
1. Clone or download this repository.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the development server.
4. Open `http://localhost:3000` in your browser.

## Screenshots
Add screenshots of your app here:

![Landing Page](screenshots/landing.png)
![Listings Page](screenshots/listings.png)
![Create Listing](screenshots/create-listing.png)

## Student Details
- **Name:**
- **Matric Number:**

> _Please fill in your name and matric number above before submission._

---
_MIT-811 School Project – Peer-to-Peer Housing Platform_
Look at the [Nuxt documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Setup

Make sure to install dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
