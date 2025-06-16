# Messages

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Messages is a real-time chat application built with Next.js 13, Prisma, and Pusher. It provides group and direct messaging with social logins and file uploads out of the box.

## Table of Contents
- [Features](#features)
- [Demo](#demo)
- [Setup](#setup)
  - [Simple Mode Setup](#simple-mode-setup)
  - [Advanced Mode Setup](#advanced-mode-setup)
- [Usage](#usage)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [FAQ](#faq)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

## Features
- Real-time chat powered by Pusher
- Social and credential authentication via NextAuth
- Group conversations and one-on-one messaging
- File and image uploads through Cloudinary
- Read receipts and online status indicators
- Responsive UI built with Tailwind CSS
- TypeScript and Prisma for type-safe data handling
- Client-side form validation with react-hook-form
- Toast notifications for errors and status updates

## Demo
A short demo is available on [YouTube](https://www.youtube.com/watch?v=PGPGcKBpAk8).

## Setup
Below are quick steps to get the project running. Environment variables are required for database access, authentication, and Pusher.

### Simple Mode Setup
1. **Clone the Repository**
   ```bash
   git clone <repo-url>
   cd messages
   ```
2. **Install Dependencies**
   ```bash
   npm install
   ```
3. **Configure Environment**
   ```bash
   cp .env .env.local
   ```
   Required variables:
   * `APP_MODE=simple`
   * `DATABASE_URL=`
   * `NEXTAUTH_SECRET=`
   * `NEXT_PUBLIC_PUSHER_APP_KEY=`
   * `PUSHER_APP_ID=`
   * `PUSHER_SECRET=`
   * `NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=`
   * `GITHUB_ID=`
   * `GITHUB_SECRET=`
   * `GOOGLE_CLIENT_ID=`
   * `GOOGLE_CLIENT_SECRET=`
4. **Run the App**
   ```bash
   npm run dev
   ```
   To run tests, use `npm test`. Lint the project with `npm run lint`.

### Advanced Mode Setup
Advanced mode may require a production database, custom Pusher configuration, or additional plugins. Set `APP_MODE=advanced` in `.env.local` and provide any extra secrets such as a Cloudinary API key.

## Usage
1. Sign up or log in with GitHub, Google, or email credentials.
2. Create a conversation and add participants or start a direct chat.
3. Send messages or upload files. Uploaded images will appear inline.
4. Read receipts and online indicators update automatically in real time.

## Deployment
Deployments work great on Vercel.
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project)
1. Push your fork to GitHub.
2. In Vercel, import the project and set the environment variables from `.env.local`.
3. Trigger a deployment.

## Contributing
Pull requests are welcome. For major changes, please open an issue first. Be sure to run `npm install` and `npm run lint` before submitting.

## FAQ
1. **Is there a test suite?** Not yet. Lint the project with `npm run lint`.
2. **What Node version is required?** Node 18 LTS is recommended.
3. **How do I reset the database?** Update `DATABASE_URL` in `.env.local` and run `npx prisma db push`.

## License
This project is licensed under the MIT license.

## Acknowledgements
- [Next.js](https://nextjs.org/)
- [Prisma](https://www.prisma.io/)
- [Pusher](https://pusher.com/)
- [Tailwind CSS](https://tailwindcss.com/)

## Contact
For issues or feature requests, please open an issue on GitHub.
