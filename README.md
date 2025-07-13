# 🎮 Discord Clone - Full Stack Real-Time Chat Application

A modern, full-featured Discord clone built with **Next.js 13**, **React**, **Socket.io**, **Prisma**, **TailwindCSS**, **MySQL**, and **TypeScript**. This application provides real-time messaging, voice/video calls, server management, and a beautiful, responsive user interface.

![Discord Clone](https://img.shields.io/badge/Next.js-13-black?style=for-the-badge&logo=next.js)
![React](https://img.shields.io/badge/React-18-blue?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=for-the-badge&logo=typescript)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3-38B2AC?style=for-the-badge&logo=tailwind-css)
![Prisma](https://img.shields.io/badge/Prisma-5-2D3748?style=for-the-badge&logo=prisma)

## ✨ Features

### 🔐 Authentication & Security
- **Secure Authentication** with Clerk
- **Role-based Access Control** (Admin, Moderator, Guest)
- **Protected Routes** and API endpoints

### 💬 Real-Time Communication
- **Real-time messaging** using Socket.io
- **WebSocket fallback** with polling for reliability
- **Message editing and deletion** in real-time
- **File attachments** support (images, PDFs) via UploadThing
- **Emoji picker** for enhanced messaging experience

### 📺 Voice & Video Calls
- **Text, Audio, and Video channels**
- **1:1 video calls** between members
- **Group voice/video calls** using LiveKit
- **High-quality audio/video streaming**

### 🏢 Server Management
- **Create and customize servers** with images and names
- **Channel creation** (Text, Audio, Video)
- **Member management** (Kick, Role changes)
- **Unique invite link generation** with full invite system
- **Server settings and permissions**

### 🎨 User Experience
- **Beautiful UI** with TailwindCSS and ShadcnUI components
- **Dark/Light mode** theme switching
- **Fully responsive** mobile and desktop design
- **Infinite scroll** message loading (batches of 10)
- **Loading states and error handling**

### 🛠️ Technical Features
- **Form validation** using react-hook-form and Zod
- **RESTful API** with route handlers (app/api)
- **Database ORM** with Prisma
- **File upload** system with UploadThing
- **Real-time updates** across all connected clients

## 🏗️ Tech Stack

| Technology | Purpose | Version |
|------------|---------|---------|
| **Next.js** | React framework with SSR/SSG | 13.x |
| **React** | Frontend library | 18.x |
| **TypeScript** | Type-safe JavaScript | 5.x |
| **TailwindCSS** | Utility-first CSS framework | 3.x |
| **Prisma** | Database ORM | 5.x |
| **Socket.io** | Real-time communication | 4.x |
| **MySQL** | Database (PlanetScale) | - |
| **Clerk** | Authentication service | 4.x |
| **LiveKit** | Video/Audio streaming | 1.x |
| **UploadThing** | File upload service | 5.x |
| **Zod** | Schema validation | 3.x |
| **React Hook Form** | Form handling | 7.x |

## 🚀 Quick Start

### Prerequisites

- **Node.js** version 18.x.x or higher
- **npm** or **yarn** package manager
- **MySQL database** (PlanetScale recommended)
- **Clerk account** for authentication
- **UploadThing account** for file uploads
- **LiveKit account** for video/audio calls

### 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/devang47/discord-clone.git
   cd discord-clone
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Environment Setup**
   
   Create a `.env.local` file in the root directory:
   
   ```env
   # Clerk Authentication
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   CLERK_SECRET_KEY=your_clerk_secret_key
   NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
   NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
   NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/
   NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/

   # Database
   DATABASE_URL=your_mysql_database_url

   # UploadThing (File Uploads)
   UPLOADTHING_SECRET=your_uploadthing_secret
   UPLOADTHING_APP_ID=your_uploadthing_app_id

   # LiveKit (Video/Audio)
   LIVEKIT_API_KEY=your_livekit_api_key
   LIVEKIT_API_SECRET=your_livekit_api_secret
   NEXT_PUBLIC_LIVEKIT_URL=your_livekit_url
   ```

4. **Database Setup**
   ```bash
   # Generate Prisma client
   npx prisma generate
   
   # Push database schema
   npx prisma db push
   
   # (Optional) Seed the database
   npx prisma db seed
   ```

5. **Start the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

   Open [http://localhost:3000](http://localhost:3000) in your browser.

## 📁 Project Structure

```
discord-clone/
├── app/                    # Next.js 13 app directory
│   ├── (auth)/            # Authentication routes
│   ├── (invite)/          # Invite handling routes
│   ├── (main)/            # Main application routes
│   ├── (setup)/           # Initial setup page
│   ├── api/               # API routes
│   └── globals.css        # Global styles
├── components/            # Reusable React components
│   ├── chat/              # Chat-related components
│   ├── modals/            # Modal components
│   ├── navigation/        # Navigation components
│   ├── providers/         # Context providers
│   ├── server/            # Server-related components
│   └── ui/                # UI components (shadcn/ui)
├── hooks/                 # Custom React hooks
├── lib/                   # Utility functions and configurations
├── pages/                 # API routes for Socket.io
├── prisma/                # Database schema and migrations
└── public/                # Static assets
```

## 🛠️ Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build production bundle |
| `npm run start` | Start production server |
| `npm run lint` | Run ESLint |
| `npm run lint:fix` | Fix ESLint errors |
| `npm run type-check` | Run TypeScript checks |

## 🎯 Key Features Explained

### Real-Time Messaging
- Messages are instantly delivered using Socket.io
- Support for text, images, and PDF files
- Message editing and deletion with real-time updates
- Emoji reactions and rich text formatting

### Server & Channel Management
- Create unlimited servers with custom names and images
- Organize conversations with Text, Audio, and Video channels
- Manage members with role-based permissions
- Generate shareable invite links

### Voice & Video Calls
- High-quality audio/video streaming powered by LiveKit
- Support for both 1:1 conversations and group calls
- Screen sharing capabilities
- Adaptive bitrate for optimal performance

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [shadcn/ui](https://ui.shadcn.com/) for the beautiful UI components
- [Clerk](https://clerk.dev/) for authentication
- [LiveKit](https://livekit.io/) for video/audio streaming
- [UploadThing](https://uploadthing.com/) for file uploads
- [PlanetScale](https://planetscale.com/) for the database

## 📞 Support

If you have any questions or need help, please open an issue on GitHub or contact the maintainers.

---

<div align="center">
  <strong>Built with ❤️ using Next.js and modern web technologies</strong>
</div>
