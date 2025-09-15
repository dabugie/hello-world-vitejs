# Hello World - React + TypeScript + Vite

A quick containerized React application for testing port integration in servers. Built with TypeScript and Vite, featuring Docker deployment with Nginx.

## Features

- ⚡️ **Vite** - Fast build tool with HMR (Hot Module Replacement)
- ⚛️ **React 18.3.1** - Latest React with concurrent features
- 🔷 **TypeScript** - Type-safe development
- 🎨 **SWC** - Super-fast TypeScript/JavaScript compiler
- 📦 **Docker** - Containerized deployment with Nginx
- 🔧 **ESLint** - Code linting and formatting

## Getting Started

### Prerequisites

- Node.js (v20 or higher)
- npm or yarn
- Docker (for containerized deployment)

### Development

1. Install dependencies:
```bash
npm install
```

2. Start development server:
```bash
npm run dev
```

3. Open [http://localhost:5173](http://localhost:5173) in your browser

### Production Build

```bash
npm run build
```

### Docker Deployment

Build and run the application in a Docker container:

```bash
npm run docker:up
```

This will build the Docker image and run the container on [http://localhost:3000](http://localhost:3000)

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint
- `npm run docker:up` - Build and run Docker container

## Project Structure

```
├── src/                 # Source code
├── deployment/          # Docker configuration
│   ├── Dockerfile       # Multi-stage Docker build
│   ├── docker-compose.yml
│   └── nginx/
│       └── nginx.conf   # Nginx configuration
├── public/              # Static assets
└── dist/                # Production build output
```

## Technologies Used

- **React**: Frontend library
- **TypeScript**: Type-safe JavaScript
- **Vite**: Build tool and dev server
- **SWC**: Fast TypeScript/JavaScript compiler
- **Docker**: Containerization
- **Nginx**: Web server for production
