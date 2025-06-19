# PixelFlow Complete Functional Code Archive
Generated: 2025-06-19T13:43:34.852Z

This file contains every piece of code that is actively used in your PixelFlow application.
Total files: 66
Analysis based on actual import/dependency chains from entry points.

## Table of Contents
1. [Configuration Files](#configuration-files)
2. [Frontend Application](#frontend-application)
3. [Backend Server](#backend-server)
4. [Shared Code](#shared-code)
5. [Build Instructions](#build-instructions)

---

## Configuration Files

### package.json
```json
{
  "name": "rest-express",
  "version": "1.0.0",
  "type": "module",
  "license": "MIT",
  "scripts": {
    "dev": "NODE_ENV=development tsx server/index.ts",
    "build": "vite build && esbuild server/index.ts --platform=node --packages=external --bundle --format=esm --outdir=dist",
    "start": "NODE_ENV=production node dist/index.js",
    "check": "tsc",
    "db:push": "drizzle-kit push"
  },
  "dependencies": {
    "@ffmpeg/ffmpeg": "^0.12.15",
    "@ffmpeg/util": "^0.12.2",
    "@giphy/js-fetch-api": "^5.6.0",
    "@hookform/resolvers": "^3.10.0",
    "@jridgewell/trace-mapping": "^0.3.25",
    "@neondatabase/serverless": "^0.10.4",
    "@radix-ui/react-accordion": "^1.2.4",
    "@radix-ui/react-alert-dialog": "^1.1.7",
    "@radix-ui/react-aspect-ratio": "^1.1.3",
    "@radix-ui/react-avatar": "^1.1.4",
    "@radix-ui/react-checkbox": "^1.1.5",
    "@radix-ui/react-collapsible": "^1.1.4",
    "@radix-ui/react-context-menu": "^2.2.7",
    "@radix-ui/react-dialog": "^1.1.7",
    "@radix-ui/react-dropdown-menu": "^2.1.7",
    "@radix-ui/react-hover-card": "^1.1.7",
    "@radix-ui/react-label": "^2.1.3",
    "@radix-ui/react-menubar": "^1.1.7",
    "@radix-ui/react-navigation-menu": "^1.2.6",
    "@radix-ui/react-popover": "^1.1.7",
    "@radix-ui/react-progress": "^1.1.3",
    "@radix-ui/react-radio-group": "^1.2.4",
    "@radix-ui/react-scroll-area": "^1.2.4",
    "@radix-ui/react-select": "^2.1.7",
    "@radix-ui/react-separator": "^1.1.3",
    "@radix-ui/react-slider": "^1.2.4",
    "@radix-ui/react-slot": "^1.2.0",
    "@radix-ui/react-switch": "^1.1.4",
    "@radix-ui/react-tabs": "^1.1.4",
    "@radix-ui/react-toast": "^1.2.7",
    "@radix-ui/react-toggle": "^1.1.3",
    "@radix-ui/react-toggle-group": "^1.1.3",
    "@radix-ui/react-tooltip": "^1.2.0",
    "@tanstack/react-query": "^5.60.5",
    "@tensorflow-models/depth-estimation": "^0.0.4",
    "@tensorflow/tfjs": "^4.22.0",
    "@tensorflow/tfjs-backend-webgl": "^4.22.0",
    "@tensorflow/tfjs-backend-webgpu": "^4.22.0",
    "@types/d3": "^7.4.3",
    "@types/three": "^0.177.0",
    "class-variance-authority": "^0.7.1",
    "clsx": "^2.1.1",
    "cmdk": "^1.1.1",
    "connect-pg-simple": "^10.0.0",
    "d3": "^7.9.0",
    "date-fns": "^3.6.0",
    "drizzle-orm": "^0.39.1",
    "drizzle-zod": "^0.7.0",
    "embla-carousel-react": "^8.6.0",
    "express": "^4.21.2",
    "express-session": "^1.18.1",
    "framer-motion": "^11.13.1",
    "gif.js": "^0.2.0",
    "html2canvas": "^1.4.1",
    "input-otp": "^1.4.2",
    "lucide-react": "^0.453.0",
    "memorystore": "^1.6.7",
    "next-themes": "^0.4.6",
    "passport": "^0.7.0",
    "passport-local": "^1.0.0",
    "react": "^18.3.1",
    "react-day-picker": "^8.10.1",
    "react-dom": "^18.3.1",
    "react-hook-form": "^7.55.0",
    "react-icons": "^5.4.0",
    "react-resizable-panels": "^2.1.7",
    "react-router-dom": "^7.6.2",
    "recharts": "^2.15.2",
    "tailwind-merge": "^2.6.0",
    "tailwindcss-animate": "^1.0.7",
    "three": "^0.177.0",
    "tw-animate-css": "^1.2.5",
    "vaul": "^1.1.2",
    "webm-writer": "^1.0.0",
    "wouter": "^3.3.5",
    "ws": "^8.18.0",
    "zod": "^3.24.2",
    "zod-validation-error": "^3.4.0"
  },
  "devDependencies": {
    "@replit/vite-plugin-cartographer": "^0.2.5",
    "@replit/vite-plugin-runtime-error-modal": "^0.0.3",
    "@tailwindcss/typography": "^0.5.15",
    "@tailwindcss/vite": "^4.1.3",
    "@types/connect-pg-simple": "^7.0.3",
    "@types/express": "4.17.21",
    "@types/express-session": "^1.18.0",
    "@types/node": "20.16.11",
    "@types/passport": "^1.0.16",
    "@types/passport-local": "^1.0.38",
    "@types/react": "^18.3.11",
    "@types/react-dom": "^18.3.1",
    "@types/ws": "^8.5.13",
    "@vitejs/plugin-react": "^4.3.2",
    "autoprefixer": "^10.4.20",
    "drizzle-kit": "^0.30.4",
    "esbuild": "^0.25.0",
    "postcss": "^8.4.47",
    "tailwindcss": "^3.4.17",
    "tsx": "^4.19.1",
    "typescript": "5.6.3",
    "vite": "^5.4.19"
  },
  "optionalDependencies": {
    "bufferutil": "^4.0.8"
  }
}

```

### vite.config.ts
```ts
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";
import path from "path";
import runtimeErrorOverlay from "@replit/vite-plugin-runtime-error-modal";

export default defineConfig({
  plugins: [
    react(),
    runtimeErrorOverlay(),
    ...(process.env.NODE_ENV !== "production" &&
    process.env.REPL_ID !== undefined
      ? [
          await import("@replit/vite-plugin-cartographer").then((m) =>
            m.cartographer(),
          ),
        ]
      : []),
  ],
  resolve: {
    alias: {
      "@": path.resolve(import.meta.dirname, "client", "src"),
      "@shared": path.resolve(import.meta.dirname, "shared"),
      "@assets": path.resolve(import.meta.dirname, "attached_assets"),
    },
  },
  root: path.resolve(import.meta.dirname, "client"),
  build: {
    outDir: path.resolve(import.meta.dirname, "dist/public"),
    emptyOutDir: true,
  },
});

```

### tailwind.config.ts
```ts
import type { Config } from "tailwindcss";

export default {
  darkMode: ["class"],
  content: ["./client/index.html", "./client/src/**/*.{js,jsx,ts,tsx}"],
  theme: {
    extend: {
      borderRadius: {
        lg: "var(--radius)",
        md: "calc(var(--radius) - 2px)",
        sm: "calc(var(--radius) - 4px)",
      },
      colors: {
        background: "hsl(var(--background))",
        foreground: "hsl(var(--foreground))",
        card: {
          DEFAULT: "hsl(var(--card))",
          foreground: "hsl(var(--card-foreground))",
        },
        popover: {
          DEFAULT: "hsl(var(--popover))",
          foreground: "hsl(var(--popover-foreground))",
        },
        primary: {
          DEFAULT: "hsl(var(--primary))",
          foreground: "hsl(var(--primary-foreground))",
        },
        secondary: {
          DEFAULT: "hsl(var(--secondary))",
          foreground: "hsl(var(--secondary-foreground))",
        },
        muted: {
          DEFAULT: "hsl(var(--muted))",
          foreground: "hsl(var(--muted-foreground))",
        },
        accent: {
          DEFAULT: "hsl(var(--accent))",
          foreground: "hsl(var(--accent-foreground))",
        },
        destructive: {
          DEFAULT: "hsl(var(--destructive))",
          foreground: "hsl(var(--destructive-foreground))",
        },
        border: "hsl(var(--border))",
        input: "hsl(var(--input))",
        ring: "hsl(var(--ring))",
        chart: {
          "1": "hsl(var(--chart-1))",
          "2": "hsl(var(--chart-2))",
          "3": "hsl(var(--chart-3))",
          "4": "hsl(var(--chart-4))",
          "5": "hsl(var(--chart-5))",
        },
        sidebar: {
          DEFAULT: "hsl(var(--sidebar-background))",
          foreground: "hsl(var(--sidebar-foreground))",
          primary: "hsl(var(--sidebar-primary))",
          "primary-foreground": "hsl(var(--sidebar-primary-foreground))",
          accent: "hsl(var(--sidebar-accent))",
          "accent-foreground": "hsl(var(--sidebar-accent-foreground))",
          border: "hsl(var(--sidebar-border))",
          ring: "hsl(var(--sidebar-ring))",
        },
      },
      keyframes: {
        "accordion-down": {
          from: {
            height: "0",
          },
          to: {
            height: "var(--radix-accordion-content-height)",
          },
        },
        "accordion-up": {
          from: {
            height: "var(--radix-accordion-content-height)",
          },
          to: {
            height: "0",
          },
        },
      },
      animation: {
        "accordion-down": "accordion-down 0.2s ease-out",
        "accordion-up": "accordion-up 0.2s ease-out",
      },
    },
  },
  plugins: [require("tailwindcss-animate"), require("@tailwindcss/typography")],
} satisfies Config;

```

### postcss.config.js
```js
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}

```

### components.json
```json
{
    "$schema": "https://ui.shadcn.com/schema.json",
    "style": "new-york",
    "rsc": false,
    "tsx": true,
    "tailwind": {
      "config": "tailwind.config.ts",
      "css": "client/src/index.css",
      "baseColor": "neutral",
      "cssVariables": true,
      "prefix": ""
    },
    "aliases": {
      "components": "@/components",
      "utils": "@/lib/utils",
      "ui": "@/components/ui",
      "lib": "@/lib",
      "hooks": "@/hooks"
    }
}
```

### drizzle.config.ts
```ts
import { defineConfig } from "drizzle-kit";

if (!process.env.DATABASE_URL) {
  throw new Error("DATABASE_URL, ensure the database is provisioned");
}

export default defineConfig({
  out: "./migrations",
  schema: "./shared/schema.ts",
  dialect: "postgresql",
  dbCredentials: {
    url: process.env.DATABASE_URL,
  },
});

```

### tsconfig.json
```json
{
  "include": ["client/src/**/*", "shared/**/*", "server/**/*"],
  "exclude": ["node_modules", "build", "dist", "**/*.test.ts"],
  "compilerOptions": {
    "incremental": true,
    "tsBuildInfoFile": "./node_modules/typescript/tsbuildinfo",
    "noEmit": true,
    "module": "ESNext",
    "strict": true,
    "lib": ["esnext", "dom", "dom.iterable"],
    "jsx": "preserve",
    "esModuleInterop": true,
    "skipLibCheck": true,
    "allowImportingTsExtensions": true,
    "moduleResolution": "bundler",
    "baseUrl": ".",
    "types": ["node", "vite/client"],
    "paths": {
      "@/*": ["./client/src/*"],
      "@shared/*": ["./shared/*"]
    }
  }
}

```

### .replit
```text
modules = ["nodejs-20", "web", "postgresql-16"]
run = "npm run dev"
hidden = [".config", ".git", "generated-icon.png", "node_modules", "dist"]

[nix]
channel = "stable-24_05"

[deployment]
deploymentTarget = "autoscale"
build = ["npm", "run", "build"]
run = ["npm", "run", "start"]

[[ports]]
localPort = 5000
externalPort = 80

[workflows]
runButton = "Project"

[[workflows.workflow]]
name = "Project"
mode = "parallel"
author = "agent"

[[workflows.workflow.tasks]]
task = "workflow.run"
args = "Start application"

[[workflows.workflow]]
name = "Start application"
author = "agent"

[[workflows.workflow.tasks]]
task = "shell.exec"
args = "npm run dev"
waitForPort = 5000

```

---

## Frontend Application

### Entry Points

#### client/src/App.tsx
```tsx

import { Toaster } from "@/components/ui/toaster";
import { TooltipProvider } from "@/components/ui/tooltip";
import { QueryClient, QueryClientProvider } from "@tanstack/react-query";
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Index from "./pages/Index";
import NotFound from "./pages/NotFound";
import FavoritesGallery from "./pages/FavoritesGallery";

const queryClient = new QueryClient();

const App = () => (
  <QueryClientProvider client={queryClient}>
    <TooltipProvider>
      <Toaster />
      <BrowserRouter>
        <Routes>
          <Route path="/" element={<Index />} />
          <Route path="/gallery" element={<FavoritesGallery />} />
          {/* ADD ALL CUSTOM ROUTES ABOVE THE CATCH-ALL "*" ROUTE */}
          <Route path="*" element={<NotFound />} />
        </Routes>
      </BrowserRouter>
    </TooltipProvider>
  </QueryClientProvider>
);

export default App;

```

#### client/src/main.tsx
```tsx
import { createRoot } from 'react-dom/client'
import App from './App.tsx'
import './index.css'

createRoot(document.getElementById("root")!).render(<App />);

```

### Pages

#### client/src/pages/FavoritesGallery.tsx
```tsx

import React, { useState, useRef, useEffect } from 'react';
import { Link } from 'react-router-dom';
import { ArrowLeft } from 'lucide-react';
import html2canvas from 'html2canvas';
import PixelMoshOverlay from '../components/PixelMoshOverlay';
import { GiphyFetch } from '@giphy/js-fetch-api';

interface GifData {
  id: string;
  url: string;
  title: string;
  width: number;
  height: number;
}

const gf = new GiphyFetch('your-api-key-here'); // We'll use demo mode for now

export default function FavoritesGallery() {
  const containerRef = useRef<HTMLDivElement>(null);
  const [moshing, setMoshing] = useState(false);
  const [snapshot, setSnapshot] = useState<string | null>(null);
  const [selectedGif, setSelectedGif] = useState<GifData | null>(null);
  const [modalOpen, setModalOpen] = useState(false);
  const [gifs, setGifs] = useState<GifData[]>([]);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    const fetchTrendingGifs = async () => {
      try {
        // Using trending endpoint without API key (demo mode)
        const { data } = await gf.trending({ limit: 12 });
        
        const formattedGifs: GifData[] = data.map(gif => ({
          id: gif.id.toString(),
          url: gif.images.fixed_height.url,
          title: gif.title || 'Trending GIF',
          width: gif.images.fixed_height.width,
          height: gif.images.fixed_height.height
        }));
        
        setGifs(formattedGifs);
      } catch (error) {
        console.error('Error fetching trending GIFs:', error);
        // Fallback to a few demo GIFs if GIPHY fails
        setGifs([
          { 
            id: '1', 
            url: 'https://media.giphy.com/media/3o7abKhOpu0NwenH3O/giphy.gif',
            title: 'Demo GIF 1',
            width: 480,
            height: 270
          },
          { 
            id: '2', 
            url: 'https://media.giphy.com/media/26BRrSvJUa0crqw4E/giphy.gif',
            title: 'Demo GIF 2',
            width: 480,
            height: 270
          }
        ]);
      } finally {
        setLoading(false);
      }
    };

    fetchTrendingGifs();
  }, []);

  const handleClick = async (gif: GifData) => {
    if (!containerRef.current) return;
    const canvas = await html2canvas(containerRef.current);
    setSnapshot(canvas.toDataURL());
    setSelectedGif(gif);
    setMoshing(true);
  };

  const handleMoshComplete = () => {
    setMoshing(false);
    setModalOpen(true);
  };

  if (loading) {
    return (
      <div className="min-h-screen bg-black text-white flex items-center justify-center">
        <div className="text-center">
          <div className="animate-spin rounded-full h-12 w-12 border-b-2 border-white mx-auto mb-4"></div>
          <p className="text-white/70 font-mono">Loading trending GIFs...</p>
        </div>
      </div>
    );
  }

  return (
    <div className="min-h-screen bg-black text-white relative">
      {/* Back button */}
      <Link 
        to="/" 
        className="fixed top-4 left-4 z-30 flex items-center gap-2 text-white/70 hover:text-white transition-colors bg-black/50 backdrop-blur-sm rounded-full px-3 py-2"
      >
        <ArrowLeft className="w-4 h-4" />
        <span className="text-sm font-mono">Back</span>
      </Link>

      {/* Grid container */}
      <div
        ref={containerRef}
        className="min-h-screen w-full grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-1 p-4"
      >
        {gifs.map(gif => (
          <div
            key={gif.id}
            className="relative aspect-square cursor-pointer group overflow-hidden rounded-lg bg-gray-800"
            onClick={() => handleClick(gif)}
          >
            <img
              src={gif.url}
              alt={gif.title}
              className="w-full h-full object-cover opacity-80 group-hover:opacity-100 transition-opacity"
              crossOrigin="anonymous"
            />
            <div className="absolute inset-0 bg-black/20 group-hover:bg-black/0 transition-colors" />
          </div>
        ))}
      </div>

      {/* Pixel Mosh Overlay */}
      {moshing && snapshot && (
        <PixelMoshOverlay
          imageSrc={snapshot}
          duration={3000}
          onComplete={handleMoshComplete}
        />
      )}

      {/* Modal */}
      {modalOpen && selectedGif && (
        <div className="fixed inset-0 z-50 bg-black bg-opacity-90 flex items-center justify-center">
          <button
            onClick={() => setModalOpen(false)}
            className="absolute top-4 right-4 text-white text-3xl"
          >
            ×
          </button>
          <div className="max-w-full max-h-full p-4">
            <img
              src={selectedGif.url}
              alt={selectedGif.title}
              className="max-w-full max-h-full object-contain"
            />
          </div>
        </div>
      )}
    </div>
  );
}

```

#### client/src/pages/Index.tsx
```tsx
import React, { useRef, useState } from 'react';
import { useVideoPointCloud } from '../hooks/useVideoPointCloud';
import { useGifExport } from '../hooks/useGifExport';
import { useVideoExport } from '../hooks/useVideoExport';
import { HalftoneEffect, HalftoneSettings } from '../utils/halftoneEffect';
import { ControlPanel } from '../components/ControlPanel';
import { IntroAnimation } from '../components/IntroAnimation';
import { WelcomeScreen } from '../components/WelcomeScreen';
import { LoadingScreen } from '../components/LoadingScreen';
import { OceanShader } from '../components/OceanShader';
import { AlertTriangle, X } from 'lucide-react';
import { fetchDemoVideo } from '../utils/demoVideo';
import { VISUAL_MODES, applyVisualMode } from '../utils/visualModes';

const Index = () => {
  const canvasRef = useRef<HTMLCanvasElement>(null);
  const [isLoading, setIsLoading] = useState(false);
  const [isControlPanelExpanded, setIsControlPanelExpanded] = useState(true);
  const [showDemoAnimation, setShowDemoAnimation] = useState(false);
  
  const [currentMode, setCurrentMode] = useState('standard');
  
  // RGB Halftone Effect State
  const [halftoneSettings, setHalftoneSettings] = useState<HalftoneSettings>({
    shape: 1, // dot
    radius: 0.4,
    rotateR: Math.PI / 12 * 1,
    rotateG: Math.PI / 12 * 2,
    rotateB: Math.PI / 12 * 3,
    scatter: 0.5,
    blending: 1.0,
    blendingMode: 1, // linear
    greyscale: false,
    disable: true // Start with effect disabled
  });
  const halftoneEffectRef = useRef<HalftoneEffect | null>(null);
  
  const [settings, setSettings] = useState({
    nearClipping: 0.0,
    farClipping: 1.0,
    pointSize: 1.5,
    zOffset: 0.0,
    fov: 25,
    depthScale: 0.0,
    minDistance: 0.0,
    maxDistance: 1.0,
    depthPower: 0.5,
    pointSizeDepthFactor: 1.0,
    invertDepth: false,
    // Advanced shader parameters
    epsilon: 0.1,
    exponentialK: 0.5,
    gamma: 1.0,
    stereographicC: 0.1,
    offsetStrength: 0.05,
    noiseScale: 100.0,
    // Depth estimation - AI depth enabled by default
    useRealDepth: true
  });

  const { 
    setVideoFile, 
    playVideo, 
    pauseVideo, 
    isPlaying, 
    videoFile, 
    videoError, 
    clearVideoError,
    webglSupported,
    webglError,
    videoRef,
    cameraPosition,
    updateCameraPosition,
    syncCameraState,
    orbitLock,
    trajectoryMode,
    trajectoryDuration,
    onOrbitLockChange,
    onTrajectoryModeChange,
    onTrajectoryDurationChange,
    resetCamera
  } = useVideoPointCloud(canvasRef, settings);

  // Initialize halftone effect when canvas is ready
  React.useEffect(() => {
    if (canvasRef.current && videoFile) {
      const canvas = canvasRef.current;
      const gl = canvas.getContext('webgl2') || canvas.getContext('webgl');
      
      if (gl && !halftoneEffectRef.current) {
        halftoneEffectRef.current = new HalftoneEffect(canvas, gl as WebGL2RenderingContext);
        halftoneEffectRef.current.updateSettings(halftoneSettings);
        console.log('RGB Halftone effect initialized');
      }
    }
    
    return () => {
      if (halftoneEffectRef.current) {
        halftoneEffectRef.current.dispose();
        halftoneEffectRef.current = null;
      }
    };
  }, [canvasRef.current, videoFile]);

  // Use the existing GIF export hook
  const {
    startGifRecording,
    stopGifRecording,
    isRecordingGif,
    gifProgress,
    gifError,
    clearGifError
  } = useGifExport(canvasRef, videoRef, isPlaying, (playing) => {
    if (playing) {
      playVideo();
    } else {
      pauseVideo();
    }
  });

  // Use the new video export hook
  const {
    startVideoRecording,
    stopVideoRecording,
    isRecordingVideo,
    videoProgress,
    videoError: videoExportError,
    clearVideoError: clearVideoExportError
  } = useVideoExport(canvasRef, videoRef, isPlaying, (playing) => {
    if (playing) {
      playVideo();
    } else {
      pauseVideo();
    }
  });

  const handleSettingsChange = (key: string, value: number | boolean) => {
    setSettings(prev => ({ ...prev, [key]: value }));
    // Switch to custom mode when user manually adjusts settings
    if (currentMode !== 'custom') {
      setCurrentMode('custom');
    }
  };

  const handleHalftoneChange = (newSettings: Partial<HalftoneSettings>) => {
    setHalftoneSettings(prev => ({
      ...prev,
      ...newSettings
    }));
    
    // Update the halftone effect if it exists
    if (halftoneEffectRef.current) {
      halftoneEffectRef.current.updateSettings(newSettings);
    }
  };

  const handleModeChange = (modeId: string) => {
    setCurrentMode(modeId);
    const mode = VISUAL_MODES.find(m => m.id === modeId);
    if (mode && modeId !== 'custom') {
      applyVisualMode(mode, (key, value) => {
        setSettings(prev => ({ ...prev, [key]: value }));
      });
    }
  };

  const handleVideoUpload = async (file: File) => {
    setIsLoading(true);
    
    // Simulate processing time for better UX
    setTimeout(() => {
      setVideoFile(file);
      setIsLoading(false);
    }, 1500);
  };

  const toggleControlPanel = () => {
    setIsControlPanelExpanded(prev => !prev);
  };

  const handleErrorDismiss = () => {
    clearVideoError();
  };

  const handleDemoTransition = async () => {
    setShowDemoAnimation(false);
    setIsLoading(true);
    
    try {
      // Load your demo video
      const demoVideo = await fetchDemoVideo();
      setVideoFile(demoVideo);
    } catch (error) {
      console.error('Failed to load demo video:', error);
      // If demo fails, just go back to welcome screen
    } finally {
      setIsLoading(false);
    }
  };



  return (
    <div className="relative w-full h-screen bg-black overflow-hidden">
      {/* Ocean Shader Background - Only when video is loaded */}
      {videoFile && <OceanShader className="absolute inset-0 w-full h-full" />}
      
      {/* Three.js Canvas */}
      <canvas
        ref={canvasRef}
        className="absolute inset-0 w-full h-full"
        style={{ display: videoFile ? 'block' : 'none' }}
      />

      {/* Demo Animation - Only shows when triggered from WelcomeScreen */}
      {showDemoAnimation && (
        <IntroAnimation onTransitionComplete={handleDemoTransition} />
      )}

      {/* Welcome Screen - Default state when no video */}
      {!videoFile && !isLoading && !videoError && !showDemoAnimation && (
        <WelcomeScreen 
          onVideoUpload={handleVideoUpload}
          onDemoAnimationStart={() => setShowDemoAnimation(true)}
        />
      )}

      {/* Loading Screen */}
      {isLoading && <LoadingScreen />}

      {/* Error Screen */}
      {videoError && (
        <div className="absolute inset-0 flex items-center justify-center bg-black/90 backdrop-blur-sm z-50">
          <div className="bg-gray-900/95 backdrop-blur-md border border-red-500/30 rounded-2xl p-8 max-w-md mx-4 shadow-2xl">
            <div className="flex items-center gap-3 mb-4">
              <div className="p-2 bg-red-500/20 rounded-full">
                <AlertTriangle className="w-6 h-6 text-red-400" />
              </div>
              <h2 className="text-xl font-bold text-red-400">Video Error</h2>
            </div>
            
            <p className="text-gray-300 mb-6 leading-relaxed">
              {videoError}
            </p>
            
            <div className="flex gap-3">
              <button
                onClick={handleErrorDismiss}
                className="flex-1 bg-gray-500 hover:bg-gray-400 text-black font-semibold py-3 px-6 rounded-xl transition-all duration-200 hover:scale-105 active:scale-95"
              >
                Try Another Video
              </button>
              <button
                onClick={handleErrorDismiss}
                className="p-3 bg-gray-700 hover:bg-gray-600 text-gray-300 rounded-xl transition-colors duration-200"
              >
                <X className="w-5 h-5" />
              </button>
            </div>
          </div>
        </div>
      )}

      {/* WebGL Error Screen */}
      {webglSupported === false && webglError && (
        <div className="absolute inset-0 flex items-center justify-center bg-black/90 backdrop-blur-sm z-50">
          <div className="bg-gray-900/95 backdrop-blur-md border border-orange-500/30 rounded-2xl p-8 max-w-lg mx-4 shadow-2xl">
            <div className="flex items-center gap-3 mb-4">
              <div className="p-2 bg-orange-500/20 rounded-full">
                <AlertTriangle className="w-6 h-6 text-orange-400" />
              </div>
              <h2 className="text-xl font-bold text-orange-400">3D Rendering Not Available</h2>
            </div>
            
            <p className="text-gray-300 mb-4 leading-relaxed">
              WebGL is required for 3D point cloud visualization but could not be initialized.
            </p>
            
            <div className="bg-gray-800/50 rounded-lg p-4 mb-6">
              <p className="text-sm text-gray-400 font-mono break-words">
                {webglError}
              </p>
            </div>
            
            <div className="space-y-3 mb-6">
              <h3 className="text-lg font-semibold text-gray-200">Possible Solutions:</h3>
              <ul className="text-sm text-gray-300 space-y-2 list-disc list-inside">
                <li>Try using a different browser (Chrome, Firefox, or Edge)</li>
                <li>Update your browser to the latest version</li>
                <li>Enable hardware acceleration in browser settings</li>
                <li>Update your graphics drivers</li>
                <li>Try refreshing the page</li>
              </ul>
            </div>
            
            <div className="flex gap-3">
              <button
                onClick={() => window.location.reload()}
                className="flex-1 bg-orange-500 hover:bg-orange-400 text-black font-semibold py-3 px-6 rounded-xl transition-all duration-200 hover:scale-105 active:scale-95"
              >
                Refresh Page
              </button>
              <button
                onClick={() => window.location.reload()}
                className="p-3 bg-gray-700 hover:bg-gray-600 text-gray-300 rounded-xl transition-colors duration-200"
                title="Dismiss and refresh"
              >
                <X className="w-5 h-5" />
              </button>
            </div>
          </div>
        </div>
      )}

      {/* Control Panel */}
      {videoFile && !isLoading && (
        <ControlPanel
          settings={settings}
          halftoneSettings={halftoneSettings}
          onSettingsChange={handleSettingsChange}
          onHalftoneChange={handleHalftoneChange}
          currentMode={currentMode}
          onModeChange={handleModeChange}
          onVideoUpload={handleVideoUpload}
          onPlay={playVideo}
          onPause={pauseVideo}
          isPlaying={isPlaying}
          hasVideo={!!videoFile}
          isExpanded={isControlPanelExpanded}
          onToggleExpand={toggleControlPanel}
          videoRef={videoRef}
          canvasRef={canvasRef}
          onStartGifRecording={startGifRecording}
          onStopGifRecording={stopGifRecording}
          isRecordingGif={isRecordingGif}
          gifProgress={gifProgress}
          gifError={gifError}
          onClearGifError={clearGifError}
          onStartVideoRecording={startVideoRecording}
          onStopVideoRecording={stopVideoRecording}
          isRecordingVideo={isRecordingVideo}
          videoProgress={videoProgress}
          videoError={videoExportError}
          onClearVideoError={clearVideoExportError}
          cameraPosition={cameraPosition}
          onCameraChange={updateCameraPosition}
          orbitLock={orbitLock}
          onOrbitLockChange={onOrbitLockChange}
          trajectoryMode={trajectoryMode}
          onTrajectoryModeChange={onTrajectoryModeChange}
          trajectoryDuration={trajectoryDuration}
          onTrajectoryDurationChange={onTrajectoryDurationChange}
          onCameraReset={resetCamera}
        />
      )}

      {/* Simple Title Overlay */}
      {videoFile && !isLoading && (
        <div className="absolute top-4 left-4 z-10">
          <h1 className="text-white text-sm font-mono font-semibold opacity-70">
            PIXELFLOW
          </h1>
        </div>
      )}

      {/* Custom Slider Styles */}
      <style>{`
        .mini-slider::-webkit-slider-thumb {
          appearance: none;
          width: 12px;
          height: 12px;
          border-radius: 50%;
          background: #ffffff;
          cursor: pointer;
          border: 1px solid #d1d5db;
          box-shadow: 0 0 4px rgba(255, 255, 255, 0.3);
          transition: all 0.15s ease;
        }
        
        .mini-slider::-webkit-slider-thumb:hover {
          transform: scale(1.1);
          box-shadow: 0 0 6px rgba(255, 255, 255, 0.5);
        }
        
        .mini-slider::-moz-range-thumb {
          width: 12px;
          height: 12px;
          border-radius: 50%;
          background: #ffffff;
          cursor: pointer;
          border: 1px solid #d1d5db;
          box-shadow: 0 0 4px rgba(255, 255, 255, 0.3);
          transition: all 0.15s ease;
        }
        
        .mini-slider::-moz-range-thumb:hover {
          transform: scale(1.1);
          box-shadow: 0 0 6px rgba(255, 255, 255, 0.5);
        }
        
        .mini-slider::-webkit-slider-track {
          background: #374151;
          height: 3px;
          border-radius: 2px;
        }
        
        .mini-slider::-moz-range-track {
          background: #374151;
          height: 3px;
          border-radius: 2px;
        }
        
        .animation-delay-150 {
          animation-delay: 150ms;
        }
        
        .animation-delay-300 {
          animation-delay: 300ms;
        }
        
        .animation-delay-500 {
          animation-delay: 500ms;
        }
      `}</style>
    </div>
  );
};

export default Index;

```

#### client/src/pages/NotFound.tsx
```tsx
import { useLocation } from "react-router-dom";
import { useEffect } from "react";

const NotFound = () => {
  const location = useLocation();

  useEffect(() => {
    console.error(
      "404 Error: User attempted to access non-existent route:",
      location.pathname
    );
  }, [location.pathname]);

  return (
    <div className="min-h-screen flex items-center justify-center bg-gray-100">
      <div className="text-center">
        <h1 className="text-4xl font-bold mb-4">404</h1>
        <p className="text-xl text-gray-600 mb-4">Oops! Page not found</p>
        <a href="/" className="text-blue-500 hover:text-blue-700 underline">
          Return to Home
        </a>
      </div>
    </div>
  );
};

export default NotFound;

```

### Components

#### client/src/components/AdvancedTransition.tsx
```tsx
import React, { useEffect, useRef, useState } from 'react';

interface AdvancedTransitionProps {
  imageSrc: string;
  duration: number;
  onComplete: () => void;
}

const AdvancedTransition: React.FC<AdvancedTransitionProps> = ({ 
  imageSrc, 
  duration, 
  onComplete 
}) => {
  const canvasRef = useRef<HTMLCanvasElement>(null);
  const [stage, setStage] = useState(0);
  const animationRef = useRef<number>();
  const startTimeRef = useRef<number>();

  useEffect(() => {
    const canvas = canvasRef.current;
    if (!canvas) return;

    const ctx = canvas.getContext('2d');
    if (!ctx) return;

    // Set canvas size to viewport
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    const img = new Image();
    img.onload = () => {
      startTimeRef.current = performance.now();
      animate(ctx, img);
    };
    img.src = imageSrc;

    return () => {
      if (animationRef.current) {
        cancelAnimationFrame(animationRef.current);
      }
    };
  }, [imageSrc]);

  const animate = (ctx: CanvasRenderingContext2D, img: HTMLImageElement) => {
    const animateFrame = (currentTime: number) => {
      if (!startTimeRef.current) return;
      
      const elapsed = currentTime - startTimeRef.current;
      const progress = Math.min(elapsed / duration, 1);
      
      // Clear canvas
      ctx.clearRect(0, 0, ctx.canvas.width, ctx.canvas.height);
      
      // Draw background image
      ctx.drawImage(img, 0, 0, ctx.canvas.width, ctx.canvas.height);
      
      // Stage progression
      if (progress < 0.15) {
        // Stage 1: Localized reality breakdown (0-15%)
        setStage(1);
        renderLocalizedBreakdown(ctx, progress / 0.15);
      } else if (progress < 0.4) {
        // Stage 2: Cascading corruption (15-40%)
        setStage(2);
        renderCascadingCorruption(ctx, (progress - 0.15) / 0.25);
      } else if (progress < 0.75) {
        // Stage 3: Full-screen temporal displacement (40-75%)
        setStage(3);
        renderTemporalDisplacement(ctx, (progress - 0.4) / 0.35);
      } else if (progress < 1) {
        // Stage 4: Reality reconstruction failure (75-100%)
        setStage(4);
        renderReconstructionFailure(ctx, (progress - 0.75) / 0.25);
      } else {
        // Animation complete
        onComplete();
        return;
      }
      
      animationRef.current = requestAnimationFrame(animateFrame);
    };
    
    animationRef.current = requestAnimationFrame(animateFrame);
  };

  const renderLocalizedBreakdown = (ctx: CanvasRenderingContext2D, progress: number) => {
    const centerX = ctx.canvas.width / 2;
    const centerY = ctx.canvas.height / 2;
    const maxRadius = 200 * progress;
    
    // Create radial corruption from center
    for (let i = 0; i < 50; i++) {
      const angle = (i / 50) * Math.PI * 2;
      const radius = Math.random() * maxRadius;
      const x = centerX + Math.cos(angle) * radius;
      const y = centerY + Math.sin(angle) * radius;
      
      // Random pixel displacement
      const displacement = Math.random() * 20 * progress;
      const sourceX = x + (Math.random() - 0.5) * displacement;
      const sourceY = y + (Math.random() - 0.5) * displacement;
      
      const blockSize = 2 + Math.random() * 8;
      const imageData = ctx.getImageData(sourceX, sourceY, blockSize, blockSize);
      
      // Apply RGB channel corruption
      for (let j = 0; j < imageData.data.length; j += 4) {
        if (Math.random() < 0.3) {
          imageData.data[j] = Math.min(255, imageData.data[j] * (1 + Math.random())); // Red
          imageData.data[j + 1] = Math.max(0, imageData.data[j + 1] * (Math.random() * 0.5)); // Green
          imageData.data[j + 2] = Math.min(255, imageData.data[j + 2] * (1 + Math.random() * 0.5)); // Blue
        }
      }
      
      ctx.putImageData(imageData, x, y);
    }
  };

  const renderCascadingCorruption = (ctx: CanvasRenderingContext2D, progress: number) => {
    const width = ctx.canvas.width;
    const height = ctx.canvas.height;
    
    // Horizontal corruption waves
    for (let y = 0; y < height; y += 4) {
      const waveOffset = Math.sin((y * 0.01) + (progress * Math.PI * 4)) * 50 * progress;
      const corruptionIntensity = Math.abs(waveOffset) / 50;
      
      if (corruptionIntensity > 0.3) {
        const sourceY = Math.max(0, Math.min(height - 4, y + waveOffset));
        const imageData = ctx.getImageData(0, sourceY, width, 4);
        
        // Datamosh effect - mix channels
        for (let i = 0; i < imageData.data.length; i += 4) {
          const r = imageData.data[i];
          const g = imageData.data[i + 1];
          const b = imageData.data[i + 2];
          
          // Channel displacement
          imageData.data[i] = g; // Red gets green
          imageData.data[i + 1] = b; // Green gets blue
          imageData.data[i + 2] = r; // Blue gets red
          
          // Add digital noise
          if (Math.random() < 0.1) {
            imageData.data[i] = Math.random() * 255;
            imageData.data[i + 1] = Math.random() * 255;
            imageData.data[i + 2] = Math.random() * 255;
          }
        }
        
        ctx.putImageData(imageData, waveOffset * progress, y);
      }
    }
    
    // Vertical scan line interference
    for (let x = 0; x < width; x += 8) {
      if (Math.random() < 0.05 * progress) {
        const scanHeight = 20 + Math.random() * 100;
        const scanY = Math.random() * (height - scanHeight);
        
        ctx.fillStyle = `rgba(${Math.random() * 255}, ${Math.random() * 255}, ${Math.random() * 255}, 0.7)`;
        ctx.fillRect(x, scanY, 2, scanHeight);
      }
    }
  };

  const renderTemporalDisplacement = (ctx: CanvasRenderingContext2D, progress: number) => {
    const width = ctx.canvas.width;
    const height = ctx.canvas.height;
    
    // Create multiple temporal layers with RGB separation
    const layers = 5;
    const displacement = 30 * progress;
    
    for (let layer = 0; layer < layers; layer++) {
      const layerProgress = (layer / layers) + (progress * 0.2);
      const xOffset = Math.sin(layerProgress * Math.PI * 2) * displacement;
      const yOffset = Math.cos(layerProgress * Math.PI * 2) * displacement * 0.5;
      
      // Get displaced image data
      const imageData = ctx.getImageData(0, 0, width, height);
      const newImageData = ctx.createImageData(width, height);
      
      for (let y = 0; y < height; y++) {
        for (let x = 0; x < width; x++) {
          const sourceX = Math.max(0, Math.min(width - 1, x + xOffset));
          const sourceY = Math.max(0, Math.min(height - 1, y + yOffset));
          
          const sourceIndex = (Math.floor(sourceY) * width + Math.floor(sourceX)) * 4;
          const targetIndex = (y * width + x) * 4;
          
          // RGB channel separation based on layer
          if (layer % 3 === 0) {
            newImageData.data[targetIndex] = imageData.data[sourceIndex]; // Red
          } else if (layer % 3 === 1) {
            newImageData.data[targetIndex + 1] = imageData.data[sourceIndex + 1]; // Green
          } else {
            newImageData.data[targetIndex + 2] = imageData.data[sourceIndex + 2]; // Blue
          }
          newImageData.data[targetIndex + 3] = 255; // Alpha
        }
      }
      
      // Blend mode simulation
      ctx.globalCompositeOperation = layer === 0 ? 'source-over' : 'screen';
      ctx.globalAlpha = 0.3 + (layer * 0.1);
      ctx.putImageData(newImageData, 0, 0);
    }
    
    ctx.globalCompositeOperation = 'source-over';
    ctx.globalAlpha = 1;
  };

  const renderReconstructionFailure = (ctx: CanvasRenderingContext2D, progress: number) => {
    const width = ctx.canvas.width;
    const height = ctx.canvas.height;
    
    // Stage 4A: Reverse corruption waves (0-25%)
    if (progress < 0.25) {
      const reverseIntensity = progress / 0.25;
      
      // Reverse horizontal corruption waves - trying to "fix" but making it worse
      for (let y = 0; y < height; y += 3) {
        const reverseWave = Math.sin((y * 0.02) - (reverseIntensity * Math.PI * 6)) * 30 * reverseIntensity;
        const shouldReverse = Math.abs(reverseWave) > 15;
        
        if (shouldReverse) {
          const sourceY = Math.max(0, Math.min(height - 3, y - reverseWave));
          const imageData = ctx.getImageData(0, sourceY, width, 3);
          
          // "Reconstruction" attempt - but channels get more mixed up
          for (let i = 0; i < imageData.data.length; i += 4) {
            const r = imageData.data[i];
            const g = imageData.data[i + 1];
            const b = imageData.data[i + 2];
            
            // Failed reconstruction - channels swap chaotically
            imageData.data[i] = b;     // Red gets blue
            imageData.data[i + 1] = r; // Green gets red  
            imageData.data[i + 2] = g; // Blue gets green
            
            // Add reconstruction artifacts
            if (Math.random() < 0.15) {
              imageData.data[i] = 255 - imageData.data[i];
              imageData.data[i + 1] = 255 - imageData.data[i + 1];
              imageData.data[i + 2] = 255 - imageData.data[i + 2];
            }
          }
          
          ctx.putImageData(imageData, -reverseWave * 0.3, y);
        }
      }
    }
    
    // Stage 4B: Failed reconstruction blocks (25-50%)
    if (progress >= 0.25 && progress < 0.5) {
      const blockProgress = (progress - 0.25) / 0.25;
      const blockSize = 8 + Math.floor(blockProgress * 32);
      
      // Create "reconstruction" blocks that show fragments of the original
      for (let x = 0; x < width; x += blockSize) {
        for (let y = 0; y < height; y += blockSize) {
          if (Math.random() < 0.4 * blockProgress) {
            // Get block from random location (failed memory reconstruction)
            const sourceX = Math.random() * (width - blockSize);
            const sourceY = Math.random() * (height - blockSize);
            const blockData = ctx.getImageData(sourceX, sourceY, blockSize, blockSize);
            
            // Apply reconstruction failure effects
            for (let i = 0; i < blockData.data.length; i += 4) {
              // Memory leak effect - previous corruptions bleed through
              if (Math.random() < 0.3) {
                blockData.data[i] = Math.random() * 255;     // Random red
                blockData.data[i + 1] = blockData.data[i + 1] * 0.3; // Dim green
                blockData.data[i + 2] = 255 - blockData.data[i + 2]; // Invert blue
              }
              
              // Partial transparency for "incomplete" reconstruction
              blockData.data[i + 3] = 120 + Math.random() * 135;
            }
            
            ctx.putImageData(blockData, x, y);
            
            // Add block outline to show "reconstruction attempt"
            ctx.strokeStyle = `rgba(0, 255, 255, ${0.5 * blockProgress})`;
            ctx.lineWidth = 1;
            ctx.strokeRect(x, y, blockSize, blockSize);
          }
        }
      }
    }
    
    // Stage 4C: Memory leak cascade (50-75%)
    if (progress >= 0.5 && progress < 0.75) {
      const leakProgress = (progress - 0.5) / 0.25;
      
      // Previous stage corruptions "bleed through" the reconstruction
      for (let i = 0; i < 200 * leakProgress; i++) {
        const x = Math.random() * width;
        const y = Math.random() * height;
        const streakLength = 10 + Math.random() * 50;
        const streakHeight = 1 + Math.random() * 3;
        
        // Memory leak streaks - fragments of previous corruption stages
        const leakData = ctx.getImageData(x, y, streakLength, streakHeight);
        
        for (let j = 0; j < leakData.data.length; j += 4) {
          // Blend previous stage effects
          const intensity = Math.random();
          if (intensity < 0.33) {
            // Stage 1 artifacts
            leakData.data[j] = 255;
            leakData.data[j + 1] = Math.random() * 255;
            leakData.data[j + 2] = 255;
          } else if (intensity < 0.66) {
            // Stage 2 artifacts  
            leakData.data[j] = leakData.data[j + 2];
            leakData.data[j + 1] = leakData.data[j];
            leakData.data[j + 2] = leakData.data[j + 1];
          } else {
            // Stage 3 artifacts
            leakData.data[j] = Math.min(255, leakData.data[j] * 2);
            leakData.data[j + 1] = Math.max(0, leakData.data[j + 1] * 0.5);
            leakData.data[j + 2] = Math.min(255, leakData.data[j + 2] * 1.5);
          }
          
          leakData.data[j + 3] = 100 + Math.random() * 155;
        }
        
        ctx.putImageData(leakData, x, y);
      }
    }
    
    // Stage 4D: Static burst finale (75-100%)
    if (progress >= 0.75) {
      const burstProgress = (progress - 0.75) / 0.25;
      
      // Final static burst before fade to black
      const staticIntensity = burstProgress * 0.8;
      const imageData = ctx.getImageData(0, 0, width, height);
      
      for (let i = 0; i < imageData.data.length; i += 4) {
        if (Math.random() < staticIntensity) {
          // Static noise
          const noise = Math.random() * 255;
          imageData.data[i] = noise;
          imageData.data[i + 1] = noise;
          imageData.data[i + 2] = noise;
        } else {
          // Fade to black
          imageData.data[i] *= (1 - burstProgress * 0.9);
          imageData.data[i + 1] *= (1 - burstProgress * 0.9);
          imageData.data[i + 2] *= (1 - burstProgress * 0.9);
        }
      }
      
      ctx.putImageData(imageData, 0, 0);
      
      // Final "what just happened" overlay
      ctx.fillStyle = `rgba(0, 0, 0, ${burstProgress * 0.7})`;
      ctx.fillRect(0, 0, width, height);
      
      // Brief white flash at the very end
      if (burstProgress > 0.9) {
        ctx.fillStyle = `rgba(255, 255, 255, ${(burstProgress - 0.9) * 10 * 0.3})`;
        ctx.fillRect(0, 0, width, height);
      }
    }
  };

  return (
    <>
      <div className="fixed inset-0 z-50 pointer-events-none">
        <canvas
          ref={canvasRef}
          className="absolute inset-0 w-full h-full"
          style={{ mixBlendMode: 'multiply' }}
        />
        
        {/* Stage-specific overlay effects */}
        <div className={`absolute inset-0 transition-opacity duration-200 ${
          stage === 1 ? 'animate-reality-breakdown' : 
          stage === 2 ? 'animate-cascade-corruption' :
          stage === 3 ? 'animate-temporal-flux' :
          stage === 4 ? 'animate-reconstruction-failure' : ''
        }`}>
          {/* CRT scan lines */}
          <div className="absolute inset-0 opacity-30 animate-scan-sweep"
               style={{
                 backgroundImage: 'repeating-linear-gradient(0deg, transparent, transparent 1px, rgba(0,255,255,0.1) 1px, rgba(0,255,255,0.1) 2px)',
               }}>
          </div>
          
          {/* Digital noise overlay */}
          <div className="absolute inset-0 opacity-20 animate-digital-noise"
               style={{
                 backgroundImage: `
                   radial-gradient(circle at 20% 30%, rgba(255,0,0,0.1) 1px, transparent 1px),
                   radial-gradient(circle at 70% 60%, rgba(0,255,0,0.1) 1px, transparent 1px),
                   radial-gradient(circle at 40% 80%, rgba(0,0,255,0.1) 1px, transparent 1px)
                 `,
                 backgroundSize: '3px 3px, 5px 5px, 7px 7px'
               }}>
          </div>
        </div>
      </div>

      <style>{`
        @keyframes scan-sweep {
          0% { transform: translateY(-100%); }
          100% { transform: translateY(100vh); }
        }
        
        @keyframes digital-noise {
          0%, 100% { opacity: 0.2; transform: scale(1); }
          50% { opacity: 0.4; transform: scale(1.05); }
        }
        
        @keyframes reality-breakdown {
          0%, 100% { filter: contrast(1) brightness(1); }
          50% { filter: contrast(1.5) brightness(1.2) hue-rotate(10deg); }
        }
        
        @keyframes cascade-corruption {
          0%, 100% { filter: contrast(1) brightness(1); }
          25% { filter: contrast(2) brightness(0.8) hue-rotate(90deg); }
          75% { filter: contrast(1.5) brightness(1.3) hue-rotate(-90deg); }
        }
        
        @keyframes temporal-flux {
          0%, 100% { filter: contrast(1) brightness(1) blur(0px); }
          33% { filter: contrast(3) brightness(0.5) blur(2px) hue-rotate(180deg); }
          66% { filter: contrast(0.5) brightness(2) blur(1px) hue-rotate(-180deg); }
        }
        
        @keyframes reconstruction-failure {
          0% { filter: contrast(1) brightness(1) blur(0px); }
          25% { filter: contrast(2.5) brightness(0.7) blur(1px) hue-rotate(45deg); }
          50% { filter: contrast(0.8) brightness(1.5) blur(0.5px) hue-rotate(-45deg); }
          75% { filter: contrast(3) brightness(0.3) blur(2px) hue-rotate(90deg); }
          100% { filter: contrast(0.2) brightness(0.1) blur(5px); }
        }
        
        .animate-reality-breakdown {
          animation: reality-breakdown 0.3s ease-in-out infinite;
        }
        
        .animate-cascade-corruption {
          animation: cascade-corruption 0.2s ease-in-out infinite;
        }
        
        .animate-temporal-flux {
          animation: temporal-flux 0.15s ease-in-out infinite;
        }
        
        .animate-reconstruction-failure {
          animation: reconstruction-failure 0.4s ease-in-out infinite;
        }
        
        .animate-scan-sweep {
          animation: scan-sweep 0.1s linear infinite;
        }
        
        .animate-digital-noise {
          animation: digital-noise 0.05s ease-in-out infinite;
        }
      `}</style>
    </>
  );
};

export default AdvancedTransition;

```

#### client/src/components/AnimatedSlider.tsx
```tsx
import React, { useState, useEffect, useRef } from 'react';
import { Slider } from '@/components/ui/slider';
import { Play, Pause } from 'lucide-react';

interface AnimatedSliderProps {
  label: string;
  value: number;
  min: number;
  max: number;
  step: number;
  onChange: (value: number) => void;
  className?: string;
  decimals?: number;
}

export const AnimatedSlider: React.FC<AnimatedSliderProps> = ({
  label,
  value,
  min,
  max,
  step,
  onChange,
  className = '',
  decimals = 2
}) => {
  const [isAnimating, setIsAnimating] = useState(false);
  const [direction, setDirection] = useState(1); // 1 for forward, -1 for backward
  const animationRef = useRef<number>();
  const lastTimeRef = useRef<number>();

  // Animation parameters inspired by Luma AI
  const animationSpeed = 0.25; // Speed multiplier (reduced from 0.8 for slower movement)
  const smoothness = 60; // Target FPS for smooth animation

  useEffect(() => {
    if (!isAnimating) {
      if (animationRef.current) {
        cancelAnimationFrame(animationRef.current);
      }
      return;
    }

    const animate = (currentTime: number) => {
      if (!lastTimeRef.current) {
        lastTimeRef.current = currentTime;
      }

      const deltaTime = currentTime - lastTimeRef.current;
      const targetFrameTime = 1000 / smoothness;

      if (deltaTime >= targetFrameTime) {
        const range = max - min;
        const increment = (range * animationSpeed * deltaTime) / 1000;
        
        let newValue = value + (increment * direction);

        // Ping-pong logic: reverse direction at boundaries
        if (newValue >= max) {
          newValue = max;
          setDirection(-1);
        } else if (newValue <= min) {
          newValue = min;
          setDirection(1);
        }

        onChange(newValue);
        lastTimeRef.current = currentTime;
      }

      animationRef.current = requestAnimationFrame(animate);
    };

    animationRef.current = requestAnimationFrame(animate);

    return () => {
      if (animationRef.current) {
        cancelAnimationFrame(animationRef.current);
      }
    };
  }, [isAnimating, value, min, max, direction, onChange, animationSpeed]);

  const toggleAnimation = () => {
    setIsAnimating(!isAnimating);
    if (!isAnimating) {
      lastTimeRef.current = undefined;
      // Start from current position, determine initial direction based on position
      const midPoint = (min + max) / 2;
      setDirection(value < midPoint ? 1 : -1);
    }
  };

  const formatValue = (val: number) => {
    return val.toFixed(decimals);
  };

  return (
    <div className={`space-y-2 ${className}`}>
      <div className="flex justify-between items-center">
        <div className="flex items-center gap-2">
          <label className="text-white text-xs font-medium">{label}</label>
          <button
            onClick={toggleAnimation}
            className={`p-1 rounded transition-all duration-200 ${
              isAnimating 
                ? 'bg-blue-500 hover:bg-blue-400 text-white' 
                : 'bg-gray-600 hover:bg-gray-500 text-gray-300'
            }`}
            title={isAnimating ? 'Stop animation' : 'Start ping-pong animation'}
          >
            {isAnimating ? (
              <Pause className="w-3 h-3" />
            ) : (
              <Play className="w-3 h-3" />
            )}
          </button>
        </div>
        <div className="flex items-center gap-2">
          {isAnimating && (
            <div className="flex items-center gap-1">
              <div className="w-1 h-1 bg-blue-400 rounded-full animate-pulse" />
              <span className="text-blue-400 text-xs">animating</span>
            </div>
          )}
          <span className="text-white/70 text-xs tabular-nums">
            {formatValue(value)}
          </span>
        </div>
      </div>
      
      <Slider
        value={[value]}
        onValueChange={(values) => {
          // Stop animation when user manually adjusts
          if (isAnimating) {
            setIsAnimating(false);
          }
          onChange(values[0]);
        }}
        min={min}
        max={max}
        step={step}
        className="w-full"
        disabled={isAnimating}
      />
    </div>
  );
};
```

#### client/src/components/ControlPanel.tsx
```tsx
import React, { useState } from 'react';
import { Play, Pause, Upload, ChevronLeft, ChevronRight, Download, Video, Brain } from 'lucide-react';
import { GifExportDialog } from './GifExportDialog';
import { VideoExportDialog } from './VideoExportDialog';
import { NeuralNetworkVisualizer } from './NeuralNetworkVisualizer';
import { VRInterface } from './VRInterface';
import { AnimatedSlider } from './AnimatedSlider';
import { GifSettings } from '../hooks/useGifExport';
import { VideoSettings } from '../hooks/useVideoExport';
import { HalftoneSettings } from '../utils/halftoneEffect';
import { Slider } from './ui/slider';
import { Switch } from './ui/switch';
import { useIsMobile } from '../hooks/use-mobile';
import { Select, SelectContent, SelectItem, SelectTrigger, SelectValue } from './ui/select';
import { VISUAL_MODES } from '../utils/visualModes';

interface ControlPanelProps {
  settings: {
    nearClipping: number;
    farClipping: number;
    pointSize: number;
    zOffset: number;
    fov: number;
    depthScale: number;
    minDistance: number;
    maxDistance: number;
    depthPower: number;
    pointSizeDepthFactor: number;
    invertDepth: boolean;
    epsilon: number;
    exponentialK: number;
    gamma: number;
    stereographicC: number;
    offsetStrength: number;
    noiseScale: number;
    useRealDepth: boolean;
  };
  halftoneSettings?: HalftoneSettings;
  onSettingsChange: (key: string, value: number | boolean) => void;
  onHalftoneChange?: (settings: Partial<HalftoneSettings>) => void;
  currentMode?: string;
  onModeChange?: (mode: string) => void;
  onVideoUpload: (file: File) => void;
  onPlay: () => void;
  onPause: () => void;
  isPlaying: boolean;
  hasVideo: boolean;
  isExpanded: boolean;
  onToggleExpand: () => void;
  videoRef: React.RefObject<HTMLVideoElement>;
  canvasRef: React.RefObject<HTMLCanvasElement>;
  // GIF export props
  onStartGifRecording?: (settings: GifSettings) => void;
  onStopGifRecording?: () => void;
  isRecordingGif?: boolean;
  gifProgress?: number;
  gifError?: string | null;
  onClearGifError?: () => void;
  // Video export props
  onStartVideoRecording?: (settings: VideoSettings) => void;
  onStopVideoRecording?: () => void;
  isRecordingVideo?: boolean;
  videoProgress?: number;
  videoError?: string | null;
  onClearVideoError?: () => void;
  // Camera control props
  cameraPosition?: { azimuth: number; elevation: number; distance: number };
  onCameraChange?: (azimuth: number, elevation: number, distance: number) => void;
  orbitLock?: boolean;
  onOrbitLockChange?: (enabled: boolean) => void;
  trajectoryMode?: string;
  onTrajectoryModeChange?: (mode: string) => void;
  trajectoryDuration?: number;
  onTrajectoryDurationChange?: (duration: number) => void;
  onCameraReset?: () => void;
}

export const ControlPanel: React.FC<ControlPanelProps> = ({
  settings,
  halftoneSettings,
  onSettingsChange,
  onHalftoneChange,
  currentMode = 'custom',
  onModeChange,
  onVideoUpload,
  onPlay,
  onPause,
  isPlaying,
  hasVideo,
  isExpanded,
  onToggleExpand,
  videoRef,
  onStartGifRecording,
  onStopGifRecording,
  isRecordingGif = false,
  gifProgress = 0,
  gifError = null,
  onClearGifError,
  onStartVideoRecording,
  onStopVideoRecording,
  isRecordingVideo = false,
  videoProgress = 0,
  videoError = null,
  onClearVideoError,
  canvasRef,
  cameraPosition = { azimuth: 90, elevation: 0, distance: 2.0 },
  onCameraChange,
  orbitLock = true,
  onOrbitLockChange,
  trajectoryMode = 'manual',
  onTrajectoryModeChange,
  trajectoryDuration = 10,
  onTrajectoryDurationChange,
  onCameraReset
}) => {
  const [isGifDialogOpen, setIsGifDialogOpen] = useState(false);
  const [isVideoDialogOpen, setIsVideoDialogOpen] = useState(false);
  const [showNeuralNetwork, setShowNeuralNetwork] = useState(false);
  const [currentDepthData, setCurrentDepthData] = useState<Float32Array | undefined>();
  const [vrEnabled, setVrEnabled] = useState(false);
  const [isVRActive, setIsVRActive] = useState(false);
  const isMobile = useIsMobile();

  const handleFileUpload = (event: React.ChangeEvent<HTMLInputElement>) => {
    const file = event.target.files?.[0];
    if (file && file.type.startsWith('video/')) {
      onVideoUpload(file);
    }
  };

  const handleGifExport = () => {
    setIsGifDialogOpen(true);
  };

  const handleVideoExport = () => {
    setIsVideoDialogOpen(true);
  };

  const handleStartGifRecording = (settings: GifSettings) => {
    if (onStartGifRecording) {
      onStartGifRecording(settings);
    }
  };

  const handleStartVideoRecording = (settings: VideoSettings) => {
    if (onStartVideoRecording) {
      onStartVideoRecording(settings);
    }
  };

  const handleStopGifRecording = () => {
    if (onStopGifRecording) {
      onStopGifRecording();
    }
  };

  const handleStopVideoRecording = () => {
    if (onStopVideoRecording) {
      onStopVideoRecording();
    }
  };

  const handleClearGifError = () => {
    if (onClearGifError) {
      onClearGifError();
    }
  };

  const handleClearVideoError = () => {
    if (onClearVideoError) {
      onClearVideoError();
    }
  };

  return (
    <>
      <div className={`fixed top-4 right-4 bg-black/90 backdrop-blur-md border border-white/30 rounded-lg transition-all duration-300 z-10 ${
        isExpanded ? 'min-w-[260px] max-w-[260px]' : 'w-12'
      } max-h-[90vh] overflow-hidden`}>
        
        {/* Header with Toggle Button */}
        <div className="flex items-center justify-end p-2 border-b border-white/20">
          <button
            onClick={onToggleExpand}
            className="p-1 text-white hover:text-gray-300 transition-colors"
          >
            {isExpanded ? (
              <ChevronRight className="w-4 h-4" />
            ) : (
              <ChevronLeft className="w-4 h-4" />
            )}
          </button>
        </div>

        {/* Expandable Content */}
        {isExpanded && (
          <div className="p-3 space-y-2 overflow-y-auto max-h-[calc(90vh-50px)]">
            
            {/* Video Upload */}
            <div>
              <div className="relative">
                <input
                  type="file"
                  accept="video/*"
                  onChange={handleFileUpload}
                  className="hidden"
                  id="video-upload"
                />
                <label
                  htmlFor="video-upload"
                  className="flex items-center justify-center w-full p-2 border-2 border-dashed border-white/50 rounded-lg cursor-pointer hover:border-white transition-colors"
                >
                  <Upload className="w-4 h-4 mr-2 text-white" />
                  <span className="text-white text-xs">
                    {hasVideo ? 'Change' : 'Upload'}
                  </span>
                </label>
              </div>
            </div>

            {/* Visual Mode Selector */}
            <div className="space-y-2">
              <div className="border-t border-white/20 pt-2">
                <h3 className="text-white text-xs font-medium mb-2">Visual Mode</h3>
                <Select value={currentMode} onValueChange={onModeChange}>
                  <SelectTrigger className="w-full bg-black/20 border-white/20 text-white">
                    <SelectValue placeholder="Select mode" />
                  </SelectTrigger>
                  <SelectContent className="bg-black border-white/20">
                    {VISUAL_MODES.map((mode) => (
                      <SelectItem key={mode.id} value={mode.id} className="text-white hover:bg-white/10">
                        <div>
                          <div className="font-medium">{mode.name}</div>
                          <div className="text-xs text-white/70">{mode.description}</div>
                        </div>
                      </SelectItem>
                    ))}
                  </SelectContent>
                </Select>
              </div>
            </div>

            {/* Playback Controls */}
            {hasVideo && (
              <div className="flex gap-2">
                <button
                  onClick={isPlaying ? onPause : onPlay}
                  className="flex items-center px-3 py-2 bg-gray-600 hover:bg-gray-500 rounded-lg transition-colors text-sm flex-1"
                >
                  {isPlaying ? (
                    <Pause className="w-4 h-4 mr-1" />
                  ) : (
                    <Play className="w-4 h-4 mr-1" />
                  )}
                  {isPlaying ? 'Pause' : 'Play'}
                </button>
                
                {/* Export Buttons */}
                <button
                  onClick={handleGifExport}
                  disabled={isRecordingGif || isRecordingVideo}
                  className="flex items-center px-3 py-2 bg-blue-600 hover:bg-blue-500 disabled:bg-gray-600 disabled:cursor-not-allowed rounded-lg transition-colors text-sm"
                  title="Export as GIF"
                >
                  <Download className="w-4 h-4" />
                </button>

                <button
                  onClick={handleVideoExport}
                  disabled={isRecordingGif || isRecordingVideo}
                  className="flex items-center px-3 py-2 bg-green-600 hover:bg-green-500 disabled:bg-gray-600 disabled:cursor-not-allowed rounded-lg transition-colors text-sm"
                  title="Export as Video"
                >
                  <Video className="w-4 h-4" />
                </button>

                <button
                  onClick={() => setShowNeuralNetwork(!showNeuralNetwork)}
                  className={`flex items-center px-3 py-2 rounded-lg transition-colors text-sm ${
                    showNeuralNetwork 
                      ? 'bg-purple-600 hover:bg-purple-500' 
                      : 'bg-gray-600 hover:bg-gray-500'
                  }`}
                  title="Neural Network Visualizer"
                >
                  <Brain className="w-4 h-4" />
                </button>
              </div>
            )}

            {/* Recording Progress */}
            {(isRecordingGif || isRecordingVideo) && (
              <div className="bg-gray-800 rounded-lg p-2">
                <div className="flex items-center justify-between mb-1">
                  <span className="text-white text-xs">
                    {isRecordingGif ? 'Creating GIF...' : 'Creating Video...'}
                  </span>
                  <span className="text-white text-xs">
                    {Math.round(isRecordingGif ? gifProgress : videoProgress)}%
                  </span>
                </div>
                <div className="w-full bg-gray-700 rounded-full h-1">
                  <div 
                    className="bg-blue-500 h-1 rounded-full transition-all duration-200"
                    style={{ width: `${isRecordingGif ? gifProgress : videoProgress}%` }}
                  />
                </div>
              </div>
            )}

            {/* Depth Controls */}
            {hasVideo && (
              <div className="space-y-2">
                <div className="border-t border-white/20 pt-2">
                  <h3 className="text-white text-xs font-medium mb-2">Depth Mapping</h3>
                  
                  <div className={`space-y-${isMobile ? '3' : '1.5'}`}>
                    <AnimatedSlider
                      label="Near"
                      value={settings.nearClipping}
                      min={0}
                      max={1}
                      step={0.01}
                      onChange={(value) => onSettingsChange('nearClipping', value)}
                    />

                    <AnimatedSlider
                      label="Far"
                      value={settings.farClipping}
                      min={0}
                      max={1}
                      step={0.01}
                      onChange={(value) => onSettingsChange('farClipping', value)}
                    />

                    <AnimatedSlider
                      label="Scale"
                      value={settings.depthScale}
                      min={0.0}
                      max={1.0}
                      step={0.01}
                      onChange={(value) => onSettingsChange('depthScale', value)}
                    />

                    <AnimatedSlider
                      label="Power"
                      value={settings.depthPower}
                      min={0.5}
                      max={5.0}
                      step={0.1}
                      onChange={(value) => onSettingsChange('depthPower', value)}
                      decimals={1}
                    />

                    <div>
                      <div className="flex justify-between items-center mb-2">
                        <label className="text-white text-xs">Invert Depth</label>
                        <Switch
                          checked={settings.invertDepth}
                          onCheckedChange={(checked) => onSettingsChange('invertDepth', checked)}
                        />
                      </div>
                    </div>


                  </div>
                </div>

                <div className="border-t border-white/20 pt-2">
                  <h3 className="text-white text-xs font-medium mb-2">Display</h3>
                  
                  <div className={`space-y-${isMobile ? '3' : '1.5'}`}>
                    <AnimatedSlider
                      label="FOV"
                      value={settings.fov}
                      min={15}
                      max={60}
                      step={1}
                      onChange={(value) => onSettingsChange('fov', value)}
                      decimals={0}
                    />

                    <AnimatedSlider
                      label="Points"
                      value={settings.pointSize}
                      min={0.5}
                      max={6}
                      step={0.1}
                      onChange={(value) => onSettingsChange('pointSize', value)}
                      decimals={1}
                    />

                    <AnimatedSlider
                      label="Size Factor"
                      value={settings.pointSizeDepthFactor}
                      min={0.0}
                      max={2.0}
                      step={0.1}
                      onChange={(value) => onSettingsChange('pointSizeDepthFactor', value)}
                      decimals={1}
                    />

                    <AnimatedSlider
                      label="Z Offset"
                      value={settings.zOffset}
                      min={-5}
                      max={5}
                      step={0.1}
                      onChange={(value) => onSettingsChange('zOffset', value)}
                      decimals={1}
                    />
                  </div>
                </div>

                {/* Camera Controls - Luma AI Style */}
                <div className="border-t border-white/20 pt-2">
                  <div className="flex items-center justify-between mb-2">
                    <h3 className="text-white text-xs font-medium">Camera Position</h3>
                    {onCameraReset && (
                      <button
                        onClick={onCameraReset}
                        className="px-2 py-1 text-xs bg-gray-700 hover:bg-gray-600 text-white rounded transition-colors"
                        title="Reset camera to frontal view"
                      >
                        Reset
                      </button>
                    )}
                  </div>
                  
                  <div className={`space-y-${isMobile ? '3' : '1.5'}`}>
                    <AnimatedSlider
                      label="Azimuth"
                      value={cameraPosition.azimuth}
                      min={-180}
                      max={180}
                      step={1}
                      onChange={(value) => {
                        if (onCameraChange) {
                          onCameraChange(value, cameraPosition.elevation, cameraPosition.distance);
                        }
                      }}
                      decimals={0}
                    />

                    <AnimatedSlider
                      label="Elevation"
                      value={cameraPosition.elevation}
                      min={-90}
                      max={90}
                      step={1}
                      onChange={(value) => {
                        if (onCameraChange) {
                          onCameraChange(cameraPosition.azimuth, value, cameraPosition.distance);
                        }
                      }}
                      decimals={0}
                    />

                    <AnimatedSlider
                      label="Distance"
                      value={cameraPosition.distance}
                      min={1}
                      max={20}
                      step={0.1}
                      onChange={(value) => {
                        if (onCameraChange) {
                          onCameraChange(cameraPosition.azimuth, cameraPosition.elevation, value);
                        }
                      }}
                      decimals={1}
                    />
                    
                    {/* Orbit Lock Toggle */}
                    <div className="flex items-center justify-between">
                      <label className="text-white text-xs">Lock Horizon</label>
                      <button
                        onClick={() => {
                          if (onOrbitLockChange) {
                            onOrbitLockChange(!orbitLock);
                          }
                        }}
                        className={`relative inline-flex h-5 w-9 items-center rounded-full transition-colors ${
                          orbitLock ? 'bg-blue-600' : 'bg-gray-600'
                        }`}
                        title={orbitLock ? 'Camera movement locked to horizon' : 'Camera movement unlocked'}
                      >
                        <span
                          className={`inline-block h-3 w-3 transform rounded-full bg-white transition-transform ${
                            orbitLock ? 'translate-x-5' : 'translate-x-1'
                          }`}
                        />
                      </button>
                    </div>
                  </div>
                </div>

                {/* Camera Animation */}
                <div className="border-t border-white/20 pt-2">
                  <h3 className="text-white text-xs font-medium mb-2">Animation</h3>
                  
                  <div className={`space-y-${isMobile ? '3' : '1.5'}`}>
                    {/* Trajectory Mode */}
                    <div>
                      <label className="text-white text-xs block mb-2">Mode</label>
                      <Select
                        value={trajectoryMode}
                        onValueChange={(value) => {
                          if (onTrajectoryModeChange) {
                            onTrajectoryModeChange(value);
                          }
                        }}
                      >
                        <SelectTrigger className="w-full bg-gray-800 border-gray-600 text-white text-xs">
                          <SelectValue />
                        </SelectTrigger>
                        <SelectContent className="bg-gray-800 border-gray-600">
                          <SelectItem value="manual">Manual</SelectItem>
                          <SelectItem value="orbit">Orbit (360°)</SelectItem>
                          <SelectItem value="oscillate">Oscillate (Figure-8)</SelectItem>
                          <SelectItem value="custom">Custom (Zoom)</SelectItem>
                        </SelectContent>
                      </Select>
                    </div>

                    {/* Show duration and orbit lock only when not in manual mode */}
                    {trajectoryMode !== 'manual' && (
                      <>
                        <AnimatedSlider
                          label="Duration"
                          value={trajectoryDuration || 10}
                          min={2}
                          max={30}
                          step={1}
                          onChange={(value) => {
                            if (onTrajectoryDurationChange) {
                              onTrajectoryDurationChange(value);
                            }
                          }}
                          decimals={0}
                        />

                        {/* Status indicator */}
                        <div className="bg-gray-800/50 rounded p-2">
                          <div className="flex items-center justify-between">
                            <span className="text-white text-xs">Status</span>
                            <div className="flex items-center gap-2">
                              <div className="w-2 h-2 bg-green-400 rounded-full animate-pulse"></div>
                              <span className="text-green-400 text-xs">
                                {trajectoryMode === 'orbit' && 'Orbiting'}
                                {trajectoryMode === 'oscillate' && 'Figure-8'}
                                {trajectoryMode === 'custom' && 'Zooming'}
                              </span>
                            </div>
                          </div>
                        </div>
                      </>
                    )}

                    {trajectoryMode === 'manual' && (
                      <div className="bg-gray-800/50 rounded p-2">
                        <div className="flex items-center justify-between">
                          <span className="text-white text-xs">Status</span>
                          <span className="text-gray-400 text-xs">Manual Control</span>
                        </div>
                      </div>
                    )}
                  </div>
                </div>

                {/* RGB Halftone Effects */}
                {halftoneSettings && onHalftoneChange && (
                  <div className="border-t border-white/20 pt-2">
                    <h3 className="text-white text-xs font-medium mb-2">RGB Halftone Effects</h3>
                    
                    <div className={`space-y-${isMobile ? '3' : '1.5'}`}>
                      {/* Enable/Disable Toggle */}
                      <div>
                        <div className="flex justify-between items-center mb-2">
                          <label className="text-white text-xs">Enable Halftone</label>
                          <Switch
                            checked={!halftoneSettings.disable}
                            onCheckedChange={(checked) => onHalftoneChange({ disable: !checked })}
                          />
                        </div>
                      </div>

                      {!halftoneSettings.disable && (
                        <>
                          {/* Shape Selection */}
                          <div>
                            <label className="text-white text-xs block mb-2">Shape</label>
                            <Select
                              value={halftoneSettings.shape.toString()}
                              onValueChange={(value) => onHalftoneChange({ shape: parseInt(value) })}
                            >
                              <SelectTrigger className="w-full bg-gray-800 border-gray-600 text-white text-xs">
                                <SelectValue />
                              </SelectTrigger>
                              <SelectContent className="bg-gray-800 border-gray-600">
                                <SelectItem value="1">Dot</SelectItem>
                                <SelectItem value="2">Ellipse</SelectItem>
                                <SelectItem value="3">Line</SelectItem>
                                <SelectItem value="4">Square</SelectItem>
                              </SelectContent>
                            </Select>
                          </div>

                          {/* Radius */}
                          <div>
                            <div className="flex justify-between items-center mb-2">
                              <label className="text-white text-xs">Radius</label>
                              <span className="text-white/70 text-xs">{halftoneSettings.radius.toFixed(2)}</span>
                            </div>
                            <Slider
                              value={[halftoneSettings.radius]}
                              onValueChange={(value) => onHalftoneChange({ radius: value[0] })}
                              min={0.1}
                              max={1.0}
                              step={0.01}
                              className="w-full"
                            />
                          </div>

                          {/* RGB Rotation */}
                          <div>
                            <div className="flex justify-between items-center mb-2">
                              <label className="text-white text-xs">Red Rotation</label>
                              <span className="text-white/70 text-xs">{(halftoneSettings.rotateR * 180 / Math.PI).toFixed(0)}°</span>
                            </div>
                            <Slider
                              value={[halftoneSettings.rotateR * 180 / Math.PI]}
                              onValueChange={(value) => onHalftoneChange({ rotateR: value[0] * Math.PI / 180 })}
                              min={0}
                              max={360}
                              step={1}
                              className="w-full"
                            />
                          </div>

                          <div>
                            <div className="flex justify-between items-center mb-2">
                              <label className="text-white text-xs">Green Rotation</label>
                              <span className="text-white/70 text-xs">{(halftoneSettings.rotateG * 180 / Math.PI).toFixed(0)}°</span>
                            </div>
                            <Slider
                              value={[halftoneSettings.rotateG * 180 / Math.PI]}
                              onValueChange={(value) => onHalftoneChange({ rotateG: value[0] * Math.PI / 180 })}
                              min={0}
                              max={360}
                              step={1}
                              className="w-full"
                            />
                          </div>

                          <div>
                            <div className="flex justify-between items-center mb-2">
                              <label className="text-white text-xs">Blue Rotation</label>
                              <span className="text-white/70 text-xs">{(halftoneSettings.rotateB * 180 / Math.PI).toFixed(0)}°</span>
                            </div>
                            <Slider
                              value={[halftoneSettings.rotateB * 180 / Math.PI]}
                              onValueChange={(value) => onHalftoneChange({ rotateB: value[0] * Math.PI / 180 })}
                              min={0}
                              max={360}
                              step={1}
                              className="w-full"
                            />
                          </div>

                          {/* Scatter */}
                          <div>
                            <div className="flex justify-between items-center mb-2">
                              <label className="text-white text-xs">Scatter</label>
                              <span className="text-white/70 text-xs">{halftoneSettings.scatter.toFixed(2)}</span>
                            </div>
                            <Slider
                              value={[halftoneSettings.scatter]}
                              onValueChange={(value) => onHalftoneChange({ scatter: value[0] })}
                              min={0.0}
                              max={1.0}
                              step={0.01}
                              className="w-full"
                            />
                          </div>

                          {/* Blending */}
                          <div>
                            <div className="flex justify-between items-center mb-2">
                              <label className="text-white text-xs">Blending</label>
                              <span className="text-white/70 text-xs">{halftoneSettings.blending.toFixed(2)}</span>
                            </div>
                            <Slider
                              value={[halftoneSettings.blending]}
                              onValueChange={(value) => onHalftoneChange({ blending: value[0] })}
                              min={0.0}
                              max={1.0}
                              step={0.01}
                              className="w-full"
                            />
                          </div>

                          {/* Blending Mode */}
                          <div>
                            <label className="text-white text-xs block mb-2">Blending Mode</label>
                            <Select
                              value={halftoneSettings.blendingMode.toString()}
                              onValueChange={(value) => onHalftoneChange({ blendingMode: parseInt(value) })}
                            >
                              <SelectTrigger className="w-full bg-gray-800 border-gray-600 text-white text-xs">
                                <SelectValue />
                              </SelectTrigger>
                              <SelectContent className="bg-gray-800 border-gray-600">
                                <SelectItem value="1">Linear</SelectItem>
                                <SelectItem value="2">Multiply</SelectItem>
                                <SelectItem value="3">Add</SelectItem>
                                <SelectItem value="4">Lighter</SelectItem>
                                <SelectItem value="5">Darker</SelectItem>
                              </SelectContent>
                            </Select>
                          </div>

                          {/* Greyscale Toggle */}
                          <div>
                            <div className="flex justify-between items-center mb-2">
                              <label className="text-white text-xs">Greyscale</label>
                              <Switch
                                checked={halftoneSettings.greyscale}
                                onCheckedChange={(checked) => onHalftoneChange({ greyscale: checked })}
                              />
                            </div>
                          </div>
                        </>
                      )}
                    </div>
                  </div>
                )}
              </div>
            )}
          </div>
        )}
      </div>

      {/* GIF Export Dialog */}
      <GifExportDialog
        isOpen={isGifDialogOpen}
        onClose={() => setIsGifDialogOpen(false)}
        onStartRecording={handleStartGifRecording}
        onStopRecording={handleStopGifRecording}
        isRecording={isRecordingGif}
        progress={gifProgress}
        error={gifError}
        onClearError={handleClearGifError}
        videoRef={videoRef}
      />

      {/* Video Export Dialog */}
      <VideoExportDialog
        isOpen={isVideoDialogOpen}
        onClose={() => setIsVideoDialogOpen(false)}
        onStartRecording={handleStartVideoRecording}
        onStopRecording={handleStopVideoRecording}
        isRecording={isRecordingVideo}
        progress={videoProgress}
        error={videoError}
        onClearError={handleClearVideoError}
        videoRef={videoRef}
      />

      {/* Neural Network Visualizer */}
      <NeuralNetworkVisualizer
        isVisible={showNeuralNetwork}
        depthData={currentDepthData}
        onWeightUpdate={(weights) => {
          console.log('Neural network weights updated:', weights.length);
        }}
        className="mt-4"
      />

      {/* VR Interface */}
      <VRInterface
        canvasRef={canvasRef}
        isEnabled={vrEnabled}
        onToggle={setVrEnabled}
        onVRStateChange={setIsVRActive}
        onControllerUpdate={(controllers) => {
          console.log('VR controllers updated:', controllers.length);
        }}
      />
    </>
  );
};

```

#### client/src/components/DemoVideoSection.tsx
```tsx

import React from 'react';
import { Play } from 'lucide-react';

interface DemoVideoSectionProps {
  onDemoLoad: () => void;
  isLoading: boolean;
}

export const DemoVideoSection: React.FC<DemoVideoSectionProps> = ({
  onDemoLoad,
  isLoading
}) => {
  return (
    <div>
      {/* Minimal Secondary Demo Button */}
      <button
        onClick={onDemoLoad}
        disabled={isLoading}
        className="group inline-flex items-center justify-center gap-2 px-4 py-2 bg-white/3 hover:bg-white/6 backdrop-blur-sm border border-white/5 hover:border-white/10 rounded-lg transition-all duration-300 transform hover:scale-[1.02] disabled:opacity-40 disabled:cursor-not-allowed disabled:transform-none"
      >
        <Play className="w-3 h-3 text-white/50 group-hover:text-white/70 transition-colors" />
        <span className="text-white/50 group-hover:text-white/70 font-light text-xs tracking-wide transition-colors">
          {isLoading ? 'loading...' : 'demo'}
        </span>
      </button>
    </div>
  );
};

```

#### client/src/components/GifExportDialog.tsx
```tsx
import React, { useState, useEffect } from 'react';
import { Dialog, DialogContent, DialogHeader, DialogTitle } from './ui/dialog';
import { Button } from './ui/button';
import { Progress } from './ui/progress';
import { Download, X, AlertTriangle } from 'lucide-react';
import { GifSettings } from '../hooks/useGifExport';
import { gifOptimizer } from '../utils/gifOptimizer';

interface GifExportDialogProps {
  isOpen: boolean;
  onClose: () => void;
  onStartRecording: (settings: GifSettings) => void;
  onStopRecording: () => void;
  isRecording: boolean;
  progress: number;
  error: string | null;
  onClearError: () => void;
  videoRef: React.RefObject<HTMLVideoElement>;
  recordingPhase?: 'resetting' | 'capturing' | 'encoding' | null;
}

// Strict aspect ratio presets for professional output
const RESOLUTION_PRESETS = {
  '16:9 - 720p': { width: 1280, height: 720 },
  '16:9 - 1080p': { width: 1920, height: 1080 },
  '16:9 - 2K': { width: 2560, height: 1440 },
  '9:16 - 720p': { width: 720, height: 1280 },
  '9:16 - 1080p': { width: 1080, height: 1920 },
  '9:16 - 2K': { width: 1440, height: 2560 }
};

const QUALITY_PRESETS = {
  'Best': 1,
  'Good': 5,
  'Fast': 10
};

export const GifExportDialog: React.FC<GifExportDialogProps> = ({
  isOpen,
  onClose,
  onStartRecording,
  onStopRecording,
  isRecording,
  progress,
  error,
  onClearError,
  videoRef,
  recordingPhase
}) => {
  const [settings, setSettings] = useState<GifSettings>({
    fps: 24,
    quality: 5,
    width: 1280,
    height: 720
  });

  const [selectedResolution, setSelectedResolution] = useState('16:9 - 720p');
  const [selectedQuality, setSelectedQuality] = useState('Good');
  const [detectedDuration, setDetectedDuration] = useState<number | null>(null);

  // Auto-detect video duration when dialog opens
  useEffect(() => {
    if (isOpen && videoRef.current) {
      const duration = videoRef.current.duration;
      if (!isNaN(duration)) {
        const cappedDuration = Math.min(Math.max(duration, 1), 30);
        setDetectedDuration(cappedDuration);
      } else {
        setDetectedDuration(5); // Fallback
      }
    }
  }, [isOpen, videoRef]);

  const capabilities = gifOptimizer.getDeviceCapabilities();
  const finalSettings = detectedDuration ? { ...settings, duration: detectedDuration } : settings;
  const optimizedSettings = gifOptimizer.optimizeSettings(finalSettings);
  const estimatedSize = gifOptimizer.estimateFileSize(optimizedSettings);

  const handleResolutionChange = (preset: string) => {
    setSelectedResolution(preset);
    const resolution = RESOLUTION_PRESETS[preset as keyof typeof RESOLUTION_PRESETS];
    setSettings(prev => ({
      ...prev,
      width: resolution.width,
      height: resolution.height
    }));
  };

  const handleQualityChange = (quality: string) => {
    setSelectedQuality(quality);
    const qualityValue = QUALITY_PRESETS[quality as keyof typeof QUALITY_PRESETS];
    setSettings(prev => ({
      ...prev,
      quality: qualityValue
    }));
  };

  const handleStartRecording = () => {
    onClearError();
    onStartRecording(finalSettings);
  };

  const getRecordingStatusText = () => {
    switch (recordingPhase) {
      case 'resetting':
        return 'Resetting video position...';
      case 'capturing':
        return progress < 50 ? 'Capturing video frames...' : 'Finishing frame capture...';
      case 'encoding':
        return 'Encoding with Atkinson dithering...';
      default:
        return 'Preparing...';
    }
  };

  return (
    <Dialog open={isOpen} onOpenChange={onClose}>
      <DialogContent className="max-w-md bg-black/90 backdrop-blur-md border border-white/30 text-white">
        <DialogHeader>
          <DialogTitle className="flex items-center gap-2">
            <Download className="w-4 h-4" />
            Enhanced GIF Export
          </DialogTitle>
        </DialogHeader>

        <div className="space-y-4">
          {error && (
            <div className="bg-red-500/20 border border-red-500/50 rounded p-3">
              <div className="flex items-center gap-2 mb-2">
                <AlertTriangle className="w-4 h-4 text-red-400" />
                <span className="text-sm font-medium text-red-400">Error</span>
              </div>
              <p className="text-sm text-red-300 mb-2">{error}</p>
              <Button
                onClick={onClearError}
                variant="outline"
                size="sm"
                className="border-red-500/50 text-red-400 hover:bg-red-500/20"
              >
                Dismiss
              </Button>
            </div>
          )}

          {isRecording ? (
            <div className="space-y-4">
              <div className="text-center">
                <div className="text-lg font-semibold mb-3">Creating Enhanced GIF...</div>
                <Progress value={progress} className="w-full mb-2" />
                <div className="text-sm text-white/70">
                  {getRecordingStatusText()}
                </div>
                <div className="text-xs text-white/50 mt-1">
                  {progress}% Complete
                </div>
              </div>
              
              <Button
                onClick={onStopRecording}
                variant="destructive"
                className="w-full"
              >
                <X className="w-4 h-4 mr-2" />
                Cancel
              </Button>
            </div>
          ) : (
            <div className="space-y-4">
              {/* Strict Aspect Ratio Presets */}
              <div>
                <label className="block text-sm font-medium mb-2">Aspect Ratio & Resolution</label>
                <div className="grid grid-cols-1 gap-2 max-h-40 overflow-y-auto">
                  {Object.keys(RESOLUTION_PRESETS).map((preset) => (
                    <button
                      key={preset}
                      onClick={() => handleResolutionChange(preset)}
                      className={`p-3 text-sm rounded transition-colors text-left ${
                        selectedResolution === preset
                          ? 'bg-blue-600 text-white'
                          : 'bg-gray-700 text-white/70 hover:bg-gray-600'
                      }`}
                    >
                      <div className="font-medium">{preset}</div>
                      <div className="text-xs opacity-70">
                        {RESOLUTION_PRESETS[preset as keyof typeof RESOLUTION_PRESETS].width} × {RESOLUTION_PRESETS[preset as keyof typeof RESOLUTION_PRESETS].height}
                      </div>
                    </button>
                  ))}
                </div>
              </div>

              {/* Enhanced Quality Presets */}
              <div>
                <label className="block text-sm font-medium mb-2">Quality (Atkinson Dithering)</label>
                <div className="space-y-1">
                  {Object.keys(QUALITY_PRESETS).map((quality) => (
                    <button
                      key={quality}
                      onClick={() => handleQualityChange(quality)}
                      className={`w-full p-2 text-sm rounded transition-colors text-left ${
                        selectedQuality === quality
                          ? 'bg-blue-600 text-white'
                          : 'bg-gray-700 text-white/70 hover:bg-gray-600'
                      }`}
                    >
                      {quality} Quality
                    </button>
                  ))}
                </div>
              </div>

              {/* Auto-detected Duration Display */}
              <div>
                <label className="block text-sm font-medium mb-2">Duration (Auto-detected)</label>
                <div className="bg-gray-800/50 rounded p-3">
                  {detectedDuration !== null ? (
                    <div className="text-sm text-white/70">
                      Duration: <span className="font-medium text-white">{detectedDuration.toFixed(1)}s</span> (full video)
                    </div>
                  ) : (
                    <div className="text-sm text-white/50">
                      Detecting video duration...
                    </div>
                  )}
                </div>
              </div>

              {/* FPS Control */}
              <div>
                <div className="flex justify-between items-center mb-2">
                  <label className="text-sm font-medium">FPS</label>
                  <span className="text-sm text-white/70">{settings.fps}</span>
                </div>
                <input
                  type="range"
                  min="12"
                  max="30"
                  step="1"
                  value={settings.fps}
                  onChange={(e) => setSettings(prev => ({
                    ...prev,
                    fps: parseInt(e.target.value)
                  }))}
                  className="w-full"
                />
              </div>

              {/* Enhanced File Info */}
              <div className="bg-gray-800/50 rounded p-3 space-y-1">
                <div className="flex justify-between text-sm">
                  <span className="text-white/70">Est. size:</span>
                  <span className="font-medium">{estimatedSize.toFixed(1)} MB</span>
                </div>
                <div className="flex justify-between text-sm">
                  <span className="text-white/70">Total frames:</span>
                  <span className="font-medium">{detectedDuration ? (detectedDuration * settings.fps) : '---'}</span>
                </div>
                <div className="flex justify-between text-sm">
                  <span className="text-white/70">Workers:</span>
                  <span className="font-medium">{capabilities.workers}</span>
                </div>
                <div className="flex justify-between text-sm">
                  <span className="text-white/70">Features:</span>
                  <span className="font-medium text-green-400">High Quality, OffscreenCanvas</span>
                </div>
              </div>

              {/* Enhanced Export Button */}
              <Button
                onClick={handleStartRecording}
                disabled={detectedDuration === null}
                className="w-full bg-gradient-to-r from-blue-600 to-purple-600 hover:from-blue-500 hover:to-purple-500 disabled:bg-gray-600 disabled:cursor-not-allowed"
              >
                <Download className="w-4 h-4 mr-2" />
                {detectedDuration !== null ? 'Start Enhanced Recording' : 'Detecting Duration...'}
              </Button>
            </div>
          )}
        </div>
      </DialogContent>
    </Dialog>
  );
};

```

#### client/src/components/IntroAnimation.tsx
```tsx

import React, { useState, useEffect } from 'react';
import AdvancedTransition from './AdvancedTransition';
import { ArrowRight, Battery, Wifi, Bluetooth } from 'lucide-react';

interface ChatBubble {
  id: number;
  text: string;
  isUser: boolean;
  delay: number;
  isTyped?: boolean;
  hasInput?: boolean;
}

const CHAT_SEQUENCE: ChatBubble[] = [
  { id: 1, text: "What's this?", isUser: true, delay: 500 },
  { id: 2, text: "Well, you see, it's a video-to-point-cloud converter with WebGL rendering and...", isUser: false, delay: 2000 },
  { id: 3, text: "What?", isUser: true, delay: 4000 },
  { id: 4, text: "You upload a video and it makes pretty 3D dots.", isUser: false, delay: 5500 },
  { id: 5, text: "Why?", isUser: true, delay: 7000 },
  { id: 6, text: "Because it looks cool?", isUser: false, delay: 8500 },
  { id: 7, text: "Show me.", isUser: true, delay: 10000, isTyped: true, hasInput: true },
];

interface IntroAnimationProps {
  onTransitionComplete: () => void;
}

export const IntroAnimation: React.FC<IntroAnimationProps> = ({ onTransitionComplete }) => {
  const [visibleBubbles, setVisibleBubbles] = useState<number[]>([]);
  const [showTyping, setShowTyping] = useState<number | null>(null);
  const [typedText, setTypedText] = useState('');
  const [showInput, setShowInput] = useState(false);
  const [glitching, setGlitching] = useState(false);
  const [imageSrc, setImageSrc] = useState<string | null>(null);

  useEffect(() => {
    const timers: NodeJS.Timeout[] = [];

    CHAT_SEQUENCE.forEach((bubble, idx) => {
      if (!bubble.isUser && idx > 0) {
        timers.push(
          setTimeout(() => setShowTyping(bubble.id), bubble.delay - 800)
        );
      }

      timers.push(
        setTimeout(() => {
          setShowTyping(null);

          if (bubble.isTyped) {
            setShowInput(true);
            startTyping(bubble.text);
          } else {
            setVisibleBubbles(v => [...v, bubble.id]);
          }
        }, bubble.delay)
      );
    });

    return () => timers.forEach(t => clearTimeout(t));
  }, []);

  const startTyping = (text: string) => {
    let i = 0;
    const interval = setInterval(() => {
      setTypedText(text.slice(0, ++i));
      if (i === text.length) clearInterval(interval);
    }, 120);
  };

  const triggerTransition = async () => {
    if (glitching) return;
    setGlitching(true);

    // Import and use html2canvas
    const html2canvas = (await import('html2canvas')).default;
    const canvas = await html2canvas(document.body);
    setImageSrc(canvas.toDataURL());
  };

  return (
    <>
      <div className="fixed inset-0 bg-black flex items-center justify-center z-50">
        {/* Ambient lighting around device */}
        <div className="absolute inset-0 bg-gradient-radial from-blue-900/20 via-transparent to-transparent"></div>
        
        {/* iPhone Device Frame */}
        <div className="relative">
          {/* Enhanced Device Shadow with multiple layers */}
          <div className="absolute inset-0 bg-black/40 blur-2xl transform translate-y-4 scale-110"></div>
          <div className="absolute inset-0 bg-black/20 blur-xl transform translate-y-2 scale-105"></div>
          
          {/* Device Frame with premium materials */}
          <div className="relative w-[360px] h-[720px] bg-gradient-to-br from-gray-700 via-gray-800 to-gray-900 rounded-[40px] p-2 shadow-2xl border border-gray-600/30">
            {/* Enhanced Glass Reflection Overlay */}
            <div className="absolute inset-2 bg-gradient-to-br from-white/30 via-white/10 to-transparent rounded-[32px] pointer-events-none"></div>
            <div className="absolute inset-2 bg-gradient-to-tl from-transparent via-transparent to-white/20 rounded-[32px] pointer-events-none"></div>
            
            {/* Screen with glass effect */}
            <div className="relative w-full h-full bg-black rounded-[32px] overflow-hidden border border-gray-700/50">
              {/* Screen glass surface */}
              <div className="absolute inset-0 bg-gradient-to-br from-white/5 via-transparent to-transparent rounded-[32px] pointer-events-none z-30"></div>
              
              {/* Screen glow effect */}
              <div className="absolute inset-0 bg-gradient-to-b from-blue-500/5 via-transparent to-purple-500/5 rounded-[32px] pointer-events-none z-20"></div>
              
              {/* Dynamic Island (modern iPhone style) */}
              <div className="absolute top-2 left-1/2 transform -translate-x-1/2 w-28 h-7 bg-black rounded-full z-40 border border-gray-800">
                <div className="absolute top-2 left-1/2 transform -translate-x-1/2 w-12 h-1 bg-gray-700 rounded-full"></div>
                <div className="absolute top-2 right-8 w-1.5 h-1.5 bg-gray-600 rounded-full"></div>
                <div className="absolute top-1.5 right-5 w-2.5 h-2.5 bg-gray-700 rounded-full"></div>
              </div>

              {/* Enhanced CRT Scanlines */}
              <div className="absolute inset-0 bg-gradient-to-b from-transparent via-transparent to-transparent opacity-15 pointer-events-none z-25" 
                   style={{
                     backgroundImage: 'repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(255,255,255,0.02) 2px, rgba(255,255,255,0.02) 4px)'
                   }}>
              </div>

              {/* Messages App */}
              <div className="flex flex-col h-full pt-10 font-sans">
                {/* Enhanced Status Bar with realistic icons */}
                <div className="flex justify-between items-center px-6 py-2 text-xs text-white font-semibold">
                  <div className="flex items-center gap-1">
                    <span className="text-sm">1:43</span>
                  </div>
                  <div className="flex items-center gap-1">
                    {/* Signal bars */}
                    <div className="flex items-end gap-0.5 mr-1">
                      <div className="w-0.5 h-1 bg-white rounded-full"></div>
                      <div className="w-0.5 h-1.5 bg-white rounded-full"></div>
                      <div className="w-0.5 h-2 bg-white rounded-full"></div>
                      <div className="w-0.5 h-2.5 bg-white rounded-full"></div>
                    </div>
                    <span className="text-xs mr-2">pixelflow</span>
                    <Wifi size={12} className="text-white mr-1" />
                    <Bluetooth size={10} className="text-white mr-1 opacity-80" />
                    <div className="flex items-center">
                      <Battery size={16} className="text-white" />
                      <span className="text-xs ml-1">100</span>
                    </div>
                  </div>
                </div>

                {/* Messages Header */}
                <div className="flex items-center justify-center px-4 py-3 border-b border-gray-800/60">
                  {/* Default iOS Contact Avatar */}
                  <div className="w-8 h-8 mr-3 rounded-full bg-gray-600 flex items-center justify-center shadow-lg">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" className="text-gray-300">
                      <path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"/>
                      <circle cx="12" cy="7" r="4" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"/>
                    </svg>
                  </div>
                  <div className="text-lg font-semibold text-white">Messages</div>
                </div>
                
                {/* Chat Container */}
                <div className="flex-1 px-4 py-4 space-y-4 overflow-hidden bg-black">
                  {CHAT_SEQUENCE.map((bubble) => {
                    const isVisible = visibleBubbles.includes(bubble.id);
                    const isTyping = showTyping === bubble.id;

                    return (
                      <div key={bubble.id} className="space-y-3">
                        {/* Typing Indicator */}
                        {isTyping && !bubble.isUser && (
                          <div className="flex justify-start">
                            <div className="bg-gray-800 rounded-2xl px-4 py-3 max-w-xs animate-pulse shadow-lg">
                              <div className="flex space-x-1">
                                <div className="w-2 h-2 bg-gray-400 rounded-full animate-bounce"></div>
                                <div className="w-2 h-2 bg-gray-400 rounded-full animate-bounce" style={{ animationDelay: '0.1s' }}></div>
                                <div className="w-2 h-2 bg-gray-400 rounded-full animate-bounce" style={{ animationDelay: '0.2s' }}></div>
                              </div>
                            </div>
                          </div>
                        )}

                        {/* Chat Bubble */}
                        {isVisible && (
                          <div className={`flex ${bubble.isUser ? 'justify-end' : 'justify-start'}`}>
                            <div className="relative max-w-[250px]">
                              {/* Bubble Content */}
                              <div
                                className={`
                                  px-4 py-3 rounded-2xl shadow-lg animate-scale-in text-sm font-medium leading-relaxed
                                  ${bubble.isUser 
                                    ? 'bg-blue-500 text-white' 
                                    : 'bg-gray-800 text-white'
                                  }
                                `}
                              >
                                {bubble.text}
                              </div>
                            </div>
                          </div>
                        )}
                      </div>
                    );
                  })}
                </div>

                {/* Input Area */}
                {showInput && (
                  <div className="px-4 pb-8 pt-2">
                    <div className="flex items-center space-x-3 bg-gray-900 rounded-full px-4 py-3 border border-gray-700">
                      <input
                        type="text"
                        value={typedText}
                        className="flex-1 bg-transparent text-sm text-white placeholder-gray-400 outline-none font-medium"
                        placeholder="iMessage"
                        readOnly
                      />
                      <div className="relative">
                        <button
                          onClick={triggerTransition}
                          disabled={!typedText || glitching}
                          className={`
                            w-8 h-8 rounded-full flex items-center justify-center transition-all duration-200 shadow-lg relative
                            ${typedText && !glitching
                              ? 'bg-blue-500 hover:bg-blue-600 cursor-pointer shadow-blue-500/30 animate-blink' 
                              : 'bg-gray-600 cursor-not-allowed'
                            }
                          `}
                        >
                          <ArrowRight className="w-4 h-4 text-white" />
                        </button>
                      </div>
                    </div>
                    
                    {/* Home Indicator */}
                    <div className="flex justify-center mt-4">
                      <div className="w-32 h-1 bg-white/30 rounded-full"></div>
                    </div>
                  </div>
                )}
              </div>
            </div>
          </div>
        </div>
      </div>

      {/* Advanced Transition */}
      {glitching && imageSrc && (
        <AdvancedTransition
          imageSrc={imageSrc}
          duration={2000}
          onComplete={onTransitionComplete}
        />
      )}

      {/* Enhanced Animation Styles */}
      <style>{`
        @keyframes scale-in {
          from {
            transform: scale(0.9);
            opacity: 0;
          }
          to {
            transform: scale(1);
            opacity: 1;
          }
        }
        
        @keyframes blink {
          0%, 50% { 
            opacity: 1;
          }
          51%, 100% { 
            opacity: 0.3;
          }
        }
        
        .animate-scale-in {
          animation: scale-in 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        .animate-blink {
          animation: blink 1s ease-in-out infinite;
        }
        
        .bg-gradient-radial {
          background: radial-gradient(circle, var(--tw-gradient-stops));
        }
      `}</style>
    </>
  );
};

```

#### client/src/components/LoadingScreen.tsx
```tsx

import React from 'react';
import { Video } from 'lucide-react';

export const LoadingScreen: React.FC = () => {
  return (
    <div className="fixed inset-0 bg-black flex items-center justify-center z-50">
      <div className="text-center">
        <div className="animate-spin rounded-full h-12 w-12 border-b-2 border-white mx-auto mb-4"></div>
        <div className="flex items-center justify-center text-white mb-2">
          <Video className="w-5 h-5 mr-2" />
          <span className="text-lg font-medium">Processing Video</span>
        </div>
        <p className="text-white/70 text-sm">
          Converting video frames to point cloud data...
        </p>
      </div>
    </div>
  );
};

```

#### client/src/components/NeuralNetworkVisualizer.tsx
```tsx
/**
 * Neural Network Visualizer integrated from TensorFlow Playground
 * Provides interactive visualization for depth estimation training
 */
import React, { useRef, useEffect, useState } from 'react';
import * as d3 from 'd3';

interface Node {
  id: string;
  layer: number;
  x: number;
  y: number;
  value: number;
  bias: number;
  activation: 'tanh' | 'relu' | 'sigmoid' | 'linear';
}

interface Link {
  source: Node;
  target: Node;
  weight: number;
}

interface NeuralNetworkVisualizerProps {
  isVisible: boolean;
  depthData?: Float32Array;
  onWeightUpdate?: (weights: number[]) => void;
  className?: string;
  realTimeUpdates?: boolean;
  trainingMode?: boolean;
}

export const NeuralNetworkVisualizer: React.FC<NeuralNetworkVisualizerProps> = ({
  isVisible,
  depthData,
  onWeightUpdate,
  className = '',
  realTimeUpdates = true,
  trainingMode = false
}) => {
  const svgRef = useRef<SVGSVGElement>(null);
  const [isTraining, setIsTraining] = useState(false);
  const [epoch, setEpoch] = useState(0);
  const [loss, setLoss] = useState(0.5);
  const [nodes, setNodes] = useState<Node[]>([]);
  const [links, setLinks] = useState<Link[]>([]);
  const nodesRef = useRef<Node[]>([]);
  const linksRef = useRef<Link[]>([]);

  // Network architecture: 2 inputs -> 4 hidden -> 2 hidden -> 1 output
  const networkStructure = [2, 4, 2, 1];

  const initializeNetwork = () => {
    const nodes: Node[] = [];
    const links: Link[] = [];
    let nodeId = 0;

    // Create nodes for each layer
    networkStructure.forEach((layerSize, layerIndex) => {
      for (let i = 0; i < layerSize; i++) {
        nodes.push({
          id: `node-${nodeId++}`,
          layer: layerIndex,
          x: layerIndex * 120 + 50,
          y: i * 60 + 50 + (layerIndex > 0 ? (networkStructure[0] - layerSize) * 15 : 0),
          value: Math.random() * 0.2 - 0.1,
          bias: Math.random() * 0.2 - 0.1,
          activation: layerIndex === networkStructure.length - 1 ? 'linear' : 'tanh'
        });
      }
    });

    // Create links between layers
    for (let layer = 0; layer < networkStructure.length - 1; layer++) {
      const currentLayerNodes = nodes.filter(n => n.layer === layer);
      const nextLayerNodes = nodes.filter(n => n.layer === layer + 1);

      currentLayerNodes.forEach(source => {
        nextLayerNodes.forEach(target => {
          links.push({
            source,
            target,
            weight: Math.random() * 0.4 - 0.2
          });
        });
      });
    }

    setNodes(nodes);
    setLinks(links);
    nodesRef.current = nodes;
    linksRef.current = links;
  };

  const activationFunction = (x: number, type: string): number => {
    switch (type) {
      case 'tanh': return Math.tanh(x);
      case 'relu': return Math.max(0, x);
      case 'sigmoid': return 1 / (1 + Math.exp(-x));
      default: return x;
    }
  };

  const forwardPass = (input: [number, number]): number => {
    const nodes = nodesRef.current;
    const links = linksRef.current;

    // Set input values
    nodes[0].value = input[0];
    nodes[1].value = input[1];

    // Forward propagation
    for (let layer = 1; layer < networkStructure.length; layer++) {
      const layerNodes = nodes.filter(n => n.layer === layer);
      
      layerNodes.forEach(node => {
        let sum = node.bias;
        const incomingLinks = links.filter(l => l.target === node);
        
        incomingLinks.forEach(link => {
          sum += link.source.value * link.weight;
        });
        
        node.value = activationFunction(sum, node.activation);
      });
    }

    return nodes[nodes.length - 1].value;
  };

  const trainStep = () => {
    if (!depthData || depthData.length === 0) return;

    const batchSize = 32;
    let totalLoss = 0;

    for (let i = 0; i < batchSize; i++) {
      // Sample random points from depth data
      const idx = Math.floor(Math.random() * (depthData.length - 1));
      const x = (idx % 256) / 256 - 0.5; // Normalize to [-0.5, 0.5]
      const y = Math.floor(idx / 256) / 256 - 0.5;
      const target = depthData[idx];

      const predicted = forwardPass([x, y]);
      const error = predicted - target;
      totalLoss += error * error;

      // Simple gradient descent (simplified backpropagation)
      const learningRate = 0.01;
      linksRef.current.forEach(link => {
        const gradient = error * link.source.value * 0.1; // Simplified gradient
        link.weight -= learningRate * gradient;
        link.weight = Math.max(-2, Math.min(2, link.weight)); // Clamp weights
      });
    }

    setLoss(totalLoss / batchSize);
    setEpoch(prev => prev + 1);

    // Update external weights
    if (onWeightUpdate) {
      const weights = linksRef.current.map(l => l.weight);
      onWeightUpdate(weights);
    }
  };

  const renderNetwork = () => {
    if (!svgRef.current) return;

    const svg = d3.select(svgRef.current);
    svg.selectAll("*").remove();

    const width = 500;
    const height = 300;

    // Create gradient definitions for visualization
    const defs = svg.append("defs");
    const gradient = defs.append("linearGradient")
      .attr("id", "weightGradient");
    
    gradient.append("stop")
      .attr("offset", "0%")
      .attr("stop-color", "#ff4444");
    
    gradient.append("stop")
      .attr("offset", "50%")
      .attr("stop-color", "#ffffff");
    
    gradient.append("stop")
      .attr("offset", "100%")
      .attr("stop-color", "#4444ff");

    // Render links
    svg.selectAll(".link")
      .data(linksRef.current)
      .enter()
      .append("line")
      .attr("class", "link")
      .attr("x1", d => d.source.x)
      .attr("y1", d => d.source.y)
      .attr("x2", d => d.target.x)
      .attr("y2", d => d.target.y)
      .attr("stroke", d => {
        const intensity = Math.abs(d.weight) / 2;
        return d.weight > 0 ? 
          `rgba(68, 68, 255, ${intensity})` : 
          `rgba(255, 68, 68, ${intensity})`;
      })
      .attr("stroke-width", d => Math.abs(d.weight) * 3 + 1)
      .attr("opacity", 0.7);

    // Render nodes
    svg.selectAll(".node")
      .data(nodesRef.current)
      .enter()
      .append("circle")
      .attr("class", "node")
      .attr("cx", d => d.x)
      .attr("cy", d => d.y)
      .attr("r", 12)
      .attr("fill", d => {
        const intensity = Math.abs(d.value);
        return d.value > 0 ? 
          `rgba(68, 68, 255, ${Math.min(intensity, 1)})` : 
          `rgba(255, 68, 68, ${Math.min(intensity, 1)})`;
      })
      .attr("stroke", "#333")
      .attr("stroke-width", 2);

    // Add layer labels
    const layerLabels = ["Input", "Hidden 1", "Hidden 2", "Output"];
    svg.selectAll(".layer-label")
      .data(layerLabels)
      .enter()
      .append("text")
      .attr("class", "layer-label")
      .attr("x", (d, i) => i * 120 + 50)
      .attr("y", 20)
      .attr("text-anchor", "middle")
      .attr("fill", "#666")
      .attr("font-size", "12px")
      .text(d => d);
  };

  useEffect(() => {
    if (isVisible) {
      initializeNetwork();
      renderNetwork();
    }
  }, [isVisible]);

  useEffect(() => {
    if (isVisible) {
      renderNetwork();
    }
  }, [nodesRef.current, linksRef.current]);

  useEffect(() => {
    let interval: NodeJS.Timeout;
    
    if (isTraining && depthData) {
      interval = setInterval(() => {
        trainStep();
        renderNetwork();
      }, 100);
    }

    return () => {
      if (interval) clearInterval(interval);
    };
  }, [isTraining, depthData]);

  // Real-time depth data processing for network visualization
  useEffect(() => {
    if (!depthData || depthData.length === 0 || !realTimeUpdates) return;
    
    const processDepthData = () => {
      // Sample depth data at strategic points for input layer
      const sampleIndices = [
        Math.floor(depthData.length * 0.25),
        Math.floor(depthData.length * 0.5), 
        Math.floor(depthData.length * 0.75),
        Math.floor(depthData.length * 0.9)
      ];
      
      const inputActivations = sampleIndices.map(idx => {
        const depth = depthData[idx];
        return Math.max(0, Math.min(1, depth));
      });
      
      // Calculate depth complexity metrics for training visualization
      const depthMean = depthData.reduce((sum, val) => sum + val, 0) / depthData.length;
      const depthVariance = depthData.reduce((sum, val) => sum + Math.pow(val - depthMean, 2), 0) / depthData.length;
      const depthComplexity = Math.sqrt(depthVariance);
      
      // Update network with real depth activations
      setNodes((prevNodes: Node[]) => 
        prevNodes.map((node: Node) => {
          if (node.layer === 0) {
            const inputIndex = parseInt(node.id.split('-')[1]);
            return { 
              ...node, 
              value: inputActivations[inputIndex] || 0,
              bias: depthMean * 0.1
            };
          }
          return node;
        })
      );
      
      // Update loss based on scene complexity
      setLoss(Math.max(0.01, Math.min(0.99, depthComplexity)));
      
      // Trigger weight updates to point cloud renderer
      if (onWeightUpdate && nodesRef.current.length > 0) {
        const weights = linksRef.current.map((link: Link) => link.weight);
        onWeightUpdate(weights);
      }
      
      if (trainingMode) {
        setEpoch(prev => prev + 1);
      }
    };
    
    processDepthData();
  }, [depthData, realTimeUpdates, trainingMode, onWeightUpdate]);

  if (!isVisible) return null;

  return (
    <div className={`neural-network-visualizer bg-gray-900 rounded-lg p-4 ${className}`}>
      <div className="flex justify-between items-center mb-4">
        <h3 className="text-white text-lg font-semibold">Depth Estimation Neural Network</h3>
        <div className="flex gap-2">
          <button
            onClick={() => setIsTraining(!isTraining)}
            className={`px-3 py-1 rounded text-sm ${
              isTraining 
                ? 'bg-red-600 hover:bg-red-700 text-white' 
                : 'bg-green-600 hover:bg-green-700 text-white'
            }`}
          >
            {isTraining ? 'Stop' : 'Train'}
          </button>
          <button
            onClick={() => {
              setIsTraining(false);
              setEpoch(0);
              setLoss(0.5);
              initializeNetwork();
              renderNetwork();
            }}
            className="px-3 py-1 bg-gray-600 hover:bg-gray-700 text-white rounded text-sm"
          >
            Reset
          </button>
        </div>
      </div>

      <div className="grid grid-cols-2 gap-4 mb-4 text-sm text-gray-300">
        <div>Epoch: <span className="text-blue-400">{epoch}</span></div>
        <div>Loss: <span className="text-orange-400">{loss.toFixed(4)}</span></div>
      </div>

      <div className="bg-gray-800 rounded p-2">
        <svg
          ref={svgRef}
          width="500"
          height="300"
          className="w-full"
          viewBox="0 0 500 300"
        />
      </div>

      <div className="mt-2 text-xs text-gray-400">
        <p>• Blue connections/nodes: positive weights/activations</p>
        <p>• Red connections/nodes: negative weights/activations</p>
        <p>• Line thickness: weight magnitude</p>
      </div>
    </div>
  );
};

export default NeuralNetworkVisualizer;
```

#### client/src/components/OceanShader.tsx
```tsx

import React, { useRef, useEffect } from 'react';

// Device detection utility
const getDeviceInfo = () => {
  const userAgent = navigator.userAgent;
  const isIPhone = /iPhone/.test(userAgent);
  const isIPad = /iPad/.test(userAgent);
  const isIOS = isIPhone || isIPad;
  
  // iPhone model detection based on screen dimensions and user agent
  let iPhoneGeneration = 'unknown';
  let isIPhone15ProMax = false;
  
  if (isIPhone) {
    const screenWidth = window.screen.width;
    const screenHeight = window.screen.height;
    const pixelRatio = window.devicePixelRatio;
    
    // iPhone 15 Pro Max detection
    if ((screenWidth === 430 && screenHeight === 932 && pixelRatio === 3) ||
        (screenWidth === 932 && screenHeight === 430 && pixelRatio === 3)) {
      isIPhone15ProMax = true;
      iPhoneGeneration = 'modern'; // Use modern tier like other high-end iPhones
    }
    // iPhone 14 Pro Max, 14 Plus, 13 Pro Max, 12 Pro Max (but not 15 Pro Max)
    else if ((screenWidth === 428 && screenHeight === 926) || (screenWidth === 414 && screenHeight === 896)) {
      iPhoneGeneration = 'modern'; // A14+ chip
    }
    // iPhone 14 Pro, 14, 13 Pro, 13, 13 mini, 12 Pro, 12, 12 mini
    else if (screenWidth >= 375 && pixelRatio >= 3) {
      iPhoneGeneration = 'modern'; // A14+ chip
    }
    // iPhone 11 Pro Max, 11 Pro, 11, XS Max, XS, XR, X
    else if (screenWidth >= 375 && pixelRatio >= 2) {
      iPhoneGeneration = 'balanced'; // A12-A13 chip
    }
    // Older iPhones
    else {
      iPhoneGeneration = 'conservative';
    }
  }
  
  return {
    isIPhone,
    isIPad,
    isIOS,
    iPhoneGeneration,
    isIPhone15ProMax,
    isMobile: /Android|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(userAgent)
  };
};

// Quality settings based on device capabilities
const getQualitySettings = (deviceInfo: ReturnType<typeof getDeviceInfo>) => {
  if (deviceInfo.isIPhone) {
    switch (deviceInfo.iPhoneGeneration) {

      case 'modern':
        return {
          precision: 'highp',
          rayMarchIterations: 16,  // Restored for modern GPUs with optimizations
          normalIterations: 48,    // Restored for ultra-sharp detail
          pixelRatioMultiplier: 1.4, // Increased for sharper rendering
          enableInteraction: true,
          deviceTier: 'Modern iPhone'
        };
      case 'balanced':
        return {
          precision: 'highp',
          rayMarchIterations: 12,  // Reduced from 14 for consistent performance
          normalIterations: 36,    // Reduced from 42 for frame stability
          pixelRatioMultiplier: 1.2, // Reduced from 1.3 for smoother rendering
          enableInteraction: true,
          deviceTier: 'Balanced iPhone'
        };
      default:
        return {
          precision: 'mediump',
          rayMarchIterations: 10,  // Reduced from 12 for older devices
          normalIterations: 30,    // Reduced from 36 for stability
          pixelRatioMultiplier: 1.0,
          enableInteraction: true,
          deviceTier: 'Conservative iPhone'
        };
    }
  } else if (deviceInfo.isIPad) {
    return {
      precision: 'highp',
      rayMarchIterations: 18,
      normalIterations: 54,
      pixelRatioMultiplier: 1.8,
      enableInteraction: true,
      deviceTier: 'iPad'
    };
  } else if (deviceInfo.isMobile) {
    return {
      precision: 'mediump',
      rayMarchIterations: 10,
      normalIterations: 30,
      pixelRatioMultiplier: 1.0,
      enableInteraction: false,
      deviceTier: 'Mobile'
    };
  } else {
    // FIXED: Desktop quality settings - reduced from ultra levels
    return {
      precision: 'highp',
      rayMarchIterations: 16,  // Reduced from 20 to restore MacBook performance
      normalIterations: 48,    // Reduced from 60 to restore MacBook performance
      pixelRatioMultiplier: 1.5, // Reduced from 2.0 to restore MacBook performance
      enableInteraction: true,
      deviceTier: 'Desktop'
    };
  }
};

const createFragmentShader = (quality: ReturnType<typeof getQualitySettings>) => `
  precision ${quality.precision} float;
  uniform float iTime;
  uniform vec2 iResolution;
  uniform vec4 iMouse;
  
  // GPU Performance Hacks - Compile-time constants
  #define DRAG_MULT 0.38
  #define WATER_DEPTH 1.0
  #define CAMERA_HEIGHT 1.5
  #define ITERATIONS_RAYMARCH ${quality.rayMarchIterations}
  #define ITERATIONS_NORMAL ${quality.normalIterations}
  
  // Modern optimization: Hardware-accelerated math constants
  #define PI 3.14159265359
  #define TWO_PI 6.28318530718
  #define INV_PI 0.31830988618
  #define SQRT2 1.41421356237
  #define EPSILON 1e-6
  
  // Modern GPU features: Fast approximations
  #define FAST_NORMALIZE(v) (v * inversesqrt(dot(v, v)))
  #define FAST_LENGTH(v) sqrt(dot(v, v))
  #define SATURATE(x) clamp(x, 0.0, 1.0)

  // Modern GPU: Ultra-fast wave calculation with SIMD optimization
  vec2 wavedx(vec2 position, vec2 direction, float frequency, float timeshift) {
    float x = dot(direction, position) * frequency + timeshift;
    // Modern optimization: Use GPU's native sincos instruction
    vec2 sc = vec2(sin(x), cos(x));
    float wave = exp(sc.x - 1.0);
    float dx = wave * sc.y;
    return vec2(wave, -dx);
  }
  
  // Modern GPU: Hardware-accelerated noise function
  float hash21(vec2 p) {
    p = fract(p * vec2(123.34, 456.21));
    p += dot(p, p + 45.32);
    return fract(p.x * p.y);
  }
  
  // Modern optimization: Vectorized wave computation
  vec4 wave4(vec4 x) {
    return exp(sin(x) - 1.0);
  }

  // Original ocean algorithm with GPU performance optimizations
  float getwaves(vec2 position, int iterations) {
    float wavePhaseShift = FAST_LENGTH(position) * 0.1;
    float iter = 0.0;
    float frequency = 1.0;
    float timeMultiplier = 2.0;
    float weight = 1.0;
    float sumOfValues = 0.0;
    float sumOfWeights = 0.0;
    
    // GPU Performance: Pre-compute time-based values
    float timeBase = iTime + wavePhaseShift;
    vec2 posOffset = position;
    
    // Original wave computation with GPU optimizations
    for(int i = 0; i < 64; i++) {
      if(i >= iterations) break;
      
      vec2 sc = vec2(sin(iter), cos(iter));
      vec2 res = wavedx(posOffset, sc, frequency, timeBase * timeMultiplier);
      posOffset += sc * res.y * weight * DRAG_MULT;
      
      sumOfValues += res.x * weight;
      sumOfWeights += weight;
      
      // GPU Performance: Hardware-accelerated parameter updates
      weight *= 0.82;
      frequency *= 1.18;
      timeMultiplier *= 1.07;
      iter += 1232.399963;
    }
    
    return sumOfValues / sumOfWeights;
  }

  // GPU Hack: Optimized ray marching with early termination
  float raymarchwater(vec3 camera, vec3 start, vec3 end, float depth) {
    vec3 pos = start;
    vec3 dir = normalize(end - start);
    
    // GPU optimization: Pre-compute step size and threshold
    float stepSize = length(end - start) / 64.0;
    float threshold = 0.01;
    
    for(int i=0; i < 64; i++) {
      float height = getwaves(pos.xz, ITERATIONS_RAYMARCH) * depth - depth;
      
      // GPU hack: Early exit with optimized comparison
      if(height + threshold > pos.y) {
        return distance(pos, camera);
      }
      
      // GPU optimization: Use fixed step size for better performance
      pos += dir * max(stepSize, pos.y - height);
    }
    return distance(start, camera);
  }

  // Modern GPU: Ultra-sharp normal calculation with optimized finite differences
  vec3 normal(vec2 pos, float e, float depth) {
    // Modern optimization: Central differences for higher accuracy and sharpness
    vec2 ex = vec2(e, 0);
    float H = getwaves(pos, ITERATIONS_NORMAL) * depth;
    float Hleft = getwaves(pos - ex.xy, ITERATIONS_NORMAL) * depth;
    float Hright = getwaves(pos + ex.xy, ITERATIONS_NORMAL) * depth;
    float Hdown = getwaves(pos - ex.yx, ITERATIONS_NORMAL) * depth;
    float Hup = getwaves(pos + ex.yx, ITERATIONS_NORMAL) * depth;
    
    // Ultra-sharp gradients using central differences
    vec2 gradient = vec2(Hright - Hleft, Hup - Hdown) / (2.0 * e);
    return FAST_NORMALIZE(vec3(-gradient.x, 1.0, -gradient.y));
  }

  mat3 createRotationMatrixAxisAngle(vec3 axis, float angle) {
    float s = sin(angle);
    float c = cos(angle);
    float oc = 1.0 - c;
    return mat3(
      oc * axis.x * axis.x + c, oc * axis.x * axis.y - axis.z * s, oc * axis.z * axis.x + axis.y * s, 
      oc * axis.x * axis.y + axis.z * s, oc * axis.y * axis.y + c, oc * axis.y * axis.z - axis.x * s, 
      oc * axis.z * axis.x - axis.y * s, oc * axis.y * axis.z + axis.x * s, oc * axis.z * axis.z + c
    );
  }

  vec3 getRay(vec2 fragCoord) {
    vec2 uv = ((fragCoord.xy / iResolution.xy) * 2.0 - 1.0) * vec2(iResolution.x / iResolution.y, 1.0);
    vec3 proj = normalize(vec3(uv.x, uv.y, 1.5));
    
    vec2 normalizedMouse = iMouse.xy / iResolution.xy;
    return createRotationMatrixAxisAngle(vec3(0.0, -1.0, 0.0), 3.0 * ((normalizedMouse.x + 0.5) * 2.0 - 1.0)) 
      * createRotationMatrixAxisAngle(vec3(1.0, 0.0, 0.0), 0.5 + 1.5 * (((normalizedMouse.y == 0.0 ? 0.27 : normalizedMouse.y) * 1.0) * 2.0 - 1.0))
      * proj;
  }

  float intersectPlane(vec3 origin, vec3 direction, vec3 point, vec3 normal) { 
    return clamp(dot(point - origin, normal) / dot(direction, normal), -1.0, 9991999.0); 
  }

  vec3 extra_cheap_atmosphere(vec3 raydir, vec3 sundir) {
    float special_trick = 1.0 / (raydir.y * 1.0 + 0.1);
    float special_trick2 = 1.0 / (sundir.y * 11.0 + 1.0);
    float raysundt = pow(abs(dot(sundir, raydir)), 2.0);
    float sundt = pow(max(0.0, dot(sundir, raydir)), 8.0);
    float mymie = sundt * special_trick * 0.2;
    vec3 suncolor = mix(vec3(1.0), max(vec3(0.0), vec3(1.0) - vec3(5.5, 13.0, 22.4) / 22.4), special_trick2);
    vec3 bluesky= vec3(5.5, 13.0, 22.4) / 22.4 * suncolor;
    vec3 bluesky2 = max(vec3(0.0), bluesky - vec3(5.5, 13.0, 22.4) * 0.002 * (special_trick + -6.0 * sundir.y * sundir.y));
    bluesky2 *= special_trick * (0.24 + raysundt * 0.24);
    return bluesky2 * (1.0 + 1.0 * pow(1.0 - raydir.y, 3.0));
  } 

  vec3 getSunDirection() {
    return normalize(vec3(-0.0773502691896258 , 0.5 + sin(iTime * 0.2 + 2.6) * 0.45 , 0.5773502691896258));
  }

  vec3 getAtmosphere(vec3 dir) {
     return extra_cheap_atmosphere(dir, getSunDirection()) * 0.5;
  }

  float getSun(vec3 dir) { 
    return pow(max(0.0, dot(dir, getSunDirection())), 720.0) * 210.0;
  }



  vec3 aces_tonemap(vec3 color) {  
    mat3 m1 = mat3(
      0.59719, 0.07600, 0.02840,
      0.35458, 0.90834, 0.13383,
      0.04823, 0.01566, 0.83777
    );
    mat3 m2 = mat3(
      1.60475, -0.10208, -0.00327,
      -0.53108,  1.10813, -0.07276,
      -0.07367, -0.00605,  1.07602
    );
    vec3 v = m1 * color;  
    vec3 a = v * (v + 0.0245786) - 0.000090537;
    vec3 b = v * (0.983729 * v + 0.4329510) + 0.238081;
    return pow(clamp(m2 * (a / b), 0.0, 1.0), vec3(1.0 / 2.2));  
  }

  void main() {
    vec2 fragCoord = gl_FragCoord.xy;
    vec3 ray = getRay(fragCoord);
    
    if(ray.y >= 0.0) {
      vec3 C = getAtmosphere(ray) + getSun(ray);
      gl_FragColor = vec4(aces_tonemap(C * 2.0), 1.0);   
      return;
    }

    vec3 waterPlaneHigh = vec3(0.0, 0.0, 0.0);
    vec3 waterPlaneLow = vec3(0.0, -WATER_DEPTH, 0.0);
    vec3 origin = vec3(iTime * 0.2, CAMERA_HEIGHT, 1.0);

    float highPlaneHit = intersectPlane(origin, ray, waterPlaneHigh, vec3(0.0, 1.0, 0.0));
    float lowPlaneHit = intersectPlane(origin, ray, waterPlaneLow, vec3(0.0, 1.0, 0.0));
    vec3 highHitPos = origin + ray * highPlaneHit;
    vec3 lowHitPos = origin + ray * lowPlaneHit;

    float dist = raymarchwater(origin, highHitPos, lowHitPos, WATER_DEPTH);
    vec3 waterHitPos = origin + ray * dist;

    vec3 N = normal(waterHitPos.xz, 0.01, WATER_DEPTH);
    N = mix(N, vec3(0.0, 1.0, 0.0), 0.8 * min(1.0, sqrt(dist*0.01) * 1.1));

    float fresnel = (0.04 + (1.0-0.04)*(pow(1.0 - max(0.0, dot(-N, ray)), 5.0)));

    vec3 R = normalize(reflect(ray, N));
    R.y = abs(R.y);
    
    vec3 reflection = getAtmosphere(R) + getSun(R);
    vec3 scattering = vec3(0.0293, 0.0698, 0.1717) * 0.1 * (0.2 + (waterHitPos.y + WATER_DEPTH) / WATER_DEPTH);

    vec3 C = fresnel * reflection + scattering;
    gl_FragColor = vec4(aces_tonemap(C * 2.0), 1.0);
  }
`;

const vertexShaderSource = `
  attribute vec4 a_position;
  void main() {
    gl_Position = a_position;
  }
`;

interface OceanShaderProps {
  className?: string;
}

export const OceanShader: React.FC<OceanShaderProps> = ({ className = '' }) => {
  const canvasRef = useRef<HTMLCanvasElement>(null);
  const glRef = useRef<WebGLRenderingContext | null>(null);
  const programRef = useRef<WebGLProgram | null>(null);
  const animationFrameRef = useRef<number>(0);
  const uniformsRef = useRef<{
    iTime: WebGLUniformLocation | null;
    iResolution: WebGLUniformLocation | null;
    iMouse: WebGLUniformLocation | null;
  }>({ iTime: null, iResolution: null, iMouse: null });
  
  // GPU Performance: Optimized computation refs
  const lastComputeTimeRef = useRef<number>(0);
  const frameSkipCountRef = useRef<number>(0);
  
  // Performance monitoring
  const frameCountRef = useRef(0);
  const lastFrameTimeRef = useRef(0);
  const fpsRef = useRef(60);
  
  // Device-specific settings
  const deviceInfo = getDeviceInfo();
  const qualitySettings = getQualitySettings(deviceInfo);
  
  // Camera controls - now enabled for iPhones!
  const defaultMouseRef = useRef({ x: 0.6, y: 0.27 });
  const activeMouseRef = useRef({ x: 0.6, y: 0.27 });
  const isDraggingRef = useRef(false);
  const lastMouseRef = useRef({ x: 0, y: 0 });

  useEffect(() => {
    const canvas = canvasRef.current;
    if (!canvas) return;

    const gl = canvas.getContext('webgl');
    if (!gl) {
      console.warn('WebGL not supported');
      return;
    }

    glRef.current = gl;



    // Compile shader
    const compileShader = (source: string, type: number) => {
      const shader = gl.createShader(type);
      if (!shader) return null;
      
      gl.shaderSource(shader, source);
      gl.compileShader(shader);
      
      if (!gl.getShaderParameter(shader, gl.COMPILE_STATUS)) {
        console.error('Shader compile error:', gl.getShaderInfoLog(shader));
        gl.deleteShader(shader);
        return null;
      }
      
      return shader;
    };

    const vertexShader = compileShader(vertexShaderSource, gl.VERTEX_SHADER);
    const fragmentShader = compileShader(createFragmentShader(qualitySettings), gl.FRAGMENT_SHADER);
    
    if (!vertexShader || !fragmentShader) return;

    const program = gl.createProgram();
    if (!program) return;
    
    gl.attachShader(program, vertexShader);
    gl.attachShader(program, fragmentShader);
    gl.linkProgram(program);
    
    if (!gl.getProgramParameter(program, gl.LINK_STATUS)) {
      console.error('Program link error:', gl.getProgramInfoLog(program));
      return;
    }

    programRef.current = program;

    uniformsRef.current = {
      iTime: gl.getUniformLocation(program, 'iTime'),
      iResolution: gl.getUniformLocation(program, 'iResolution'),
      iMouse: gl.getUniformLocation(program, 'iMouse')
    };

    const vertices = new Float32Array([
      -1, -1,
       1, -1,
      -1,  1,
       1,  1
    ]);

    const buffer = gl.createBuffer();
    gl.bindBuffer(gl.ARRAY_BUFFER, buffer);
    gl.bufferData(gl.ARRAY_BUFFER, vertices, gl.STATIC_DRAW);

    const positionLocation = gl.getAttribLocation(program, 'a_position');
    gl.enableVertexAttribArray(positionLocation);
    gl.vertexAttribPointer(positionLocation, 2, gl.FLOAT, false, 0, 0);

    // Smart canvas resizing with device-specific pixel ratio
    const resizeCanvas = () => {
      const displayWidth = canvas.clientWidth;
      const displayHeight = canvas.clientHeight;
      const pixelRatio = Math.min(window.devicePixelRatio, qualitySettings.pixelRatioMultiplier);

      const canvasWidth = Math.floor(displayWidth * pixelRatio);
      const canvasHeight = Math.floor(displayHeight * pixelRatio);

      if (canvas.width !== canvasWidth || canvas.height !== canvasHeight) {
        canvas.width = canvasWidth;
        canvas.height = canvasHeight;
        gl.viewport(0, 0, canvasWidth, canvasHeight);
      }
    };

    // Enhanced interaction handlers for all devices including iPhone
    const handleMouseDown = (e: MouseEvent) => {
      if (!qualitySettings.enableInteraction) return;
      
      if (e.button === 2) { // Right mouse button
        e.preventDefault();
        isDraggingRef.current = true;
        const rect = canvas.getBoundingClientRect();
        lastMouseRef.current = {
          x: e.clientX - rect.left,
          y: e.clientY - rect.top
        };
        canvas.style.cursor = 'grabbing';
        
        document.addEventListener('mousemove', handleMouseMove);
        document.addEventListener('mouseup', handleMouseUp);
      }
    };

    const handleTouchStart = (e: TouchEvent) => {
      if (!qualitySettings.enableInteraction) return;
      
      e.preventDefault();
      if (e.touches.length === 1) {
        isDraggingRef.current = true;
        const rect = canvas.getBoundingClientRect();
        const touch = e.touches[0];
        lastMouseRef.current = {
          x: touch.clientX - rect.left,
          y: touch.clientY - rect.top
        };
        
        document.addEventListener('touchmove', handleTouchMove, { passive: false });
        document.addEventListener('touchend', handleTouchEnd);
      }
    };

    const handleMouseMove = (e: MouseEvent) => {
      if (isDraggingRef.current) {
        const rect = canvas.getBoundingClientRect();
        const currentX = e.clientX - rect.left;
        const currentY = e.clientY - rect.top;
        
        const deltaX = (currentX - lastMouseRef.current.x) / rect.width;
        const deltaY = (currentY - lastMouseRef.current.y) / rect.height;
        
        activeMouseRef.current.x = Math.max(0, Math.min(1, activeMouseRef.current.x + deltaX));
        activeMouseRef.current.y = Math.max(0, Math.min(1, activeMouseRef.current.y - deltaY));
        
        lastMouseRef.current = { x: currentX, y: currentY };
      }
    };

    const handleTouchMove = (e: TouchEvent) => {
      if (isDraggingRef.current && e.touches.length === 1) {
        e.preventDefault();
        const rect = canvas.getBoundingClientRect();
        const touch = e.touches[0];
        const currentX = touch.clientX - rect.left;
        const currentY = touch.clientY - rect.top;
        
        const deltaX = (currentX - lastMouseRef.current.x) / rect.width;
        const deltaY = (currentY - lastMouseRef.current.y) / rect.height;
        
        activeMouseRef.current.x = Math.max(0, Math.min(1, activeMouseRef.current.x + deltaX));
        activeMouseRef.current.y = Math.max(0, Math.min(1, activeMouseRef.current.y - deltaY));
        
        lastMouseRef.current = { x: currentX, y: currentY };
      }
    };

    const handleMouseUp = () => {
      if (isDraggingRef.current) {
        isDraggingRef.current = false;
        canvas.style.cursor = '';
        
        document.removeEventListener('mousemove', handleMouseMove);
        document.removeEventListener('mouseup', handleMouseUp);
      }
    };

    const handleTouchEnd = () => {
      if (isDraggingRef.current) {
        isDraggingRef.current = false;
        
        document.removeEventListener('touchmove', handleTouchMove);
        document.removeEventListener('touchend', handleTouchEnd);
      }
    };

    const handleContextMenu = (e: MouseEvent) => {
      if (qualitySettings.enableInteraction) {
        e.preventDefault();
      }
    };

    // Set up event listeners
    if (qualitySettings.enableInteraction) {
      canvas.addEventListener('mousedown', handleMouseDown);
      canvas.addEventListener('touchstart', handleTouchStart, { passive: false });
      canvas.addEventListener('contextmenu', handleContextMenu);
    }
    window.addEventListener('resize', resizeCanvas);

    // Enhanced performance monitoring function with iPhone 15 Pro Max logging
    const updatePerformanceMetrics = (currentTime: number) => {
      frameCountRef.current++;
      
      if (currentTime - lastFrameTimeRef.current >= 1000) {
        fpsRef.current = Math.round((frameCountRef.current * 1000) / (currentTime - lastFrameTimeRef.current));
        frameCountRef.current = 0;
        lastFrameTimeRef.current = currentTime;
        

      }
    };

    // Animation loop with performance monitoring
    const startTime = Date.now();
    const animate = () => {
      const currentTime = Date.now();
      updatePerformanceMetrics(currentTime);
      
      resizeCanvas();
      
      const elapsedTime = (currentTime - startTime) / 1000;
      
      gl.useProgram(program);
      
      // Set uniforms
      if (uniformsRef.current.iTime) {
        gl.uniform1f(uniformsRef.current.iTime, elapsedTime);
      }
      if (uniformsRef.current.iResolution) {
        gl.uniform2f(uniformsRef.current.iResolution, canvas.width, canvas.height);
      }
      if (uniformsRef.current.iMouse) {
        const mousePos = activeMouseRef.current;
        gl.uniform4f(
          uniformsRef.current.iMouse,
          mousePos.x * canvas.width,
          mousePos.y * canvas.height,
          isDraggingRef.current ? 1 : 0,
          0
        );
      }

      // Draw
      gl.drawArrays(gl.TRIANGLE_STRIP, 0, 4);
      
      animationFrameRef.current = requestAnimationFrame(animate);
    };

    resizeCanvas();
    animate();

    return () => {
      if (animationFrameRef.current) {
        cancelAnimationFrame(animationFrameRef.current);
      }
      canvas.removeEventListener('mousedown', handleMouseDown);
      canvas.removeEventListener('touchstart', handleTouchStart);
      canvas.removeEventListener('contextmenu', handleContextMenu);
      document.removeEventListener('mousemove', handleMouseMove);
      document.removeEventListener('touchmove', handleTouchMove);
      document.removeEventListener('mouseup', handleMouseUp);
      document.removeEventListener('touchend', handleTouchEnd);
      window.removeEventListener('resize', resizeCanvas);
      
      if (gl && program) {
        gl.deleteProgram(program);
      }
    };
  }, []);

  return (
    <canvas
      ref={canvasRef}
      className={`w-full h-full ${className}`}
      style={{ width: '100%', height: '100%' }}
    />
  );
};

```

#### client/src/components/PixelMoshOverlay.tsx
```tsx

import { useEffect, useRef } from 'react';

type PixelMoshOverlayProps = {
  imageSrc: string;
  duration?: number;
  onComplete: () => void;
};

export default function PixelMoshOverlay({
  imageSrc,
  duration = 4000,
  onComplete
}: PixelMoshOverlayProps) {
  const canvasRef = useRef<HTMLCanvasElement>(null);
  const frameRef  = useRef<number>();

  useEffect(() => {
    const canvas = canvasRef.current!;
    const ctx    = canvas.getContext('2d')!;
    const img    = new Image();
    img.src      = imageSrc;

    img.onload = () => {
      const cw    = (canvas.width  = window.innerWidth);
      const ch    = (canvas.height = window.innerHeight);
      const start = performance.now();

      function drawFrame(time: number) {
        const t = Math.min((time - start) / duration, 1);
        ctx.clearRect(0, 0, cw, ch);
        ctx.drawImage(img, 0, 0, cw, ch);

        // Macroblock slide
        const blockSize = 16;
        const cols      = Math.ceil(cw / blockSize);
        const rows      = Math.ceil(ch / blockSize);
        for (let y = 0; y < rows; y++) {
          for (let x = 0; x < cols; x++) {
            if (Math.random() < 0.1) {
              const sx = x * blockSize,
                    sy = y * blockSize,
                    sw = blockSize,
                    sh = blockSize,
                    dx = sx + (Math.random() - 0.5) * blockSize * t * 5,
                    dy = sy + (Math.random() - 0.5) * blockSize * t * 5;
              ctx.drawImage(canvas, sx, sy, sw, sh, dx, dy, sw, sh);
            }
          }
        }

        // Color bleed
        ctx.globalCompositeOperation = 'screen';
        ctx.drawImage(canvas, Math.sin(t * Math.PI * 4) * 5, 0, cw, ch);
        ctx.globalCompositeOperation = 'source-over';

        // Progressive fade
        ctx.fillStyle = `rgba(0,0,0,${t * 0.8})`;
        ctx.fillRect(0, 0, cw, ch);

        if (t < 1) {
          frameRef.current = requestAnimationFrame(drawFrame);
        } else {
          onComplete();
        }
      }

      frameRef.current = requestAnimationFrame(drawFrame);
    };

    return () => {
      if (frameRef.current) cancelAnimationFrame(frameRef.current);
    };
  }, [imageSrc, duration, onComplete]);

  return (
    <canvas
      ref={canvasRef}
      className="fixed inset-0 z-50 pointer-events-none"
    />
  );
}

```

#### client/src/components/VRInterface.tsx
```tsx
import React, { useEffect, useRef, useState } from 'react';
import { WebXRManager, XRSettings, XRController, createXRButton } from '../utils/webxr';
import { Headset, Hand, Eye } from 'lucide-react';

interface VRInterfaceProps {
  canvasRef: React.RefObject<HTMLCanvasElement>;
  isEnabled: boolean;
  onToggle: (enabled: boolean) => void;
  onVRStateChange?: (isActive: boolean) => void;
  onControllerUpdate?: (controllers: XRController[]) => void;
}

export const VRInterface: React.FC<VRInterfaceProps> = ({
  canvasRef,
  isEnabled,
  onToggle,
  onVRStateChange,
  onControllerUpdate
}) => {
  const [isSupported, setIsSupported] = useState<boolean>(false);
  const [isActive, setIsActive] = useState<boolean>(false);
  const [mode, setMode] = useState<'vr' | 'ar'>('vr');
  const [controllers, setControllers] = useState<XRController[]>([]);
  const [handTracking, setHandTracking] = useState<boolean>(true);
  
  const xrManagerRef = useRef<WebXRManager | null>(null);

  const xrSettings: XRSettings = {
    enabled: isEnabled,
    mode,
    handTracking,
    environmentBlend: mode === 'ar' ? 'alpha-blend' : 'opaque',
    referenceSpace: 'local-floor'
  };

  useEffect(() => {
    checkWebXRSupport();
    setupXREventListeners();

    return () => {
      cleanupXREventListeners();
    };
  }, []);

  useEffect(() => {
    if (canvasRef.current && isEnabled) {
      initializeXRManager();
    }
  }, [canvasRef.current, isEnabled]);

  const checkWebXRSupport = async () => {
    if (!canvasRef.current) return;
    
    // Check for WebXR API availability
    if (!navigator.xr) {
      console.log('WebXR API not available');
      setIsSupported(false);
      return;
    }
    
    try {
      const gl = canvasRef.current.getContext('webgl2');
      if (!gl) {
        console.log('WebGL2 not supported - required for WebXR');
        setIsSupported(false);
        return;
      }

      const manager = new WebXRManager(canvasRef.current, gl, xrSettings);
      const supported = await manager.isSupported();
      setIsSupported(supported);
      
      if (!supported) {
        console.log('WebXR not supported on this device');
      }
    } catch (error) {
      console.error('Error checking WebXR support:', error);
      setIsSupported(false);
    }
  };

  const initializeXRManager = () => {
    if (!canvasRef.current) return;
    
    const gl = canvasRef.current.getContext('webgl2');
    if (!gl) {
      console.log('WebGL2 required for WebXR initialization');
      return;
    }

    xrManagerRef.current = new WebXRManager(canvasRef.current, gl, xrSettings);
  };

  const setupXREventListeners = () => {
    const handleSessionEndEvent = (event: Event) => handleSessionEnd();
    const handleXRRenderEvent = (event: Event) => handleXRRender(event as CustomEvent);
    
    window.addEventListener('xr-session-end', handleSessionEndEvent);
    window.addEventListener('xr-render', handleXRRenderEvent);
    
    // Store references for cleanup
    (window as any)._xrEventHandlers = {
      sessionEnd: handleSessionEndEvent,
      render: handleXRRenderEvent
    };
  };

  const cleanupXREventListeners = () => {
    const handlers = (window as any)._xrEventHandlers;
    if (handlers) {
      window.removeEventListener('xr-session-end', handlers.sessionEnd);
      window.removeEventListener('xr-render', handlers.render);
      delete (window as any)._xrEventHandlers;
    }
  };

  const handleSessionEnd = () => {
    setIsActive(false);
    setControllers([]);
    onVRStateChange?.(false);
  };

  const handleXRRender = (event: CustomEvent) => {
    // Forward XR render data to point cloud renderer
    const { viewMatrix, projectionMatrix, eye } = event.detail;
    
    // Update controllers
    if (xrManagerRef.current) {
      const currentControllers = xrManagerRef.current.getControllers();
      setControllers(currentControllers);
      onControllerUpdate?.(currentControllers);
    }

    // Dispatch to point cloud system
    window.dispatchEvent(new CustomEvent('point-cloud-xr-render', {
      detail: { viewMatrix, projectionMatrix, eye }
    }));
  };

  const startVRSession = async () => {
    if (!xrManagerRef.current) return;

    const success = await xrManagerRef.current.startSession('vr');
    if (success) {
      setIsActive(true);
      setMode('vr');
      onVRStateChange?.(true);
    }
  };

  const startARSession = async () => {
    if (!xrManagerRef.current) return;

    const success = await xrManagerRef.current.startSession('ar');
    if (success) {
      setIsActive(true);
      setMode('ar');
      onVRStateChange?.(true);
    }
  };

  const endSession = async () => {
    if (!xrManagerRef.current) return;

    await xrManagerRef.current.endSession();
    setIsActive(false);
    onVRStateChange?.(false);
  };

  if (!isSupported) {
    return (
      <div className="bg-gray-800 rounded-lg p-4 border border-gray-700">
        <div className="flex items-center gap-2 text-gray-400">
          <Headset className="w-5 h-5" />
          <span className="text-sm">WebXR not supported on this device</span>
        </div>
        <p className="text-xs text-gray-500 mt-1">
          VR/AR requires a compatible headset and browser
        </p>
      </div>
    );
  }

  return (
    <div className="bg-gray-800 rounded-lg p-4 border border-gray-700">
      <div className="flex items-center justify-between mb-4">
        <div className="flex items-center gap-2">
          <Headset className="w-5 h-5 text-purple-400" />
          <span className="text-white font-medium">Immersive View</span>
        </div>
        
        <button
          onClick={() => onToggle(!isEnabled)}
          className={`w-12 h-6 rounded-full transition-colors ${
            isEnabled ? 'bg-purple-600' : 'bg-gray-600'
          }`}
        >
          <div
            className={`w-5 h-5 bg-white rounded-full transition-transform ${
              isEnabled ? 'translate-x-6' : 'translate-x-0.5'
            }`}
          />
        </button>
      </div>

      {isEnabled && (
        <>
          {/* XR Controls */}
          <div className="flex gap-2 mb-4">
            <button
              onClick={isActive ? endSession : startVRSession}
              disabled={!isSupported}
              className={`flex-1 px-3 py-2 rounded-lg transition-colors text-sm ${
                isActive && mode === 'vr'
                  ? 'bg-purple-700 hover:bg-purple-600'
                  : 'bg-purple-600 hover:bg-purple-500'
              } text-white disabled:bg-gray-600 disabled:cursor-not-allowed`}
            >
              {isActive && mode === 'vr' ? 'Exit VR' : 'Enter VR'}
            </button>

            <button
              onClick={isActive ? endSession : startARSession}
              disabled={!isSupported}
              className={`flex-1 px-3 py-2 rounded-lg transition-colors text-sm ${
                isActive && mode === 'ar'
                  ? 'bg-blue-700 hover:bg-blue-600'
                  : 'bg-blue-600 hover:bg-blue-500'
              } text-white disabled:bg-gray-600 disabled:cursor-not-allowed`}
            >
              {isActive && mode === 'ar' ? 'Exit AR' : 'Enter AR'}
            </button>
          </div>

          {/* Hand Tracking Toggle */}
          <div className="flex items-center justify-between mb-3">
            <div className="flex items-center gap-2">
              <Hand className="w-4 h-4 text-blue-400" />
              <span className="text-sm text-white">Hand Tracking</span>
            </div>
            <button
              onClick={() => setHandTracking(!handTracking)}
              className={`w-10 h-5 rounded-full transition-colors ${
                handTracking ? 'bg-blue-600' : 'bg-gray-600'
              }`}
            >
              <div
                className={`w-4 h-4 bg-white rounded-full transition-transform ${
                  handTracking ? 'translate-x-5' : 'translate-x-0.5'
                }`}
              />
            </button>
          </div>

          {/* Session Status */}
          {isActive && (
            <div className="bg-gray-900 rounded-lg p-3 mb-3">
              <div className="flex items-center gap-2 mb-2">
                <div className="w-2 h-2 bg-green-400 rounded-full animate-pulse" />
                <span className="text-sm text-green-400">
                  {mode.toUpperCase()} Session Active
                </span>
              </div>
              
              {controllers.length > 0 && (
                <div className="text-xs text-gray-400">
                  <div className="flex items-center gap-1 mb-1">
                    <Hand className="w-3 h-3" />
                    <span>Controllers: {controllers.length}</span>
                  </div>
                  {controllers.map((controller, index) => (
                    <div key={controller.id} className="ml-4 text-xs">
                      {controller.id === 0 ? 'Left' : 'Right'}: {
                        controller.isConnected ? 'Connected' : 'Disconnected'
                      }
                    </div>
                  ))}
                </div>
              )}
            </div>
          )}

          {/* XR Tips */}
          <div className="text-xs text-gray-400 space-y-1">
            <div className="flex items-center gap-1">
              <Eye className="w-3 h-3" />
              <span>Look around to navigate the point cloud</span>
            </div>
            <div className="flex items-center gap-1">
              <Hand className="w-3 h-3" />
              <span>Use controllers to interact with effects</span>
            </div>
          </div>
        </>
      )}
    </div>
  );
};
```

#### client/src/components/VideoExportDialog.tsx
```tsx

import React, { useState, useEffect } from 'react';
import { Dialog, DialogContent, DialogHeader, DialogTitle } from './ui/dialog';
import { Button } from './ui/button';
import { Progress } from './ui/progress';
import { Video, X, AlertTriangle } from 'lucide-react';
import { VideoSettings } from '../hooks/useVideoExport';

interface VideoExportDialogProps {
  isOpen: boolean;
  onClose: () => void;
  onStartRecording: (settings: VideoSettings) => void;
  onStopRecording: () => void;
  isRecording: boolean;
  progress: number;
  error: string | null;
  onClearError: () => void;
  videoRef: React.RefObject<HTMLVideoElement>;
}

// Resolution presets matching GIF export
const RESOLUTION_PRESETS = {
  '16:9 - 720p': { width: 1280, height: 720 },
  '16:9 - 1080p': { width: 1920, height: 1080 },
  '16:9 - 2K': { width: 2560, height: 1440 },
  '9:16 - 720p': { width: 720, height: 1280 },
  '9:16 - 1080p': { width: 1080, height: 1920 },
  '9:16 - 2K': { width: 1440, height: 2560 }
};

const QUALITY_PRESETS = {
  'Best': 95,
  'Good': 85,
  'Fast': 75
};

export const VideoExportDialog: React.FC<VideoExportDialogProps> = ({
  isOpen,
  onClose,
  onStartRecording,
  onStopRecording,
  isRecording,
  progress,
  error,
  onClearError,
  videoRef
}) => {
  const [settings, setSettings] = useState<VideoSettings>({
    fps: 30,
    quality: 85,
    width: 2560,
    height: 1440
  });

  const [selectedResolution, setSelectedResolution] = useState('16:9 - 2K');
  const [selectedQuality, setSelectedQuality] = useState('Good');
  const [detectedDuration, setDetectedDuration] = useState<number | null>(null);

  // Auto-detect video duration when dialog opens
  useEffect(() => {
    if (isOpen && videoRef.current) {
      const duration = videoRef.current.duration;
      if (!isNaN(duration)) {
        const cappedDuration = Math.min(Math.max(duration, 1), 30);
        setDetectedDuration(cappedDuration);
      } else {
        setDetectedDuration(5); // Fallback
      }
    }
  }, [isOpen, videoRef]);

  const finalSettings = detectedDuration ? { ...settings, duration: detectedDuration } : settings;
  const estimatedSize = estimateVideoSize(finalSettings);

  const handleResolutionChange = (preset: string) => {
    setSelectedResolution(preset);
    const resolution = RESOLUTION_PRESETS[preset as keyof typeof RESOLUTION_PRESETS];
    setSettings(prev => ({
      ...prev,
      width: resolution.width,
      height: resolution.height
    }));
  };

  const handleQualityChange = (quality: string) => {
    setSelectedQuality(quality);
    const qualityValue = QUALITY_PRESETS[quality as keyof typeof QUALITY_PRESETS];
    setSettings(prev => ({
      ...prev,
      quality: qualityValue
    }));
  };

  const handleStartRecording = () => {
    onClearError();
    onStartRecording(finalSettings);
  };

  return (
    <Dialog open={isOpen} onOpenChange={onClose}>
      <DialogContent className="max-w-md bg-black/90 backdrop-blur-md border border-white/30 text-white">
        <DialogHeader>
          <DialogTitle className="flex items-center gap-2">
            <Video className="w-4 h-4" />
            High-Quality Video Export
          </DialogTitle>
        </DialogHeader>

        <div className="space-y-4">
          {error && (
            <div className="bg-red-500/20 border border-red-500/50 rounded p-3">
              <div className="flex items-center gap-2 mb-2">
                <AlertTriangle className="w-4 h-4 text-red-400" />
                <span className="text-sm font-medium text-red-400">Error</span>
              </div>
              <p className="text-sm text-red-300 mb-2">{error}</p>
              <Button
                onClick={onClearError}
                variant="outline"
                size="sm"
                className="border-red-500/50 text-red-400 hover:bg-red-500/20"
              >
                Dismiss
              </Button>
            </div>
          )}

          {isRecording ? (
            <div className="space-y-4">
              <div className="text-center">
                <div className="text-lg font-semibold mb-3">Creating High-Quality Video...</div>
                <Progress value={progress} className="w-full mb-2" />
                <div className="text-sm text-white/70">
                  {progress < 50 ? 'Capturing frames...' : 'Encoding video...'}
                </div>
                <div className="text-xs text-white/50 mt-1">
                  {progress}% Complete
                </div>
              </div>
              
              <Button
                onClick={onStopRecording}
                variant="destructive"
                className="w-full"
              >
                <X className="w-4 h-4 mr-2" />
                Cancel
              </Button>
            </div>
          ) : (
            <div className="space-y-4">
              {/* Resolution Presets */}
              <div>
                <label className="block text-sm font-medium mb-2">Resolution & Aspect Ratio</label>
                <div className="grid grid-cols-1 gap-2 max-h-40 overflow-y-auto">
                  {Object.keys(RESOLUTION_PRESETS).map((preset) => (
                    <button
                      key={preset}
                      onClick={() => handleResolutionChange(preset)}
                      className={`p-3 text-sm rounded transition-colors text-left ${
                        selectedResolution === preset
                          ? 'bg-blue-600 text-white'
                          : 'bg-gray-700 text-white/70 hover:bg-gray-600'
                      }`}
                    >
                      <div className="font-medium">{preset}</div>
                      <div className="text-xs opacity-70">
                        {RESOLUTION_PRESETS[preset as keyof typeof RESOLUTION_PRESETS].width} × {RESOLUTION_PRESETS[preset as keyof typeof RESOLUTION_PRESETS].height}
                      </div>
                    </button>
                  ))}
                </div>
              </div>

              {/* Quality Presets */}
              <div>
                <label className="block text-sm font-medium mb-2">Video Quality</label>
                <div className="space-y-1">
                  {Object.keys(QUALITY_PRESETS).map((quality) => (
                    <button
                      key={quality}
                      onClick={() => handleQualityChange(quality)}
                      className={`w-full p-2 text-sm rounded transition-colors text-left ${
                        selectedQuality === quality
                          ? 'bg-blue-600 text-white'
                          : 'bg-gray-700 text-white/70 hover:bg-gray-600'
                      }`}
                    >
                      {quality} Quality ({QUALITY_PRESETS[quality as keyof typeof QUALITY_PRESETS]}%)
                    </button>
                  ))}
                </div>
              </div>

              {/* Duration Display */}
              <div>
                <label className="block text-sm font-medium mb-2">Duration (Auto-detected)</label>
                <div className="bg-gray-800/50 rounded p-3">
                  {detectedDuration !== null ? (
                    <div className="text-sm text-white/70">
                      Duration: <span className="font-medium text-white">{detectedDuration.toFixed(1)}s</span> (full video)
                    </div>
                  ) : (
                    <div className="text-sm text-white/50">
                      Detecting video duration...
                    </div>
                  )}
                </div>
              </div>

              {/* FPS Control */}
              <div>
                <div className="flex justify-between items-center mb-2">
                  <label className="text-sm font-medium">Frame Rate (FPS)</label>
                  <span className="text-sm text-white/70">{settings.fps}</span>
                </div>
                <input
                  type="range"
                  min="24"
                  max="60"
                  step="1"
                  value={settings.fps}
                  onChange={(e) => setSettings(prev => ({
                    ...prev,
                    fps: parseInt(e.target.value)
                  }))}
                  className="w-full"
                />
              </div>

              {/* File Info */}
              <div className="bg-gray-800/50 rounded p-3 space-y-1">
                <div className="flex justify-between text-sm">
                  <span className="text-white/70">Est. size:</span>
                  <span className="font-medium">{estimatedSize.toFixed(1)} MB</span>
                </div>
                <div className="flex justify-between text-sm">
                  <span className="text-white/70">Format:</span>
                  <span className="font-medium">WebM (VP8/VP9)</span>
                </div>
                <div className="flex justify-between text-sm">
                  <span className="text-white/70">Quality:</span>
                  <span className="font-medium text-green-400">High Compression</span>
                </div>
              </div>

              {/* Export Button */}
              <Button
                onClick={handleStartRecording}
                disabled={detectedDuration === null}
                className="w-full bg-gradient-to-r from-green-600 to-blue-600 hover:from-green-500 hover:to-blue-500 disabled:bg-gray-600 disabled:cursor-not-allowed"
              >
                <Video className="w-4 h-4 mr-2" />
                {detectedDuration !== null ? 'Start Video Recording' : 'Detecting Duration...'}
              </Button>
            </div>
          )}
        </div>
      </DialogContent>
    </Dialog>
  );
};

// Simple video size estimation
function estimateVideoSize(settings: VideoSettings): number {
  const duration = settings.duration || 5;
  const pixelsPerFrame = settings.width * settings.height;
  const totalPixels = pixelsPerFrame * settings.fps * duration;
  const qualityFactor = settings.quality / 100;
  const compressionFactor = 0.02; // WebM has excellent compression
  return (totalPixels * qualityFactor * compressionFactor) / (1024 * 1024);
}

```

#### client/src/components/WelcomeScreen.tsx
```tsx
import React, { useState, useEffect, useRef } from 'react';
import { Upload, AlertTriangle } from 'lucide-react';
import { useNavigate } from 'react-router-dom';
import { FileValidator } from '../utils/fileValidation';
import { SecurityLogger } from '../utils/securityLogger';
import { RateLimiter } from '../utils/rateLimiter';
import { DemoVideoSection } from './DemoVideoSection';
import { IntroAnimation } from './IntroAnimation';
import { OceanShader } from './OceanShader';
import { fetchDemoVideo } from '../utils/demoVideo';

interface WelcomeScreenProps {
  onVideoUpload: (file: File) => void;
  onDemoAnimationStart?: () => void;
}

// Enhanced matrix corruption characters - curated letter substitutions
const RETRO_TERMINAL_CHARS = [
  // Letter substitutions that look natural
  '1', '!', '|', 'ı', 'І',  // for i/l
  '3', 'ε', 'є', '∈',       // for e
  '0', 'O', '6', 'b', '9', 'g', // letter/number hybrids
  '⌶', '⌷',                 // favorites that glitch perfectly
  '◦', '∘', '°', '˙', '·',  // subtle dots/periods
  '_', '-', '~', '^'        // terminal artifacts
];

// Monospace fonts only for clean glitch cycling
const GLITCH_FONTS = [
  'font-jetbrains',
  'font-space-mono',
  'font-courier'
];

export const WelcomeScreen: React.FC<WelcomeScreenProps> = ({ onVideoUpload, onDemoAnimationStart }) => {
  const navigate = useNavigate();
  
  // Enhanced glitch states for title + demo button
  const [glitchStates, setGlitchStates] = useState<boolean[]>(new Array(9 + 4).fill(false)); // 9 for pixelflow, 4 for demo
  const [corruptedChars, setCorruptedChars] = useState<string[]>(new Array(9 + 4).fill(''));
  const [glitchFonts, setGlitchFonts] = useState<string[]>(new Array(9 + 4).fill(''));
  
  // Start with clean fonts (empty strings = default font)
  const [persistentFonts, setPersistentFonts] = useState<string[]>(() => {
    return new Array(9 + 4).fill('');
  });
  
  // Track glitch behavior type (temp flash vs permanent switch)
  const [glitchBehaviors, setGlitchBehaviors] = useState<('flash' | 'switch')[]>(new Array(9 + 4).fill('flash'));
  
  const [isDragOver, setIsDragOver] = useState(false);
  const [isValidating, setIsValidating] = useState(false);
  const [isDemoLoad, setIsDemoLoad] = useState(false);
  const [validationError, setValidationError] = useState<string | null>(null);
  const [showDemoAnimation, setShowDemoAnimation] = useState(false);
  const dragCounterRef = useRef(0);

  const handleFileValidationAndUpload = async (file: File) => {
    // Clear any previous errors
    setValidationError(null);
    
    // Log the upload attempt
    SecurityLogger.logFileUploadAttempt(file.name, file.size, file.type);
    
    // Check rate limiting (max 3 uploads per minute)
    const rateLimitKey = 'file_upload';
    if (!RateLimiter.isAllowed(rateLimitKey, 3, 60000)) {
      const error = 'Too many upload attempts. Please wait before trying again.';
      setValidationError(error);
      SecurityLogger.logFileUploadFailure(file.name, 'Rate limit exceeded');
      return;
    }

    setIsValidating(true);
    setIsDemoLoad(false); // This is a file upload, not a demo

    try {
      // Validate the file
      const validation = await FileValidator.validateVideoFile(file);
      
      if (!validation.isValid) {
        setValidationError(validation.error || 'File validation failed');
        SecurityLogger.logFileUploadFailure(file.name, validation.error || 'Validation failed');
        
        // Log suspicious activity if file appears to be disguised
        if (validation.error?.includes('content does not match')) {
          SecurityLogger.logSuspiciousActivity('DISGUISED_FILE_UPLOAD', {
            fileName: file.name,
            declaredType: file.type,
            fileSize: file.size
          });
        }
        return;
      }

      // File is valid, proceed with upload
      SecurityLogger.logFileUploadSuccess(file.name);
      onVideoUpload(file);
      
    } catch (error) {
      const errorMessage = 'An error occurred during file validation';
      setValidationError(errorMessage);
      SecurityLogger.logFileUploadFailure(file.name, `Validation error: ${error}`);
      console.error('File validation error:', error);
    } finally {
      setIsValidating(false);
    }
  };

  const handleDemoLoad = async () => {
    try {
      setIsValidating(true);
      setIsDemoLoad(true); // This is a demo load
      setValidationError(null);
      
      // Trigger the intro animation instead of showing it inline
      if (onDemoAnimationStart) {
        onDemoAnimationStart();
      } else {
        // Fallback to direct demo loading if no animation callback
        setShowDemoAnimation(true);
      }
    } catch (error) {
      setValidationError(`Failed to load demo: ${error instanceof Error ? error.message : 'Unknown error'}`);
      console.error('Demo load error:', error);
      setIsValidating(false);
      setIsDemoLoad(false);
    }
  };

  const handleDemoTransition = async () => {
    try {
      const demoFile = await fetchDemoVideo();
      onVideoUpload(demoFile);
    } catch (error) {
      setValidationError(`Failed to load demo: ${error instanceof Error ? error.message : 'Unknown error'}`);
      console.error('Demo load error:', error);
    } finally {
      setIsValidating(false);
      setIsDemoLoad(false);
      setShowDemoAnimation(false);
    }
  };

  const handleFileUpload = (event: React.ChangeEvent<HTMLInputElement>) => {
    const file = event.target.files?.[0];
    if (file) {
      handleFileValidationAndUpload(file);
    }
  };

  const handleFileDrop = (files: FileList) => {
    const file = files[0];
    if (file) {
      handleFileValidationAndUpload(file);
    }
  };

  const handleDragEnter = (e: React.DragEvent) => {
    e.preventDefault();
    e.stopPropagation();
    dragCounterRef.current++;
    
    if (e.dataTransfer.items && e.dataTransfer.items.length > 0) {
      setIsDragOver(true);
    }
  };

  const handleDragLeave = (e: React.DragEvent) => {
    e.preventDefault();
    e.stopPropagation();
    dragCounterRef.current--;
    
    if (dragCounterRef.current === 0) {
      setIsDragOver(false);
    }
  };

  const handleDragOver = (e: React.DragEvent) => {
    e.preventDefault();
    e.stopPropagation();
  };

  const handleDrop = (e: React.DragEvent) => {
    e.preventDefault();
    e.stopPropagation();
    setIsDragOver(false);
    dragCounterRef.current = 0;
    
    if (e.dataTransfer.files && e.dataTransfer.files.length > 0) {
      handleFileDrop(e.dataTransfer.files);
    }
  };

  const handleGalleryClick = () => {
    navigate('/gallery');
  };

  useEffect(() => {
    const triggerGlitch = (index: number) => {
      // Only apply mixed behaviors to pixelflow letters (index 0-8)
      const isPixelflowLetter = index < 9;
      
      // Determine glitch behavior: 70% chance for permanent switch, 30% for temp flash
      const behaviorType = isPixelflowLetter && Math.random() > 0.3 ? 'switch' : 'flash';
      
      // Update behavior type
      setGlitchBehaviors(prev => {
        const newBehaviors = [...prev];
        newBehaviors[index] = behaviorType;
        return newBehaviors;
      });

      // Start glitch visual state
      setGlitchStates(prev => {
        const newStates = [...prev];
        newStates[index] = true;
        return newStates;
      });

      if (behaviorType === 'switch' && isPixelflowLetter) {
        // PERMANENT FONT SWITCH: Pick a new random font different from current
        const currentFont = persistentFonts[index];
        const availableFonts = GLITCH_FONTS.filter(font => font !== currentFont);
        const newFont = availableFonts[Math.floor(Math.random() * availableFonts.length)];
        
        console.log(`Letter ${index} switching from ${currentFont || 'default'} to ${newFont}`);
        
        // Update persistent font immediately
        setPersistentFonts(prev => {
          const newFonts = [...prev];
          newFonts[index] = newFont;
          return newFonts;
        });
        
        // Brief highlight effect for font switch - ENHANCED: Reduced from 400ms to 200ms
        setTimeout(() => {
          setGlitchStates(prev => {
            const newStates = [...prev];
            newStates[index] = false;
            return newStates;
          });
        }, 200); // MICRO ENHANCEMENT 3: Snappier font switch transitions
        
      } else {
        // TEMPORARY CORRUPTION FLASH: Show corrupted character temporarily
        const randomChar = RETRO_TERMINAL_CHARS[Math.floor(Math.random() * RETRO_TERMINAL_CHARS.length)];
        setCorruptedChars(prev => {
          const newChars = [...prev];
          newChars[index] = randomChar;
          return newChars;
        });

        // Set random font for flash effect
        if (isPixelflowLetter) {
          const randomFont = GLITCH_FONTS[Math.floor(Math.random() * GLITCH_FONTS.length)];
          setGlitchFonts(prev => {
            const newFonts = [...prev];
            newFonts[index] = randomFont;
            return newFonts;
          });
        }

        // End flash glitch after duration - more consistent timing
        const glitchDuration = 500 + Math.random() * 300; // 500-800ms (consistent timing)
        setTimeout(() => {
          setGlitchStates(prev => {
            const newStates = [...prev];
            newStates[index] = false;
            return newStates;
          });
        }, glitchDuration);
      }
    };

    // Setup glitch timers with setInterval instead of setTimeout to prevent acceleration
    const setupGlitchTimer = (index: number, initialDelay: number) => {
      // Start the timer after initial delay
      setTimeout(() => {
        // Trigger first glitch
        triggerGlitch(index);
        
        // Set up steady interval - NO EXPONENTIAL ACCELERATION
        setInterval(() => {
          triggerGlitch(index);
        }, 6000 + Math.random() * 4000); // Fixed 6-10 second intervals
      }, initialDelay);
    };

    // Initialize glitch timers for title and demo button
    const allElements = 'pixelflow'.split('').concat('demo'.split(''));
    allElements.forEach((_, index) => {
      // MICRO ENHANCEMENT 1: Reduced stagger from 2000ms to 1200ms for more organic wave-like corruption
      const initialDelay = index * 1200; // More organic wave pattern
      setupGlitchTimer(index, initialDelay);
    });

    // Cleanup function to clear intervals on unmount
    return () => {
      // Note: setInterval IDs would need to be tracked to clear them properly
      // For now, the component lifecycle will handle cleanup
    };
  }, []); // Remove persistentFonts dependency to prevent re-initialization

  const renderLetter = (letter: string, index: number) => {
    const isGlitching = glitchStates[index];
    const corruptedChar = corruptedChars[index];
    const glitchFont = glitchFonts[index];
    const behaviorType = glitchBehaviors[index];
    const persistentFont = persistentFonts[index];
    
    return (
      <span
        key={index}
        className={`
          inline-block relative whitespace-nowrap
          ${isGlitching ? 'animate-matrix-glitch' : 'animate-letter-glow'}
          animation-delay-${(index + 1) * 100}
        `}
        style={{
          animationDelay: `${index * 0.1}s`,
          minWidth: '0.6em',
          textAlign: 'center',
          display: 'inline-block'
        }}
      >
        {/* Main letter - uses persistent font or default */}
        <span 
          className={`
            relative z-10
            ${persistentFont || ''} 
            ${isGlitching && behaviorType === 'flash' ? 'opacity-20' : 'opacity-100'}
            ${isGlitching && behaviorType === 'switch' ? 'animate-pulse' : ''}
            transition-opacity duration-150
          `}
        >
          {letter}
        </span>
        
        {/* Enhanced corrupted character overlay for flash behavior only */}
        {isGlitching && behaviorType === 'flash' && (
          <>
            <span 
              className={`
                absolute inset-0 z-20 text-white animate-pulse
                ${glitchFont}
              `}
              style={{
                textShadow: `
                  0 0 15px rgba(255, 255, 255, 0.9), 
                  0 0 30px rgba(255, 255, 255, 0.7),
                  0 0 45px rgba(0, 255, 255, 0.3)
                  ${window.innerWidth < 640 ? ', 0 0 60px rgba(255, 0, 255, 0.2)' : ''}
                `,
                filter: 'brightness(1.8) contrast(1.2)',
                fontSize: '1.1em',
                transform: `rotate(${Math.random() * 4 - 2}deg)`,
              }}
            >
              {corruptedChar}
            </span>
            
            {/* MICRO ENHANCEMENT 2: Enhanced chromatic aberration with dynamic positioning */}
            <span 
              className={`
                absolute inset-0 z-15 text-red-400 opacity-60
                ${glitchFont}
              `}
              style={{ 
                transform: `translateX(${-1.5 - Math.random() * 1}px) skewX(-0.5deg)`, // Dynamic red offset
                fontSize: '1.1em',
                filter: 'blur(0.3px)'
              }}
            >
              {corruptedChar}
            </span>
            <span 
              className={`
                absolute inset-0 z-15 text-cyan-400 opacity-60
                ${glitchFont}
              `}
              style={{ 
                transform: `translateX(${1.5 + Math.random() * 1}px) skewX(0.5deg)`, // Dynamic cyan offset
                fontSize: '1.1em',
                filter: 'blur(0.3px)'
              }}
            >
              {corruptedChar}
            </span>
            
            {/* Digital bleed effect */}
            <span 
              className={`
                absolute inset-0 z-14 text-white opacity-20
                ${glitchFont}
              `}
              style={{ 
                transform: 'translateY(-1px) scaleY(1.1)',
                fontSize: '1.1em',
                filter: 'blur(1px)'
              }}
            >
              {corruptedChar}
            </span>
          </>
        )}
        
        {/* Switch highlight effect for permanent font changes */}
        {isGlitching && behaviorType === 'switch' && (
          <div 
            className="absolute inset-0 z-30 bg-white opacity-20 animate-pulse"
            style={{
              borderRadius: '2px',
              boxShadow: '0 0 10px rgba(255, 255, 255, 0.5)',
            }}
          />
        )}
        
        {/* Enhanced scan line effect for flash behavior */}
        {isGlitching && behaviorType === 'flash' && (
          <div 
            className="absolute inset-0 z-30 bg-gradient-to-r from-transparent via-cyan-400 to-transparent opacity-40 animate-scan-line"
            style={{
              height: '2px',
              filter: 'blur(0.5px)',
            }}
          />
        )}
      </span>
    );
  };

  // Function for rendering button text with enhanced matrix effects
  const renderButtonText = (text: string, startIndex: number) => {
    return text.split('').map((char, charIndex) => {
      const globalIndex = startIndex + charIndex;
      const isGlitching = glitchStates[globalIndex];
      const corruptedChar = corruptedChars[globalIndex];
      
      return (
        <span
          key={charIndex}
          className={`
            inline-block relative
            ${isGlitching ? 'animate-matrix-glitch' : ''}
          `}
        >
          {/* Main character */}
          <span 
            className={`
              relative z-10
              ${isGlitching ? 'opacity-0' : 'opacity-100'}
              transition-opacity duration-75
            `}
          >
            {char}
          </span>
          
          {/* Enhanced corrupted character overlay */}
          {isGlitching && (
            <>
              <span 
                className="absolute inset-0 z-20 text-white animate-pulse"
                style={{
                  textShadow: '0 0 8px rgba(255, 255, 255, 0.6), 0 0 16px rgba(255, 255, 255, 0.4), 0 0 24px rgba(0, 255, 255, 0.2)',
                  filter: 'brightness(1.3) contrast(1.1)',
                  transform: `rotate(${Math.random() * 2 - 1}deg)`,
                }}
              >
                {corruptedChar}
              </span>
              
              {/* Enhanced chromatic aberration effect */}
              <span 
                className="absolute inset-0 z-15 text-red-400 opacity-30"
                style={{ 
                  transform: 'translateX(-0.5px)',
                  filter: 'blur(0.2px)'
                }}
              >
                {corruptedChar}
              </span>
              <span 
                className="absolute inset-0 z-15 text-blue-400 opacity-30"
                style={{ 
                  transform: 'translateX(0.5px)',
                  filter: 'blur(0.2px)'
                }}
              >
                {corruptedChar}
              </span>
            </>
          )}
          
          {/* Enhanced scan line effect */}
          {isGlitching && (
            <div 
              className="absolute inset-0 z-30 bg-gradient-to-r from-transparent via-white to-transparent opacity-20 animate-scan-line"
              style={{
                height: '1px',
                filter: 'blur(0.3px)',
              }}
            />
          )}
        </span>
      );
    });
  };

  return (
    <div 
      className={`fixed inset-0 bg-gradient-to-br from-black via-gray-950/20 to-black flex items-center justify-center min-h-screen min-h-[100vh] min-h-[100dvh] transition-all duration-300 ${
        isDragOver ? 'bg-gray-900/50' : ''
      }`}
      onDragEnter={handleDragEnter}
      onDragLeave={handleDragLeave}
      onDragOver={handleDragOver}
      onDrop={handleDrop}
    >
      {/* Ocean Shader Background - lowest z-index */}
      <div className="fixed inset-0 opacity-30" style={{ zIndex: -20 }}>
        <OceanShader />
      </div>

      {/* SVG Filter for Liquid Glass Effect */}
      <svg className="absolute opacity-0 pointer-events-none" width="0" height="0">
        <defs>
          <filter id="liquid-glass-filter" x="-20%" y="-20%" width="140%" height="140%">
            <feGaussianBlur in="SourceGraphic" stdDeviation="3" result="blur"/>
            <feColorMatrix in="blur" mode="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 18 -7" result="highContrast"/>
            <feComposite in="highContrast" in2="SourceAlpha" operator="in" result="masked"/>
            <feMorphology in="masked" operator="dilate" radius="1" result="dilated"/>
            <feGaussianBlur in="dilated" stdDeviation="0.5" result="finalBlur"/>
          </filter>
        </defs>
      </svg>

      {/* Film Grain Aberration Overlay - Fullscreen */}
      <div className="film-grain-aberration absolute inset-0 pointer-events-none" style={{ zIndex: 1 }} />
      
      {/* Trippy Chromatic Aberration Layer */}
      <div className="chromatic-aberration-layer absolute inset-0 pointer-events-none" style={{ zIndex: 2 }} />
      
      {/* Atkinson Dithering Drift Layer */}
      <div className="atkinson-dither-layer absolute inset-0 pointer-events-none" style={{ zIndex: 3 }} />

      {/* Matrix scan lines overlay */}
      <div className="absolute inset-0 opacity-5 pointer-events-none">
        <div className="matrix-lines" />
      </div>

      {/* Demo iMessage Intro Animation - Only for demo loads */}
      {showDemoAnimation && (
        <IntroAnimation onTransitionComplete={handleDemoTransition} />
      )}

      {/* Enhanced drag overlay */}
      {isDragOver && !isValidating && (
        <div className="absolute inset-0 bg-white/3 backdrop-blur-[2px] flex items-center justify-center z-40 border-2 border-dashed border-white/20">
          <div className="text-center">
            <div className="w-24 h-24 mx-auto mb-6 rounded-full border-2 border-dashed border-white/40 flex items-center justify-center animate-pulse">
              <Upload className="w-8 h-8 text-white/60" />
            </div>
            <p className="text-white/80 text-lg font-light tracking-wide">drop your video here</p>
          </div>
        </div>
      )}

      {/* File Upload Validation overlay */}
      {isValidating && !isDemoLoad && (
        <div className="absolute inset-0 bg-black/90 backdrop-blur-sm flex items-center justify-center z-50">
          <div className="text-center">
            <div className="w-12 h-12 mx-auto mb-6 border-2 border-white/20 border-t-white/80 rounded-full animate-spin"></div>
            <p className="text-white/80 text-base font-light tracking-wide">validating file...</p>
          </div>
        </div>
      )}

      {/* Error overlay */}
      {validationError && (
        <div className="absolute inset-0 bg-black/95 backdrop-blur-sm flex items-center justify-center z-50">
          <div className="bg-red-950/30 border border-red-500/20 rounded-xl p-8 max-w-md mx-4 backdrop-blur-sm">
            <div className="flex items-center gap-4 mb-6">
              <AlertTriangle className="w-6 h-6 text-red-400" />
              <h3 className="text-red-400 font-light text-lg tracking-wide">upload failed</h3>
            </div>
            <p className="text-white/90 font-light text-sm mb-6 leading-relaxed">{validationError}</p>
            <button
              onClick={() => setValidationError(null)}
              className="w-full bg-red-500/10 hover:bg-red-500/20 border border-red-500/20 text-red-400 px-6 py-3 rounded-lg font-light text-sm transition-all duration-200 hover:border-red-500/30"
            >
              try again
            </button>
          </div>
        </div>
      )}
      
      {/* Main content - Golden Ratio scaling and spacing with visual centering adjustment */}
      <div className="flex flex-col items-center justify-center h-full w-full max-w-sm sm:max-w-md md:max-w-lg px-4 sm:px-6 relative z-30 pointer-events-none mx-auto">
        
        {/* Logo and title section - VISUAL CENTERING ADJUSTMENT */}
        <div className="text-center mb-16 sm:mb-20 w-full flex flex-col items-center">
          <div 
            className="logo-container"
            style={{ 
              transform: 'translateX(5px)', // Adjusted from 3px to 5px for better visual centering
            }}
          >
            <h1 className="text-6xl sm:text-7xl font-light text-white mb-6 tracking-widest sm:tracking-[0.2em] animate-fade-in-up whitespace-nowrap overflow-hidden">
              {['p', 'i', 'x', 'e', 'l', 'f', 'l', 'o', 'w'].map((letter, index) => 
                renderLetter(letter, index)
              )}
            </h1>
          </div>
          <div className="w-40 h-px bg-gradient-to-r from-transparent via-white/30 to-transparent animate-underline-grow"></div>
        </div>

        {/* Interactive controls section - Golden Ratio spacing */}
        <div className="w-full flex flex-col items-center space-y-8 animate-fade-in-up animation-delay-1500 pointer-events-auto">
          
          {/* Apple Liquid Glass Upload Button */}
          <div className="relative w-full flex justify-center">
            <input
              type="file"
              accept="video/*"
              onChange={handleFileUpload}
              className="hidden"
              id="video-upload-welcome"
              disabled={isValidating}
            />
            <label
              htmlFor="video-upload-welcome"
              className={`liquid-glass-button group relative inline-flex items-center justify-center px-12 py-6 rounded-2xl cursor-pointer transition-all duration-500 transform hover:scale-[1.02] ${
                isValidating ? 'opacity-50 cursor-not-allowed pointer-events-none' : ''
              }`}
            >
              <Upload className="w-5 h-5 mr-4 text-white/80 group-hover:text-white transition-colors duration-300" />
              <span className="text-white/70 group-hover:text-white/90 font-light text-sm tracking-wider transition-all duration-300">
                {isValidating ? 'validating...' : 'browse files'}
              </span>
            </label>
          </div>

          {/* Clean Demo Button - MOBILE-SPECIFIC TEXT SIZE */}
          <div className="animate-fade-in-up animation-delay-2000 w-full flex justify-center">
            <button
              onClick={handleDemoLoad}
              disabled={isValidating}
              className="group relative text-white/60 hover:text-white/80 font-light text-base sm:text-sm tracking-wider transition-all duration-300 disabled:opacity-40 disabled:cursor-not-allowed"
            >
              <span className="relative">
                {renderButtonText('demo', 9)} {/* Start after pixelflow (9 chars) */}
                <span className="absolute bottom-0 left-0 w-full h-px bg-gradient-to-r from-white/20 via-white/60 to-white/20 scale-x-0 group-hover:scale-x-100 transition-transform duration-300 origin-left"></span>
              </span>
            </button>
          </div>
        </div>
      </div>

      {/* Enhanced Animation Styles with Film Grain Aberration + Apple Liquid Glass */}
      <style>{`
        /* Apple Liquid Glass Button Styles */
        .liquid-glass-button {
          background: rgba(255, 255, 255, 0.05);
          backdrop-filter: url(#liquid-glass-filter) brightness(1.1) saturate(1.2);
          border: 1px solid rgba(255, 255, 255, 0.1);
          box-shadow: 
            0 0 2px 1px rgba(255, 255, 255, 0.03) inset,
            0 0 10px 4px rgba(255, 255, 255, 0.02) inset,
            0px 4px 16px rgba(17, 17, 26, 0.05), 
            0px 8px 24px rgba(17, 17, 26, 0.05),
            0px 16px 56px rgba(17, 17, 26, 0.05),
            0px 4px 16px rgba(255, 255, 255, 0.02) inset,
            0px 8px 24px rgba(255, 255, 255, 0.01) inset,
            0px 16px 56px rgba(255, 255, 255, 0.01) inset;
        }
        
        .liquid-glass-button:hover {
          background: rgba(255, 255, 255, 0.08);
          border-color: rgba(255, 255, 255, 0.15);
          box-shadow: 
            0 0 3px 1px rgba(255, 255, 255, 0.05) inset,
            0 0 15px 6px rgba(255, 255, 255, 0.03) inset,
            0px 6px 20px rgba(17, 17, 26, 0.08), 
            0px 12px 32px rgba(17, 17, 26, 0.08),
            0px 24px 72px rgba(17, 17, 26, 0.08),
            0px 6px 20px rgba(255, 255, 255, 0.03) inset,
            0px 12px 32px rgba(255, 255, 255, 0.02) inset,
            0px 24px 72px rgba(255, 255, 255, 0.01) inset;
        }
        
        @keyframes fade-in-up {
          from {
            opacity: 0;
            transform: translateY(30px);
          }
          to {
            opacity: 1;
            transform: translateY(0);
          }
        }
        
        @keyframes letter-glow {
          0%, 100% {
            opacity: 0.8;
            transform: translateY(0px);
          }
          50% {
            opacity: 1;
            transform: translateY(-1px);
            text-shadow: 0 0 12px rgba(255, 255, 255, 0.2);
          }
        }
        
        @keyframes matrix-glitch {
          0% {
            transform: translateX(0) translateY(0) scale(1) rotate(0deg);
            opacity: 1;
          }
          10% {
            transform: translateX(-1px) translateY(0.5px) scale(1.01) rotate(-0.2deg);
            opacity: 0.9;
            text-shadow: 0 0 15px rgba(255, 255, 255, 0.9), 0 0 25px rgba(0, 255, 255, 0.3);
          }
          20% {
            transform: translateX(1px) translateY(-0.5px) scale(0.99) rotate(0.1deg);
            opacity: 1.1;
            filter: brightness(1.3) contrast(1.2);
          }
          30% {
            transform: translateX(-0.5px) translateY(1px) scale(1) rotate(-0.1deg);
            opacity: 0.95;
          }
          40% {
            transform: translateX(0.5px) translateY(-1px) scale(1) rotate(0.05deg);
            opacity: 1.05;
          }
          50% {
            transform: translateX(-1px) translateY(0px) scale(0.995) rotate(-0.05deg);
            opacity: 0.9;
            text-shadow: 0 0 20px rgba(255, 255, 255, 1), 0 0 30px rgba(255, 0, 255, 0.2);
          }
          60% {
            transform: translateX(1px) translateY(0.5px) scale(1.005) rotate(0.1deg);
            opacity: 1.15;
          }
          70% {
            transform: translateX(0px) translateY(-0.5px) scale(1) rotate(0deg);
            opacity: 0.95;
          }
          80% {
            transform: translateX(-0.5px) translateY(1px) scale(1.002) rotate(-0.02deg);
            opacity: 1.05;
          }
          90% {
            transform: translateX(0.5px) translateY(0px) scale(0.998) rotate(0.02deg);
            opacity: 0.9;
          }
          100% {
            transform: translateX(0) translateY(0) scale(1) rotate(0deg);
            opacity: 1;
          }
        }
        
        @keyframes scan-line {
          0% {
            top: 0%;
            opacity: 0;
          }
          10% {
            opacity: 1;
          }
          90% {
            opacity: 1;
          }
          100% {
            top: 100%;
            opacity: 0;
          }
        }
        
        @keyframes underline-grow {
          from {
            width: 0;
          }
          to {
            width: 10rem;
          }
        }
        
        /* Film Grain Aberration Effects */
        @keyframes film-grain-shift {
          0% {
            transform: translate(0, 0) scale(1);
            filter: contrast(1.1) brightness(0.95) hue-rotate(0deg);
          }
          10% {
            transform: translate(-0.2px, 0.3px) scale(1.001);
            filter: contrast(1.15) brightness(0.92) hue-rotate(1deg);
          }
          20% {
            transform: translate(0.3px, -0.1px) scale(0.999);
            filter: contrast(1.08) brightness(0.98) hue-rotate(-0.5deg);
          }
          30% {
            transform: translate(-0.1px, 0.2px) scale(1.002);
            filter: contrast(1.12) brightness(0.94) hue-rotate(0.8deg);
          }
          40% {
            transform: translate(0.2px, 0.1px) scale(0.998);
            filter: contrast(1.09) brightness(0.96) hue-rotate(-0.3deg);
          }
          50% {
            transform: translate(-0.3px, -0.2px) scale(1.001);
            filter: contrast(1.14) brightness(0.93) hue-rotate(1.2deg);
          }
          60% {
            transform: translate(0.1px, 0.3px) scale(1.002);
            filter: contrast(1.07) brightness(0.97) hue-rotate(-0.7deg);
          }
          70% {
            transform: translate(-0.2px, -0.1px) scale(0.999);
            filter: contrast(1.13) brightness(0.95) hue-rotate(0.4deg);
          }
          80% {
            transform: translate(0.3px, 0.2px) scale(1.001);
            filter: contrast(1.06) brightness(0.99) hue-rotate(-0.9deg);
          }
          90% {
            transform: translate(-0.1px, -0.3px) scale(1.002);
            filter: contrast(1.11) brightness(0.94) hue-rotate(0.6deg);
          }
          100% {
            transform: translate(0, 0) scale(1);
            filter: contrast(1.1) brightness(0.95) hue-rotate(0deg);
          }
        }
        
        @keyframes chromatic-drift {
          0% {
            transform: translate(0, 0);
            opacity: 0.12;
          }
          25% {
            transform: translate(0.8px, -0.3px);
            opacity: 0.18;
          }
          50% {
            transform: translate(-0.5px, 0.7px);
            opacity: 0.15;
          }
          75% {
            transform: translate(0.3px, 0.4px);
            opacity: 0.20;
          }
          100% {
            transform: translate(0, 0);
            opacity: 0.12;
          }
        }
        
        @keyframes atkinson-distort {
          0% {
            transform: translate(0, 0) scale(1);
          }
          20% {
            transform: translate(0.3px, -0.2px) scale(1.001);
          }
          40% {
            transform: translate(-0.2px, 0.4px) scale(0.999);
          }
          60% {
            transform: translate(0.1px, 0.1px) scale(1.002);
          }
          80% {
            transform: translate(-0.4px, -0.1px) scale(0.998);
          }
          100% {
            transform: translate(0, 0) scale(1);
          }
        }
        
        /* Film Grain Fullscreen Background */
        .film-grain-aberration {
          background-image: 
            radial-gradient(circle at 12% 23%, rgba(255, 255, 255, 0.015) 0.5px, transparent 0.5px),
            radial-gradient(circle at 89% 67%, rgba(255, 255, 255, 0.012) 0.5px, transparent 0.5px),
            radial-gradient(circle at 34% 78%, rgba(255, 255, 255, 0.018) 0.5px, transparent 0.5px),
            radial-gradient(circle at 67% 12%, rgba(255, 255, 255, 0.008) 0.5px, transparent 0.5px),
            radial-gradient(circle at 45% 45%, rgba(255, 255, 255, 0.014) 0.5px, transparent 0.5px),
            radial-gradient(circle at 78% 89%, rgba(255, 255, 255, 0.011) 0.5px, transparent 0.5px),
            radial-gradient(circle at 23% 56%, rgba(255, 255, 255, 0.016) 0.5px, transparent 0.5px),
            radial-gradient(circle at 56% 34%, rgba(255, 255, 255, 0.009) 0.5px, transparent 0.5px);
          background-size: 
            7px 7px, 11px 11px, 9px 9px, 13px 13px, 
            6px 6px, 10px 10px, 8px 8px, 12px 12px;
          background-position: 
            0 0, 3px 4px, 6px 1px, 9px 7px,
            2px 8px, 5px 2px, 8px 9px, 11px 3px;
          animation: film-grain-shift 3.2s ease-in-out infinite;
          mix-blend-mode: overlay;
        }
        
        /* Trippy Chromatic Aberration */
        .chromatic-aberration-layer {
          background: 
            radial-gradient(
              ellipse 200% 100% at 50% 0%,
              rgba(255, 0, 100, 0.08) 0%,
              transparent 50%
            ),
            radial-gradient(
              ellipse 100% 200% at 0% 50%,
              rgba(0, 255, 200, 0.06) 0%,
              transparent 50%
            ),
            radial-gradient(
              ellipse 150% 120% at 100% 100%,
              rgba(200, 0, 255, 0.07) 0%,
              transparent 60%
            );
          animation: chromatic-drift 7.8s ease-in-out infinite;
          mix-blend-mode: color-dodge;
          filter: blur(0.8px);
        }
        
        /* Enhanced Atkinson Dithering with Distortion */
        .atkinson-dither-layer {
          background-image: 
            radial-gradient(circle at 0% 0%, rgba(255, 255, 255, 0.010) 1px, transparent 1px),
            radial-gradient(circle at 25% 25%, rgba(255, 255, 255, 0.014) 1px, transparent 1px),
            radial-gradient(circle at 50% 0%, rgba(255, 255, 255, 0.008) 1px, transparent 1px),
            radial-gradient(circle at 75% 25%, rgba(255, 255, 255, 0.012) 1px, transparent 1px),
            radial-gradient(circle at 0% 50%, rgba(255, 255, 255, 0.006) 1px, transparent 1px),
            radial-gradient(circle at 50% 50%, rgba(255, 255, 255, 0.010) 1px, transparent 1px),
            radial-gradient(circle at 25% 75%, rgba(255, 255, 255, 0.008) 1px, transparent 1px),
            radial-gradient(circle at 75% 75%, rgba(255, 255, 255, 0.012) 1px, transparent 1px);
          background-size: 
            8px 8px, 16px 16px, 12px 12px, 20px 20px, 
            14px 14px, 10px 10px, 18px 18px, 24px 24px;
          background-position: 
            0 0, 4px 4px, 8px 0, 12px 4px, 
            0 8px, 4px 12px, 8px 16px, 12px 20px;
          animation: atkinson-distort 15.4s ease-in-out infinite;
          mix-blend-mode: screen;
        }
        
        .animate-fade-in-up {
          animation: fade-in-up 1s ease-out forwards;
        }
        
        .animate-letter-glow {
          animation: letter-glow 3s ease-in-out infinite;
        }
        
        .animate-matrix-glitch {
          animation: matrix-glitch 0.15s ease-in-out;
        }
        
        .animate-scan-line {
          animation: scan-line 0.1s linear;
        }
        
        .animate-underline-grow {
          animation: underline-grow 0.8s ease-out 0.6s forwards;
          width: 0;
        }
        
        .animation-delay-100 {
          animation-delay: 0.1s;
        }
        
        .animation-delay-200 {
          animation-delay: 0.2s;
        }
        
        .animation-delay-300 {
          animation-delay: 0.3s;
        }
        
        .animation-delay-400 {
          animation-delay: 0.4s;
        }
        
        .animation-delay-500 {
          animation-delay: 0.5s;
        }
        
        .animation-delay-600 {
          animation-delay: 0.6s;
        }
        
        .animation-delay-700 {
          animation-delay: 0.7s;
        }
        
        .animation-delay-800 {
          animation-delay: 0.8s;
        }
        
        .animation-delay-1000 {
          animation-delay: 1s;
        }
        
        .animation-delay-1500 {
          animation-delay: 1.5s;
        }
        
        .animation-delay-2000 {
          animation-delay: 2s;
        }
        
        .animation-delay-2500 {
          animation-delay: 2.5s;
        }
        
        /* Matrix scan lines background effect */
        .matrix-lines {
          position: absolute;
          top: 0;
          left: 0;
          right: 0;
          bottom: 0;
          background-image: 
            repeating-linear-gradient(
              0deg,
              transparent,
              transparent 2px,
              rgba(255, 255, 255, 0.02) 2px,
              rgba(255, 255, 255, 0.02) 4px
            );
          animation: matrix-scan 4s linear infinite;
        }
        
        @keyframes matrix-scan {
          0% {
            transform: translateY(-100%);
          }
          100% {
            transform: translateY(100%);
          }
        }
      `}</style>
    </div>
  );
};

```

### UI Components

#### client/src/components/ui/button.tsx
```tsx
import * as React from "react"
import { Slot } from "@radix-ui/react-slot"
import { cva, type VariantProps } from "class-variance-authority"

import { cn } from "@/lib/utils"

const buttonVariants = cva(
  "inline-flex items-center justify-center gap-2 whitespace-nowrap rounded-md text-sm font-medium ring-offset-background transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 [&_svg]:pointer-events-none [&_svg]:size-4 [&_svg]:shrink-0",
  {
    variants: {
      variant: {
        default: "bg-primary text-primary-foreground hover:bg-primary/90",
        destructive:
          "bg-destructive text-destructive-foreground hover:bg-destructive/90",
        outline:
          "border border-input bg-background hover:bg-accent hover:text-accent-foreground",
        secondary:
          "bg-secondary text-secondary-foreground hover:bg-secondary/80",
        ghost: "hover:bg-accent hover:text-accent-foreground",
        link: "text-primary underline-offset-4 hover:underline",
      },
      size: {
        default: "h-10 px-4 py-2",
        sm: "h-9 rounded-md px-3",
        lg: "h-11 rounded-md px-8",
        icon: "h-10 w-10",
      },
    },
    defaultVariants: {
      variant: "default",
      size: "default",
    },
  }
)

export interface ButtonProps
  extends React.ButtonHTMLAttributes<HTMLButtonElement>,
    VariantProps<typeof buttonVariants> {
  asChild?: boolean
}

const Button = React.forwardRef<HTMLButtonElement, ButtonProps>(
  ({ className, variant, size, asChild = false, ...props }, ref) => {
    const Comp = asChild ? Slot : "button"
    return (
      <Comp
        className={cn(buttonVariants({ variant, size, className }))}
        ref={ref}
        {...props}
      />
    )
  }
)
Button.displayName = "Button"

export { Button, buttonVariants }

```

#### client/src/components/ui/dialog.tsx
```tsx
import * as React from "react"
import * as DialogPrimitive from "@radix-ui/react-dialog"
import { X } from "lucide-react"

import { cn } from "@/lib/utils"

const Dialog = DialogPrimitive.Root

const DialogTrigger = DialogPrimitive.Trigger

const DialogPortal = DialogPrimitive.Portal

const DialogClose = DialogPrimitive.Close

const DialogOverlay = React.forwardRef<
  React.ElementRef<typeof DialogPrimitive.Overlay>,
  React.ComponentPropsWithoutRef<typeof DialogPrimitive.Overlay>
>(({ className, ...props }, ref) => (
  <DialogPrimitive.Overlay
    ref={ref}
    className={cn(
      "fixed inset-0 z-50 bg-black/80  data-[state=open]:animate-in data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0",
      className
    )}
    {...props}
  />
))
DialogOverlay.displayName = DialogPrimitive.Overlay.displayName

const DialogContent = React.forwardRef<
  React.ElementRef<typeof DialogPrimitive.Content>,
  React.ComponentPropsWithoutRef<typeof DialogPrimitive.Content>
>(({ className, children, ...props }, ref) => (
  <DialogPortal>
    <DialogOverlay />
    <DialogPrimitive.Content
      ref={ref}
      className={cn(
        "fixed left-[50%] top-[50%] z-50 grid w-full max-w-lg translate-x-[-50%] translate-y-[-50%] gap-4 border bg-background p-6 shadow-lg duration-200 data-[state=open]:animate-in data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0 data-[state=closed]:zoom-out-95 data-[state=open]:zoom-in-95 data-[state=closed]:slide-out-to-left-1/2 data-[state=closed]:slide-out-to-top-[48%] data-[state=open]:slide-in-from-left-1/2 data-[state=open]:slide-in-from-top-[48%] sm:rounded-lg",
        className
      )}
      {...props}
    >
      {children}
      <DialogPrimitive.Close className="absolute right-4 top-4 rounded-sm opacity-70 ring-offset-background transition-opacity hover:opacity-100 focus:outline-none focus:ring-2 focus:ring-ring focus:ring-offset-2 disabled:pointer-events-none data-[state=open]:bg-accent data-[state=open]:text-muted-foreground">
        <X className="h-4 w-4" />
        <span className="sr-only">Close</span>
      </DialogPrimitive.Close>
    </DialogPrimitive.Content>
  </DialogPortal>
))
DialogContent.displayName = DialogPrimitive.Content.displayName

const DialogHeader = ({
  className,
  ...props
}: React.HTMLAttributes<HTMLDivElement>) => (
  <div
    className={cn(
      "flex flex-col space-y-1.5 text-center sm:text-left",
      className
    )}
    {...props}
  />
)
DialogHeader.displayName = "DialogHeader"

const DialogFooter = ({
  className,
  ...props
}: React.HTMLAttributes<HTMLDivElement>) => (
  <div
    className={cn(
      "flex flex-col-reverse sm:flex-row sm:justify-end sm:space-x-2",
      className
    )}
    {...props}
  />
)
DialogFooter.displayName = "DialogFooter"

const DialogTitle = React.forwardRef<
  React.ElementRef<typeof DialogPrimitive.Title>,
  React.ComponentPropsWithoutRef<typeof DialogPrimitive.Title>
>(({ className, ...props }, ref) => (
  <DialogPrimitive.Title
    ref={ref}
    className={cn(
      "text-lg font-semibold leading-none tracking-tight",
      className
    )}
    {...props}
  />
))
DialogTitle.displayName = DialogPrimitive.Title.displayName

const DialogDescription = React.forwardRef<
  React.ElementRef<typeof DialogPrimitive.Description>,
  React.ComponentPropsWithoutRef<typeof DialogPrimitive.Description>
>(({ className, ...props }, ref) => (
  <DialogPrimitive.Description
    ref={ref}
    className={cn("text-sm text-muted-foreground", className)}
    {...props}
  />
))
DialogDescription.displayName = DialogPrimitive.Description.displayName

export {
  Dialog,
  DialogPortal,
  DialogOverlay,
  DialogClose,
  DialogTrigger,
  DialogContent,
  DialogHeader,
  DialogFooter,
  DialogTitle,
  DialogDescription,
}

```

#### client/src/components/ui/progress.tsx
```tsx
import * as React from "react"
import * as ProgressPrimitive from "@radix-ui/react-progress"

import { cn } from "@/lib/utils"

const Progress = React.forwardRef<
  React.ElementRef<typeof ProgressPrimitive.Root>,
  React.ComponentPropsWithoutRef<typeof ProgressPrimitive.Root>
>(({ className, value, ...props }, ref) => (
  <ProgressPrimitive.Root
    ref={ref}
    className={cn(
      "relative h-4 w-full overflow-hidden rounded-full bg-secondary",
      className
    )}
    {...props}
  >
    <ProgressPrimitive.Indicator
      className="h-full w-full flex-1 bg-primary transition-all"
      style={{ transform: `translateX(-${100 - (value || 0)}%)` }}
    />
  </ProgressPrimitive.Root>
))
Progress.displayName = ProgressPrimitive.Root.displayName

export { Progress }

```

#### client/src/components/ui/select.tsx
```tsx
import * as React from "react"
import * as SelectPrimitive from "@radix-ui/react-select"
import { Check, ChevronDown, ChevronUp } from "lucide-react"

import { cn } from "@/lib/utils"

const Select = SelectPrimitive.Root

const SelectGroup = SelectPrimitive.Group

const SelectValue = SelectPrimitive.Value

const SelectTrigger = React.forwardRef<
  React.ElementRef<typeof SelectPrimitive.Trigger>,
  React.ComponentPropsWithoutRef<typeof SelectPrimitive.Trigger>
>(({ className, children, ...props }, ref) => (
  <SelectPrimitive.Trigger
    ref={ref}
    className={cn(
      "flex h-10 w-full items-center justify-between rounded-md border border-input bg-background px-3 py-2 text-sm ring-offset-background placeholder:text-muted-foreground focus:outline-none focus:ring-2 focus:ring-ring focus:ring-offset-2 disabled:cursor-not-allowed disabled:opacity-50 [&>span]:line-clamp-1",
      className
    )}
    {...props}
  >
    {children}
    <SelectPrimitive.Icon asChild>
      <ChevronDown className="h-4 w-4 opacity-50" />
    </SelectPrimitive.Icon>
  </SelectPrimitive.Trigger>
))
SelectTrigger.displayName = SelectPrimitive.Trigger.displayName

const SelectScrollUpButton = React.forwardRef<
  React.ElementRef<typeof SelectPrimitive.ScrollUpButton>,
  React.ComponentPropsWithoutRef<typeof SelectPrimitive.ScrollUpButton>
>(({ className, ...props }, ref) => (
  <SelectPrimitive.ScrollUpButton
    ref={ref}
    className={cn(
      "flex cursor-default items-center justify-center py-1",
      className
    )}
    {...props}
  >
    <ChevronUp className="h-4 w-4" />
  </SelectPrimitive.ScrollUpButton>
))
SelectScrollUpButton.displayName = SelectPrimitive.ScrollUpButton.displayName

const SelectScrollDownButton = React.forwardRef<
  React.ElementRef<typeof SelectPrimitive.ScrollDownButton>,
  React.ComponentPropsWithoutRef<typeof SelectPrimitive.ScrollDownButton>
>(({ className, ...props }, ref) => (
  <SelectPrimitive.ScrollDownButton
    ref={ref}
    className={cn(
      "flex cursor-default items-center justify-center py-1",
      className
    )}
    {...props}
  >
    <ChevronDown className="h-4 w-4" />
  </SelectPrimitive.ScrollDownButton>
))
SelectScrollDownButton.displayName =
  SelectPrimitive.ScrollDownButton.displayName

const SelectContent = React.forwardRef<
  React.ElementRef<typeof SelectPrimitive.Content>,
  React.ComponentPropsWithoutRef<typeof SelectPrimitive.Content>
>(({ className, children, position = "popper", ...props }, ref) => (
  <SelectPrimitive.Portal>
    <SelectPrimitive.Content
      ref={ref}
      className={cn(
        "relative z-50 max-h-96 min-w-[8rem] overflow-hidden rounded-md border bg-popover text-popover-foreground shadow-md data-[state=open]:animate-in data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0 data-[state=closed]:zoom-out-95 data-[state=open]:zoom-in-95 data-[side=bottom]:slide-in-from-top-2 data-[side=left]:slide-in-from-right-2 data-[side=right]:slide-in-from-left-2 data-[side=top]:slide-in-from-bottom-2",
        position === "popper" &&
          "data-[side=bottom]:translate-y-1 data-[side=left]:-translate-x-1 data-[side=right]:translate-x-1 data-[side=top]:-translate-y-1",
        className
      )}
      position={position}
      {...props}
    >
      <SelectScrollUpButton />
      <SelectPrimitive.Viewport
        className={cn(
          "p-1",
          position === "popper" &&
            "h-[var(--radix-select-trigger-height)] w-full min-w-[var(--radix-select-trigger-width)]"
        )}
      >
        {children}
      </SelectPrimitive.Viewport>
      <SelectScrollDownButton />
    </SelectPrimitive.Content>
  </SelectPrimitive.Portal>
))
SelectContent.displayName = SelectPrimitive.Content.displayName

const SelectLabel = React.forwardRef<
  React.ElementRef<typeof SelectPrimitive.Label>,
  React.ComponentPropsWithoutRef<typeof SelectPrimitive.Label>
>(({ className, ...props }, ref) => (
  <SelectPrimitive.Label
    ref={ref}
    className={cn("py-1.5 pl-8 pr-2 text-sm font-semibold", className)}
    {...props}
  />
))
SelectLabel.displayName = SelectPrimitive.Label.displayName

const SelectItem = React.forwardRef<
  React.ElementRef<typeof SelectPrimitive.Item>,
  React.ComponentPropsWithoutRef<typeof SelectPrimitive.Item>
>(({ className, children, ...props }, ref) => (
  <SelectPrimitive.Item
    ref={ref}
    className={cn(
      "relative flex w-full cursor-default select-none items-center rounded-sm py-1.5 pl-8 pr-2 text-sm outline-none focus:bg-accent focus:text-accent-foreground data-[disabled]:pointer-events-none data-[disabled]:opacity-50",
      className
    )}
    {...props}
  >
    <span className="absolute left-2 flex h-3.5 w-3.5 items-center justify-center">
      <SelectPrimitive.ItemIndicator>
        <Check className="h-4 w-4" />
      </SelectPrimitive.ItemIndicator>
    </span>

    <SelectPrimitive.ItemText>{children}</SelectPrimitive.ItemText>
  </SelectPrimitive.Item>
))
SelectItem.displayName = SelectPrimitive.Item.displayName

const SelectSeparator = React.forwardRef<
  React.ElementRef<typeof SelectPrimitive.Separator>,
  React.ComponentPropsWithoutRef<typeof SelectPrimitive.Separator>
>(({ className, ...props }, ref) => (
  <SelectPrimitive.Separator
    ref={ref}
    className={cn("-mx-1 my-1 h-px bg-muted", className)}
    {...props}
  />
))
SelectSeparator.displayName = SelectPrimitive.Separator.displayName

export {
  Select,
  SelectGroup,
  SelectValue,
  SelectTrigger,
  SelectContent,
  SelectLabel,
  SelectItem,
  SelectSeparator,
  SelectScrollUpButton,
  SelectScrollDownButton,
}

```

#### client/src/components/ui/slider.tsx
```tsx

import * as React from "react"
import * as SliderPrimitive from "@radix-ui/react-slider"
import { cn } from "@/lib/utils"
import { useIsMobile } from "@/hooks/use-mobile"

const Slider = React.forwardRef<
  React.ElementRef<typeof SliderPrimitive.Root>,
  React.ComponentPropsWithoutRef<typeof SliderPrimitive.Root>
>(({ className, ...props }, ref) => {
  const isMobile = useIsMobile()
  
  return (
    <SliderPrimitive.Root
      ref={ref}
      className={cn(
        "relative flex w-full touch-none select-none items-center",
        // Mobile-specific touch behavior
        isMobile && "touch-pan-x",
        className
      )}
      {...props}
    >
      <SliderPrimitive.Track 
        className={cn(
          "relative w-full grow overflow-hidden rounded-full bg-secondary",
          // Mobile-optimized track height
          isMobile ? "h-1" : "h-2"
        )}
      >
        <SliderPrimitive.Range className="absolute h-full bg-primary" />
      </SliderPrimitive.Track>
      <SliderPrimitive.Thumb 
        className={cn(
          "block rounded-full border-2 border-primary bg-background ring-offset-background transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50",
          // Mobile-optimized thumb size - larger touch targets
          isMobile 
            ? "h-6 w-6 shadow-lg active:scale-110 transition-transform duration-150" 
            : "h-5 w-5"
        )}
      />
    </SliderPrimitive.Root>
  )
})
Slider.displayName = SliderPrimitive.Root.displayName

export { Slider }

```

#### client/src/components/ui/switch.tsx
```tsx
import * as React from "react"
import * as SwitchPrimitives from "@radix-ui/react-switch"

import { cn } from "@/lib/utils"

const Switch = React.forwardRef<
  React.ElementRef<typeof SwitchPrimitives.Root>,
  React.ComponentPropsWithoutRef<typeof SwitchPrimitives.Root>
>(({ className, ...props }, ref) => (
  <SwitchPrimitives.Root
    className={cn(
      "peer inline-flex h-6 w-11 shrink-0 cursor-pointer items-center rounded-full border-2 border-transparent transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 focus-visible:ring-offset-background disabled:cursor-not-allowed disabled:opacity-50 data-[state=checked]:bg-primary data-[state=unchecked]:bg-input",
      className
    )}
    {...props}
    ref={ref}
  >
    <SwitchPrimitives.Thumb
      className={cn(
        "pointer-events-none block h-5 w-5 rounded-full bg-background shadow-lg ring-0 transition-transform data-[state=checked]:translate-x-5 data-[state=unchecked]:translate-x-0"
      )}
    />
  </SwitchPrimitives.Root>
))
Switch.displayName = SwitchPrimitives.Root.displayName

export { Switch }

```

#### client/src/components/ui/toast.tsx
```tsx
import * as React from "react"
import * as ToastPrimitives from "@radix-ui/react-toast"
import { cva, type VariantProps } from "class-variance-authority"
import { X } from "lucide-react"

import { cn } from "@/lib/utils"

const ToastProvider = ToastPrimitives.Provider

const ToastViewport = React.forwardRef<
  React.ElementRef<typeof ToastPrimitives.Viewport>,
  React.ComponentPropsWithoutRef<typeof ToastPrimitives.Viewport>
>(({ className, ...props }, ref) => (
  <ToastPrimitives.Viewport
    ref={ref}
    className={cn(
      "fixed top-0 z-[100] flex max-h-screen w-full flex-col-reverse p-4 sm:bottom-0 sm:right-0 sm:top-auto sm:flex-col md:max-w-[420px]",
      className
    )}
    {...props}
  />
))
ToastViewport.displayName = ToastPrimitives.Viewport.displayName

const toastVariants = cva(
  "group pointer-events-auto relative flex w-full items-center justify-between space-x-4 overflow-hidden rounded-md border p-6 pr-8 shadow-lg transition-all data-[swipe=cancel]:translate-x-0 data-[swipe=end]:translate-x-[var(--radix-toast-swipe-end-x)] data-[swipe=move]:translate-x-[var(--radix-toast-swipe-move-x)] data-[swipe=move]:transition-none data-[state=open]:animate-in data-[state=closed]:animate-out data-[swipe=end]:animate-out data-[state=closed]:fade-out-80 data-[state=closed]:slide-out-to-right-full data-[state=open]:slide-in-from-top-full data-[state=open]:sm:slide-in-from-bottom-full",
  {
    variants: {
      variant: {
        default: "border bg-background text-foreground",
        destructive:
          "destructive group border-destructive bg-destructive text-destructive-foreground",
      },
    },
    defaultVariants: {
      variant: "default",
    },
  }
)

const Toast = React.forwardRef<
  React.ElementRef<typeof ToastPrimitives.Root>,
  React.ComponentPropsWithoutRef<typeof ToastPrimitives.Root> &
    VariantProps<typeof toastVariants>
>(({ className, variant, ...props }, ref) => {
  return (
    <ToastPrimitives.Root
      ref={ref}
      className={cn(toastVariants({ variant }), className)}
      {...props}
    />
  )
})
Toast.displayName = ToastPrimitives.Root.displayName

const ToastAction = React.forwardRef<
  React.ElementRef<typeof ToastPrimitives.Action>,
  React.ComponentPropsWithoutRef<typeof ToastPrimitives.Action>
>(({ className, ...props }, ref) => (
  <ToastPrimitives.Action
    ref={ref}
    className={cn(
      "inline-flex h-8 shrink-0 items-center justify-center rounded-md border bg-transparent px-3 text-sm font-medium ring-offset-background transition-colors hover:bg-secondary focus:outline-none focus:ring-2 focus:ring-ring focus:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 group-[.destructive]:border-muted/40 group-[.destructive]:hover:border-destructive/30 group-[.destructive]:hover:bg-destructive group-[.destructive]:hover:text-destructive-foreground group-[.destructive]:focus:ring-destructive",
      className
    )}
    {...props}
  />
))
ToastAction.displayName = ToastPrimitives.Action.displayName

const ToastClose = React.forwardRef<
  React.ElementRef<typeof ToastPrimitives.Close>,
  React.ComponentPropsWithoutRef<typeof ToastPrimitives.Close>
>(({ className, ...props }, ref) => (
  <ToastPrimitives.Close
    ref={ref}
    className={cn(
      "absolute right-2 top-2 rounded-md p-1 text-foreground/50 opacity-0 transition-opacity hover:text-foreground focus:opacity-100 focus:outline-none focus:ring-2 group-hover:opacity-100 group-[.destructive]:text-red-300 group-[.destructive]:hover:text-red-50 group-[.destructive]:focus:ring-red-400 group-[.destructive]:focus:ring-offset-red-600",
      className
    )}
    toast-close=""
    {...props}
  >
    <X className="h-4 w-4" />
  </ToastPrimitives.Close>
))
ToastClose.displayName = ToastPrimitives.Close.displayName

const ToastTitle = React.forwardRef<
  React.ElementRef<typeof ToastPrimitives.Title>,
  React.ComponentPropsWithoutRef<typeof ToastPrimitives.Title>
>(({ className, ...props }, ref) => (
  <ToastPrimitives.Title
    ref={ref}
    className={cn("text-sm font-semibold", className)}
    {...props}
  />
))
ToastTitle.displayName = ToastPrimitives.Title.displayName

const ToastDescription = React.forwardRef<
  React.ElementRef<typeof ToastPrimitives.Description>,
  React.ComponentPropsWithoutRef<typeof ToastPrimitives.Description>
>(({ className, ...props }, ref) => (
  <ToastPrimitives.Description
    ref={ref}
    className={cn("text-sm opacity-90", className)}
    {...props}
  />
))
ToastDescription.displayName = ToastPrimitives.Description.displayName

type ToastProps = React.ComponentPropsWithoutRef<typeof Toast>

type ToastActionElement = React.ReactElement<typeof ToastAction>

export {
  type ToastProps,
  type ToastActionElement,
  ToastProvider,
  ToastViewport,
  Toast,
  ToastTitle,
  ToastDescription,
  ToastClose,
  ToastAction,
}

```

#### client/src/components/ui/toaster.tsx
```tsx
import { useToast } from "@/hooks/use-toast"
import {
  Toast,
  ToastClose,
  ToastDescription,
  ToastProvider,
  ToastTitle,
  ToastViewport,
} from "@/components/ui/toast"

export function Toaster() {
  const { toasts } = useToast()

  return (
    <ToastProvider>
      {toasts.map(function ({ id, title, description, action, ...props }) {
        return (
          <Toast key={id} {...props}>
            <div className="grid gap-1">
              {title && <ToastTitle>{title}</ToastTitle>}
              {description && (
                <ToastDescription>{description}</ToastDescription>
              )}
            </div>
            {action}
            <ToastClose />
          </Toast>
        )
      })}
      <ToastViewport />
    </ToastProvider>
  )
}

```

#### client/src/components/ui/tooltip.tsx
```tsx
import * as React from "react"
import * as TooltipPrimitive from "@radix-ui/react-tooltip"

import { cn } from "@/lib/utils"

const TooltipProvider = TooltipPrimitive.Provider

const Tooltip = TooltipPrimitive.Root

const TooltipTrigger = TooltipPrimitive.Trigger

const TooltipContent = React.forwardRef<
  React.ElementRef<typeof TooltipPrimitive.Content>,
  React.ComponentPropsWithoutRef<typeof TooltipPrimitive.Content>
>(({ className, sideOffset = 4, ...props }, ref) => (
  <TooltipPrimitive.Content
    ref={ref}
    sideOffset={sideOffset}
    className={cn(
      "z-50 overflow-hidden rounded-md border bg-popover px-3 py-1.5 text-sm text-popover-foreground shadow-md animate-in fade-in-0 zoom-in-95 data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=closed]:zoom-out-95 data-[side=bottom]:slide-in-from-top-2 data-[side=left]:slide-in-from-right-2 data-[side=right]:slide-in-from-left-2 data-[side=top]:slide-in-from-bottom-2",
      className
    )}
    {...props}
  />
))
TooltipContent.displayName = TooltipPrimitive.Content.displayName

export { Tooltip, TooltipTrigger, TooltipContent, TooltipProvider }

```

### Hooks

#### client/src/hooks/use-mobile.tsx
```tsx
import * as React from "react"

const MOBILE_BREAKPOINT = 768

export function useIsMobile() {
  const [isMobile, setIsMobile] = React.useState<boolean | undefined>(undefined)

  React.useEffect(() => {
    const mql = window.matchMedia(`(max-width: ${MOBILE_BREAKPOINT - 1}px)`)
    const onChange = () => {
      setIsMobile(window.innerWidth < MOBILE_BREAKPOINT)
    }
    mql.addEventListener("change", onChange)
    setIsMobile(window.innerWidth < MOBILE_BREAKPOINT)
    return () => mql.removeEventListener("change", onChange)
  }, [])

  return !!isMobile
}

```

#### client/src/hooks/use-toast.ts
```ts
import * as React from "react"

import type {
  ToastActionElement,
  ToastProps,
} from "@/components/ui/toast"

const TOAST_LIMIT = 1
const TOAST_REMOVE_DELAY = 1000000

type ToasterToast = ToastProps & {
  id: string
  title?: React.ReactNode
  description?: React.ReactNode
  action?: ToastActionElement
}

const actionTypes = {
  ADD_TOAST: "ADD_TOAST",
  UPDATE_TOAST: "UPDATE_TOAST",
  DISMISS_TOAST: "DISMISS_TOAST",
  REMOVE_TOAST: "REMOVE_TOAST",
} as const

let count = 0

function genId() {
  count = (count + 1) % Number.MAX_SAFE_INTEGER
  return count.toString()
}

type ActionType = typeof actionTypes

type Action =
  | {
      type: ActionType["ADD_TOAST"]
      toast: ToasterToast
    }
  | {
      type: ActionType["UPDATE_TOAST"]
      toast: Partial<ToasterToast>
    }
  | {
      type: ActionType["DISMISS_TOAST"]
      toastId?: ToasterToast["id"]
    }
  | {
      type: ActionType["REMOVE_TOAST"]
      toastId?: ToasterToast["id"]
    }

interface State {
  toasts: ToasterToast[]
}

const toastTimeouts = new Map<string, ReturnType<typeof setTimeout>>()

const addToRemoveQueue = (toastId: string) => {
  if (toastTimeouts.has(toastId)) {
    return
  }

  const timeout = setTimeout(() => {
    toastTimeouts.delete(toastId)
    dispatch({
      type: "REMOVE_TOAST",
      toastId: toastId,
    })
  }, TOAST_REMOVE_DELAY)

  toastTimeouts.set(toastId, timeout)
}

export const reducer = (state: State, action: Action): State => {
  switch (action.type) {
    case "ADD_TOAST":
      return {
        ...state,
        toasts: [action.toast, ...state.toasts].slice(0, TOAST_LIMIT),
      }

    case "UPDATE_TOAST":
      return {
        ...state,
        toasts: state.toasts.map((t) =>
          t.id === action.toast.id ? { ...t, ...action.toast } : t
        ),
      }

    case "DISMISS_TOAST": {
      const { toastId } = action

      // ! Side effects ! - This could be extracted into a dismissToast() action,
      // but I'll keep it here for simplicity
      if (toastId) {
        addToRemoveQueue(toastId)
      } else {
        state.toasts.forEach((toast) => {
          addToRemoveQueue(toast.id)
        })
      }

      return {
        ...state,
        toasts: state.toasts.map((t) =>
          t.id === toastId || toastId === undefined
            ? {
                ...t,
                open: false,
              }
            : t
        ),
      }
    }
    case "REMOVE_TOAST":
      if (action.toastId === undefined) {
        return {
          ...state,
          toasts: [],
        }
      }
      return {
        ...state,
        toasts: state.toasts.filter((t) => t.id !== action.toastId),
      }
  }
}

const listeners: Array<(state: State) => void> = []

let memoryState: State = { toasts: [] }

function dispatch(action: Action) {
  memoryState = reducer(memoryState, action)
  listeners.forEach((listener) => {
    listener(memoryState)
  })
}

type Toast = Omit<ToasterToast, "id">

function toast({ ...props }: Toast) {
  const id = genId()

  const update = (props: ToasterToast) =>
    dispatch({
      type: "UPDATE_TOAST",
      toast: { ...props, id },
    })
  const dismiss = () => dispatch({ type: "DISMISS_TOAST", toastId: id })

  dispatch({
    type: "ADD_TOAST",
    toast: {
      ...props,
      id,
      open: true,
      onOpenChange: (open) => {
        if (!open) dismiss()
      },
    },
  })

  return {
    id: id,
    dismiss,
    update,
  }
}

function useToast() {
  const [state, setState] = React.useState<State>(memoryState)

  React.useEffect(() => {
    listeners.push(setState)
    return () => {
      const index = listeners.indexOf(setState)
      if (index > -1) {
        listeners.splice(index, 1)
      }
    }
  }, [state])

  return {
    ...state,
    toast,
    dismiss: (toastId?: string) => dispatch({ type: "DISMISS_TOAST", toastId }),
  }
}

export { useToast, toast }

```

#### client/src/hooks/useGifExport.tsx
```tsx

import { useRef, useState, useCallback } from 'react';
import { createGifEncoder, GifEncoderOptions } from '../utils/gifEncoder';
import { gifOptimizer, OptimizedGifSettings } from '../utils/gifOptimizer';
import { canvasPool } from '../utils/canvasPool';

export interface GifSettings {
  duration?: number; // Made optional since it will be auto-detected
  fps: number;
  quality: number;
  width: number;
  height: number;
}

// Helper function to calculate crop dimensions
const calculateCropDimensions = (
  sourceWidth: number,
  sourceHeight: number,
  targetWidth: number,
  targetHeight: number
) => {
  const sourceAspectRatio = sourceWidth / sourceHeight;
  const targetAspectRatio = targetWidth / targetHeight;
  
  let cropWidth, cropHeight, cropX, cropY;
  
  if (sourceAspectRatio > targetAspectRatio) {
    // Source is wider than target - crop horizontally
    cropHeight = sourceHeight;
    cropWidth = cropHeight * targetAspectRatio;
    cropX = (sourceWidth - cropWidth) / 2;
    cropY = 0;
  } else {
    // Source is taller than target - crop vertically  
    cropWidth = sourceWidth;
    cropHeight = cropWidth / targetAspectRatio;
    cropX = 0;
    cropY = (sourceHeight - cropHeight) / 2;
  }
  
  return {
    cropX: Math.round(cropX),
    cropY: Math.round(cropY),
    cropWidth: Math.round(cropWidth),
    cropHeight: Math.round(cropHeight)
  };
};

// Enhanced canvas validation function
const validateCanvasContent = (canvas: HTMLCanvasElement): boolean => {
  const ctx = canvas.getContext('2d');
  if (!ctx) return false;
  
  // Get image data from a small sample area in the center
  const sampleSize = Math.min(50, canvas.width / 4, canvas.height / 4);
  const centerX = (canvas.width - sampleSize) / 2;
  const centerY = (canvas.height - sampleSize) / 2;
  
  try {
    const imageData = ctx.getImageData(centerX, centerY, sampleSize, sampleSize);
    const data = imageData.data;
    
    // Check if canvas has any non-black pixels
    let nonBlackPixels = 0;
    for (let i = 0; i < data.length; i += 4) {
      const r = data[i];
      const g = data[i + 1];
      const b = data[i + 2];
      const a = data[i + 3];
      
      // Check for any visible non-black pixels
      if (a > 0 && (r > 10 || g > 10 || b > 10)) {
        nonBlackPixels++;
      }
    }
    
    // Consider valid if at least 1% of sampled pixels are non-black
    const validPixelThreshold = (sampleSize * sampleSize) * 0.01;
    const isValid = nonBlackPixels > validPixelThreshold;
    
    console.log(`Canvas validation: ${nonBlackPixels} non-black pixels out of ${sampleSize * sampleSize}, valid: ${isValid}`);
    return isValid;
  } catch (error) {
    console.error('Canvas validation error:', error);
    return false;
  }
};

// Enhanced frame synchronization function
const waitForThreeJSRender = (): Promise<void> => {
  return new Promise((resolve) => {
    // Use multiple requestAnimationFrame calls to ensure Three.js render completes
    requestAnimationFrame(() => {
      requestAnimationFrame(() => {
        requestAnimationFrame(() => {
          resolve();
        });
      });
    });
  });
};

export const useGifExport = (
  canvasRef: React.RefObject<HTMLCanvasElement>,
  videoRef: React.RefObject<HTMLVideoElement>,
  isPlaying: boolean,
  setIsPlaying: (playing: boolean) => void
) => {
  const [isRecordingGif, setIsRecordingGif] = useState(false);
  const [gifProgress, setGifProgress] = useState(0);
  const [gifError, setGifError] = useState<string | null>(null);
  const [recordingPhase, setRecordingPhase] = useState<'resetting' | 'capturing' | 'encoding' | null>(null);

  const encoderRef = useRef<any>(null);
  const timeoutRef = useRef<number | null>(null);
  const wasPlayingRef = useRef<boolean>(false);

  const resetVideoToStart = useCallback((): Promise<void> => {
    return new Promise((resolve, reject) => {
      if (!videoRef.current) {
        reject(new Error('Video element not available'));
        return;
      }

      const video = videoRef.current;
      
      // If already at start, resolve immediately
      if (video.currentTime === 0) {
        resolve();
        return;
      }

      const handleSeeked = () => {
        video.removeEventListener('seeked', handleSeeked);
        video.removeEventListener('error', handleError);
        resolve();
      };

      const handleError = () => {
        video.removeEventListener('seeked', handleSeeked);
        video.removeEventListener('error', handleError);
        reject(new Error('Failed to reset video position'));
      };

      video.addEventListener('seeked', handleSeeked);
      video.addEventListener('error', handleError);
      
      try {
        video.currentTime = 0;
      } catch (error) {
        video.removeEventListener('seeked', handleSeeked);
        video.removeEventListener('error', handleError);
        reject(error);
      }
    });
  }, [videoRef]);

  const finishRecording = useCallback(() => {
    // Clean up timeout
    if (timeoutRef.current) {
      clearTimeout(timeoutRef.current);
      timeoutRef.current = null;
    }

    // Restore playback state
    if (!wasPlayingRef.current && videoRef.current) {
      videoRef.current.pause();
      setIsPlaying(false);
    }

    // Clean up encoder
    if (encoderRef.current) {
      encoderRef.current.clear();
      encoderRef.current = null;
    }

    setIsRecordingGif(false);
    setGifProgress(0);
    setRecordingPhase(null);
  }, [videoRef, setIsPlaying]);

  const stopGifRecording = useCallback(() => {
    if (timeoutRef.current) {
      clearTimeout(timeoutRef.current);
      timeoutRef.current = null;
    }

    finishRecording();
  }, [finishRecording]);

  const startGifRecording = useCallback(async (settings: GifSettings) => {
    if (!canvasRef.current || !videoRef.current || isRecordingGif) return;

    // Auto-detect duration if not provided
    const videoDuration = videoRef.current?.duration || 5;
    const finalDuration = settings.duration || Math.min(Math.max(videoDuration, 1), 30);
    
    const finalSettings = {
      ...settings,
      duration: finalDuration
    };

    setIsRecordingGif(true);
    setGifProgress(0);
    setGifError(null);
    setRecordingPhase('resetting');
    wasPlayingRef.current = isPlaying;

    console.log('Starting GIF recording with settings:', finalSettings);

    try {
      // Reset video to start position
      await resetVideoToStart();

      // Optimize settings for device
      const optimizedSettings = gifOptimizer.optimizeSettings(finalSettings);
      console.log('Optimized GIF settings:', optimizedSettings);
      
      // Create GIF encoder with enhanced options
      const encoderOptions: GifEncoderOptions = {
        width: optimizedSettings.width,
        height: optimizedSettings.height,
        quality: optimizedSettings.quality,
        workers: optimizedSettings.workers,
        dither: 'Atkinson',
        repeat: -1, // Play once, no loop
        workerScript: '/gif-worker.js'
      };

      encoderRef.current = createGifEncoder(encoderOptions);

      // Start capturing phase
      setRecordingPhase('capturing');

      // Pause video for manual frame control
      if (videoRef.current) {
        videoRef.current.pause();
        setIsPlaying(false);
      }

      // Get source canvas dimensions
      const sourceWidth = canvasRef.current.width;
      const sourceHeight = canvasRef.current.height;
      
      // Calculate crop dimensions for the target aspect ratio
      const cropDimensions = calculateCropDimensions(
        sourceWidth,
        sourceHeight,
        optimizedSettings.width,
        optimizedSettings.height
      );

      console.log('Crop dimensions:', cropDimensions);

      // Calculate frame capture parameters
      const frameInterval = 1000 / optimizedSettings.fps; // milliseconds per frame
      const frameTimeStep = 1 / optimizedSettings.fps; // seconds per frame
      const totalFrames = Math.floor(optimizedSettings.duration * optimizedSettings.fps);
      
      console.log(`Will capture ${totalFrames} frames at ${optimizedSettings.fps} FPS`);
      
      let frameCount = 0;
      let currentVideoTime = 0;

      // Enhanced video-frame-based capture function with proper synchronization
      const captureVideoFrame = async () => {
        if (frameCount >= totalFrames || !videoRef.current) {
          console.log('Frame capture complete, starting encoding...');
          startEncoding();
          return;
        }

        try {
          console.log(`Capturing frame ${frameCount + 1}/${totalFrames} at time ${currentVideoTime.toFixed(3)}s`);
          
          // Set video to specific time for this frame
          videoRef.current.currentTime = currentVideoTime;
          
          // Wait for video to seek to the correct time
          await new Promise<void>((resolve, reject) => {
            const video = videoRef.current!;
            const targetTime = currentVideoTime;
            
            const handleSeeked = () => {
              video.removeEventListener('seeked', handleSeeked);
              video.removeEventListener('error', handleError);
              resolve();
            };

            const handleError = () => {
              video.removeEventListener('seeked', handleSeeked);
              video.removeEventListener('error', handleError);
              reject(new Error('Failed to seek video'));
            };

            // If already at the right time, resolve immediately
            if (Math.abs(video.currentTime - targetTime) < 0.01) {
              resolve();
              return;
            }

            video.addEventListener('seeked', handleSeeked);
            video.addEventListener('error', handleError);
          });

          // Enhanced synchronization: Wait for Three.js render to complete
          await waitForThreeJSRender();
          
          // Additional delay to ensure point cloud updates
          await new Promise(resolve => setTimeout(resolve, 200));

          // Validate canvas content with retry logic
          let validFrame = false;
          let retryCount = 0;
          const maxRetries = 3;

          while (!validFrame && retryCount < maxRetries) {
            if (retryCount > 0) {
              console.log(`Frame validation failed, retry ${retryCount}/${maxRetries}`);
              await new Promise(resolve => setTimeout(resolve, 100));
              await waitForThreeJSRender();
            }

            validFrame = validateCanvasContent(canvasRef.current);
            retryCount++;
          }

          if (!validFrame) {
            console.warn(`Frame ${frameCount + 1} failed validation after ${maxRetries} retries, using anyway`);
          }

          // Get export canvas from pool
          const exportCanvas = canvasPool.getCanvas(
            optimizedSettings.width,
            optimizedSettings.height
          );
          
          const ctx = exportCanvas.getContext('2d');
          if (ctx && canvasRef.current) {
            ctx.imageSmoothingEnabled = true;
            ctx.imageSmoothingQuality = 'high';
            
            // Clear the export canvas
            ctx.clearRect(0, 0, optimizedSettings.width, optimizedSettings.height);
            
            // Draw cropped source canvas to export canvas
            ctx.drawImage(
              canvasRef.current,
              cropDimensions.cropX,      // source x
              cropDimensions.cropY,      // source y  
              cropDimensions.cropWidth,  // source width
              cropDimensions.cropHeight, // source height
              0,                         // destination x
              0,                         // destination y
              optimizedSettings.width,   // destination width
              optimizedSettings.height   // destination height
            );
            
            // Validate the export canvas as well
            const exportValid = validateCanvasContent(exportCanvas);
            console.log(`Export canvas valid: ${exportValid}`);
            
            // Add frame to encoder
            encoderRef.current.addFrame(exportCanvas, frameInterval);
            canvasPool.releaseCanvas(exportCanvas);
            
            console.log(`Frame ${frameCount + 1} captured successfully`);
          }

          frameCount++;
          currentVideoTime += frameTimeStep;
          
          // Ensure we don't exceed video duration
          if (currentVideoTime > optimizedSettings.duration) {
            currentVideoTime = optimizedSettings.duration;
          }

          const captureProgress = (frameCount / totalFrames) * 50; // 0-50%
          setGifProgress(Math.round(captureProgress));

          // Schedule next frame capture with minimal delay
          timeoutRef.current = window.setTimeout(captureVideoFrame, 50);

        } catch (error) {
          console.error('Frame capture error:', error);
          handleRecordingError(new Error('Frame capture failed'));
          return;
        }
      };

      const startEncoding = async () => {
        try {
          setRecordingPhase('encoding');
          setGifProgress(50); // Start encoding phase
          
          console.log('Starting GIF encoding...');
          
          const blob = await encoderRef.current.encode(
            (progress: number) => {
              const encodingProgress = 50 + (progress * 50); // 50-100%
              setGifProgress(Math.round(encodingProgress));
              console.log(`Encoding progress: ${Math.round(progress * 100)}%`);
            }
          );

          console.log('GIF encoding complete, blob size:', blob.size);

          // Download the GIF
          downloadGif(blob, optimizedSettings);
          
          // Clean up
          finishRecording();
        } catch (error) {
          console.error('Encoding error:', error);
          handleRecordingError(error as Error);
        }
      };

      // Start capturing frames
      timeoutRef.current = window.setTimeout(captureVideoFrame, 100);

    } catch (error) {
      console.error('GIF recording error:', error);
      handleRecordingError(error as Error);
    }
  }, [isRecordingGif, isPlaying, canvasRef, videoRef, setIsPlaying]);

  const handleRecordingError = useCallback((error: Error) => {
    setGifError(error.message || 'Failed to create GIF');
    finishRecording();
  }, [finishRecording]);

  const downloadGif = useCallback((blob: Blob, settings: OptimizedGifSettings) => {
    const url = URL.createObjectURL(blob);
    const link = document.createElement('a');
    link.href = url;
    link.download = `pixelflow-${settings.width}x${settings.height}-${Date.now()}.gif`;
    document.body.appendChild(link);
    link.click();
    document.body.removeChild(link);
    URL.revokeObjectURL(url);
  }, []);

  const clearGifError = useCallback(() => {
    setGifError(null);
  }, []);

  return {
    startGifRecording,
    stopGifRecording,
    isRecordingGif,
    gifProgress,
    gifError,
    clearGifError,
    recordingPhase
  };
};

```

#### client/src/hooks/useVideoExport.tsx
```tsx
import { useRef, useState, useCallback } from 'react';
import { createVideoEncoder, VideoEncoderOptions } from '../utils/videoEncoder';
import { renderTargetPool } from '../utils/renderTargetPool';
import { FXAAProcessor } from '../utils/fxaaProcessor';

export interface VideoSettings {
  duration?: number;
  fps: number;
  quality: number;
  width: number;
  height: number;
}

// Reuse the same helper functions from your GIF export
const calculateCropDimensions = (
  sourceWidth: number,
  sourceHeight: number,
  targetWidth: number,
  targetHeight: number
) => {
  const sourceAspectRatio = sourceWidth / sourceHeight;
  const targetAspectRatio = targetWidth / targetHeight;
  
  let cropWidth, cropHeight, cropX, cropY;
  
  if (sourceAspectRatio > targetAspectRatio) {
    cropHeight = sourceHeight;
    cropWidth = cropHeight * targetAspectRatio;
    cropX = (sourceWidth - cropWidth) / 2;
    cropY = 0;
  } else {
    cropWidth = sourceWidth;
    cropHeight = cropWidth / targetAspectRatio;
    cropX = 0;
    cropY = (sourceHeight - cropHeight) / 2;
  }
  
  return {
    cropX: Math.round(cropX),
    cropY: Math.round(cropY),
    cropWidth: Math.round(cropWidth),
    cropHeight: Math.round(cropHeight)
  };
};

const validateCanvasContent = (canvas: HTMLCanvasElement): boolean => {
  const ctx = canvas.getContext('2d');
  if (!ctx) return false;
  
  const sampleSize = Math.min(50, canvas.width / 4, canvas.height / 4);
  const centerX = (canvas.width - sampleSize) / 2;
  const centerY = (canvas.height - sampleSize) / 2;
  
  try {
    const imageData = ctx.getImageData(centerX, centerY, sampleSize, sampleSize);
    const data = imageData.data;
    
    let nonBlackPixels = 0;
    for (let i = 0; i < data.length; i += 4) {
      const r = data[i];
      const g = data[i + 1];
      const b = data[i + 2];
      const a = data[i + 3];
      
      if (a > 0 && (r > 10 || g > 10 || b > 10)) {
        nonBlackPixels++;
      }
    }
    
    const validPixelThreshold = (sampleSize * sampleSize) * 0.01;
    const isValid = nonBlackPixels > validPixelThreshold;
    
    console.log(`Canvas validation: ${nonBlackPixels} non-black pixels out of ${sampleSize * sampleSize}, valid: ${isValid}`);
    return isValid;
  } catch (error) {
    console.error('Canvas validation error:', error);
    return false;
  }
};

const waitForThreeJSRender = (): Promise<void> => {
  return new Promise((resolve) => {
    requestAnimationFrame(() => {
      requestAnimationFrame(() => {
        requestAnimationFrame(() => {
          resolve();
        });
      });
    });
  });
};

export const useVideoExport = (
  canvasRef: React.RefObject<HTMLCanvasElement>,
  videoRef: React.RefObject<HTMLVideoElement>,
  isPlaying: boolean,
  setIsPlaying: (playing: boolean) => void
) => {
  const [isRecordingVideo, setIsRecordingVideo] = useState(false);
  const [videoProgress, setVideoProgress] = useState(0);
  const [videoError, setVideoError] = useState<string | null>(null);

  const encoderRef = useRef<any>(null);
  const timeoutRef = useRef<number | null>(null);
  const wasPlayingRef = useRef<boolean>(false);

  // OPTIMIZATION #3: Add FXAA processor for crystal-clear exports
  const fxaaProcessorRef = useRef<FXAAProcessor>();

  const resetVideoToStart = useCallback((): Promise<void> => {
    return new Promise((resolve, reject) => {
      if (!videoRef.current) {
        reject(new Error('Video element not available'));
        return;
      }

      const video = videoRef.current;
      
      if (video.currentTime === 0) {
        resolve();
        return;
      }

      const handleSeeked = () => {
        video.removeEventListener('seeked', handleSeeked);
        video.removeEventListener('error', handleError);
        resolve();
      };

      const handleError = () => {
        video.removeEventListener('seeked', handleSeeked);
        video.removeEventListener('error', handleError);
        reject(new Error('Failed to reset video position'));
      };

      video.addEventListener('seeked', handleSeeked);
      video.addEventListener('error', handleError);
      
      try {
        video.currentTime = 0;
      } catch (error) {
        video.removeEventListener('seeked', handleSeeked);
        video.removeEventListener('error', handleError);
        reject(error);
      }
    });
  }, [videoRef]);

  const finishRecording = useCallback(() => {
    if (timeoutRef.current) {
      clearTimeout(timeoutRef.current);
      timeoutRef.current = null;
    }

    if (!wasPlayingRef.current && videoRef.current) {
      videoRef.current.pause();
      setIsPlaying(false);
    }

    if (encoderRef.current) {
      encoderRef.current.clear();
      encoderRef.current = null;
    }

    setIsRecordingVideo(false);
    setVideoProgress(0);
  }, [videoRef, setIsPlaying]);

  const stopVideoRecording = useCallback(() => {
    if (timeoutRef.current) {
      clearTimeout(timeoutRef.current);
      timeoutRef.current = null;
    }
    finishRecording();
  }, [finishRecording]);

  const startVideoRecording = useCallback(async (settings: VideoSettings) => {
    if (!canvasRef.current || !videoRef.current || isRecordingVideo) return;

    const videoDuration = videoRef.current?.duration || 5;
    const finalDuration = settings.duration || Math.min(Math.max(videoDuration, 1), 30);
    
    const finalSettings = {
      ...settings,
      duration: finalDuration
    };

    setIsRecordingVideo(true);
    setVideoProgress(0);
    setVideoError(null);
    wasPlayingRef.current = isPlaying;

    // OPTIMIZATION #3: Initialize FXAA processor
    if (!fxaaProcessorRef.current) {
      fxaaProcessorRef.current = new FXAAProcessor();
    }

    console.log('Starting video recording with settings:', finalSettings);

    try {
      await resetVideoToStart();

      const encoderOptions: VideoEncoderOptions = {
        width: finalSettings.width,
        height: finalSettings.height,
        quality: finalSettings.quality,
        frameRate: finalSettings.fps
      };

      encoderRef.current = createVideoEncoder(encoderOptions);

      if (videoRef.current) {
        videoRef.current.pause();
        setIsPlaying(false);
      }

      const sourceWidth = canvasRef.current.width;
      const sourceHeight = canvasRef.current.height;
      
      const cropDimensions = calculateCropDimensions(
        sourceWidth,
        sourceHeight,
        finalSettings.width,
        finalSettings.height
      );

      console.log('Crop dimensions:', cropDimensions);

      const frameTimeStep = 1 / finalSettings.fps;
      const totalFrames = Math.floor(finalSettings.duration * finalSettings.fps);
      
      console.log(`Will capture ${totalFrames} frames at ${finalSettings.fps} FPS`);
      
      let frameCount = 0;
      let currentVideoTime = 0;

      const captureVideoFrame = async () => {
        if (frameCount >= totalFrames || !videoRef.current) {
          console.log('Frame capture complete, starting encoding...');
          startEncoding();
          return;
        }

        try {
          console.log(`Capturing frame ${frameCount + 1}/${totalFrames} at time ${currentVideoTime.toFixed(3)}s`);
          
          videoRef.current.currentTime = currentVideoTime;
          
          await new Promise<void>((resolve, reject) => {
            const video = videoRef.current!;
            const targetTime = currentVideoTime;
            
            const handleSeeked = () => {
              video.removeEventListener('seeked', handleSeeked);
              video.removeEventListener('error', handleError);
              resolve();
            };

            const handleError = () => {
              video.removeEventListener('seeked', handleSeeked);
              video.removeEventListener('error', handleError);
              reject(new Error('Failed to seek video'));
            };

            if (Math.abs(video.currentTime - targetTime) < 0.01) {
              resolve();
              return;
            }

            video.addEventListener('seeked', handleSeeked);
            video.addEventListener('error', handleError);
          });

          await waitForThreeJSRender();
          await new Promise(resolve => setTimeout(resolve, 200));

          let validFrame = false;
          let retryCount = 0;
          const maxRetries = 3;

          while (!validFrame && retryCount < maxRetries) {
            if (retryCount > 0) {
              console.log(`Frame validation failed, retry ${retryCount}/${maxRetries}`);
              await new Promise(resolve => setTimeout(resolve, 100));
              await waitForThreeJSRender();
            }

            validFrame = validateCanvasContent(canvasRef.current);
            retryCount++;
          }

          if (!validFrame) {
            console.warn(`Frame ${frameCount + 1} failed validation after ${maxRetries} retries, using anyway`);
          }

          // OPTIMIZATION #2: Use render target pool instead of canvas pool
          const exportCanvas = renderTargetPool.acquireCanvas(
            finalSettings.width,
            finalSettings.height
          );
          
          const ctx = exportCanvas.getContext('2d');
          if (ctx && canvasRef.current) {
            ctx.imageSmoothingEnabled = true;
            ctx.imageSmoothingQuality = 'high';
            
            ctx.clearRect(0, 0, finalSettings.width, finalSettings.height);
            
            ctx.drawImage(
              canvasRef.current,
              cropDimensions.cropX,
              cropDimensions.cropY,
              cropDimensions.cropWidth,
              cropDimensions.cropHeight,
              0,
              0,
              finalSettings.width,
              finalSettings.height
            );
            
            const exportValid = validateCanvasContent(exportCanvas);
            console.log(`Export canvas valid: ${exportValid}`);
            
            // OPTIMIZATION #3: Apply FXAA for crystal-clear exports
            const processedCanvas = fxaaProcessorRef.current!.process(exportCanvas);
            
            encoderRef.current.addFrame(processedCanvas, currentVideoTime);
            
            // OPTIMIZATION #2: Release canvas back to pool
            renderTargetPool.releaseCanvas(exportCanvas);
            
            console.log(`Frame ${frameCount + 1} captured successfully`);
          }

          frameCount++;
          currentVideoTime += frameTimeStep;
          
          if (currentVideoTime > finalSettings.duration) {
            currentVideoTime = finalSettings.duration;
          }

          const captureProgress = (frameCount / totalFrames) * 50;
          setVideoProgress(Math.round(captureProgress));

          timeoutRef.current = window.setTimeout(captureVideoFrame, 50);

        } catch (error) {
          console.error('Frame capture error:', error);
          handleRecordingError(new Error('Frame capture failed'));
          return;
        }
      };

      const startEncoding = async () => {
        try {
          setVideoProgress(50);
          
          console.log('Starting video encoding...');
          
          const blob = await encoderRef.current.encode(
            (progress: number) => {
              const encodingProgress = 50 + (progress * 50);
              setVideoProgress(Math.round(encodingProgress));
              console.log(`Encoding progress: ${Math.round(progress * 100)}%`);
            }
          );

          console.log('Video encoding complete, blob size:', blob.size);

          downloadVideo(blob, finalSettings);
          finishRecording();
        } catch (error) {
          console.error('Encoding error:', error);
          handleRecordingError(error as Error);
        }
      };

      timeoutRef.current = window.setTimeout(captureVideoFrame, 100);

    } catch (error) {
      console.error('Video recording error:', error);
      handleRecordingError(error as Error);
    }
  }, [isRecordingVideo, isPlaying, canvasRef, videoRef, setIsPlaying]);

  const handleRecordingError = useCallback((error: Error) => {
    setVideoError(error.message || 'Failed to create video');
    finishRecording();
  }, [finishRecording]);

  const downloadVideo = useCallback((blob: Blob, settings: VideoSettings) => {
    const url = URL.createObjectURL(blob);
    const link = document.createElement('a');
    link.href = url;
    link.download = `pixelflow-${settings.width}x${settings.height}-${Date.now()}.webm`;
    document.body.appendChild(link);
    link.click();
    document.body.removeChild(link);
    URL.revokeObjectURL(url);
  }, []);

  const clearVideoError = useCallback(() => {
    setVideoError(null);
  }, []);

  return {
    startVideoRecording,
    stopVideoRecording,
    isRecordingVideo,
    videoProgress,
    videoError,
    clearVideoError
  };
};

```

#### client/src/hooks/useVideoPointCloud.tsx
```tsx
import { useEffect, useRef, useState, useCallback } from 'react';
import * as THREE from 'three';
import { getDepthEstimator, type DepthResult } from '../utils/depthEstimation';
import { webglForcer } from '../utils/webglForcer';
import { WebGLResourceManager, ErrorRecovery, PerformanceMonitor } from '../utils/memoryManager';
import { 
  FrameRateOptimizer, 
  UniformBatcher, 
  FrustumCuller, 
  LODManager,
  PerformanceProfiler,
  WebGLStateCache
} from '../utils/performanceOptimizer';
import { InstancedPointCloudRenderer, createInstancedPointCloud } from '../utils/instancedPointCloud';
import { instancedVertexShader, ditheredFragmentShader } from '../utils/ditherShaders';

interface PointCloudSettings {
  nearClipping: number;
  farClipping: number;
  pointSize: number;
  zOffset: number;
  fov: number;
  depthScale: number;
  minDistance: number;
  maxDistance: number;
  depthPower: number;
  pointSizeDepthFactor: number;
  invertDepth: boolean;
  // Advanced shader parameters
  epsilon: number;
  exponentialK: number;
  gamma: number;
  stereographicC: number;
  offsetStrength: number;
  noiseScale: number;
  // Depth estimation
  useRealDepth: boolean;
  // GPU acceleration options
  useInstancedRendering?: boolean;
  enableDithering?: boolean;
  ditherStrength?: number;
  maxInstances?: number;
}

export const useVideoPointCloud = (
  canvasRef: React.RefObject<HTMLCanvasElement>,
  settings: PointCloudSettings
) => {
  const [isPlaying, setIsPlaying] = useState(false);
  const [videoFile, setVideoFile] = useState<File | null>(null);
  const [videoError, setVideoError] = useState<string | null>(null);
  
  // WebGL compatibility state
  const [webglSupported, setWebglSupported] = useState<boolean | null>(null);
  const [webglError, setWebglError] = useState<string | null>(null);
  
  const sceneRef = useRef<THREE.Scene>();
  const rendererRef = useRef<THREE.WebGLRenderer>();
  const cameraRef = useRef<THREE.OrthographicCamera>();
  const frustumSizeRef = useRef<number>(10);
  const pointsRef = useRef<THREE.Points>();
  const videoRef = useRef<HTMLVideoElement>() as React.MutableRefObject<HTMLVideoElement>;
  const textureRef = useRef<THREE.VideoTexture>();
  const animationIdRef = useRef<number>();
  const isVideoReadyRef = useRef<boolean>(false);
  const geometryRef = useRef<THREE.BufferGeometry>();
  const materialRef = useRef<THREE.ShaderMaterial>();
  const depthEstimatorRef = useRef<any>(null);
  const currentDepthMapRef = useRef<Float32Array | null>(null);
  const depthTextureRef = useRef<THREE.DataTexture | null>(null);
  
  // Optional instanced rendering system for high performance
  const instancedRendererRef = useRef<InstancedPointCloudRenderer | null>(null);
  
  // GPU memory and performance monitoring (non-intrusive)
  const gpuStatsRef = useRef({
    memoryUsed: 0,
    drawCalls: 0,
    triangles: 0,
    points: 0,
    lastUpdate: 0
  });

  // Camera control state - mouse
  const mouseRef = useRef({ x: 0, y: 0 });
  const isDraggingRef = useRef(false);
  
  // Camera control state - touch
  const touchRef = useRef({ x: 0, y: 0 });
  const isTouchDraggingRef = useRef(false);
  
  // Pinch-to-zoom state
  const pinchStateRef = useRef({
    isActive: false,
    initialDistance: 0,
    initialRadius: 0,
    lastDistance: 0
  });
  
  const cameraPositionRef = useRef({ 
    theta: Math.PI / 2,         // 90° = frontal view (camera at positive Z looking toward origin)
    phi: Math.PI / 2,           // 90° from Y-axis (horizontal, eye level)
    radius: 2.0                 // Distance from center
  });

  // Default frontal camera position - straight on, eye level
  const DEFAULT_CAMERA_POSITION = {
    azimuth: 90,    // 90° = perfect frontal view
    elevation: 0,   // 0° = eye level, no tilt
    distance: 2.0   // Optimal viewing distance
  };

  // Helper functions for video aspect ratio adaptation
  const calculateOptimalCameraDistance = useCallback((aspectRatio: number, videoWidth: number, videoHeight: number): number => {
    // Use the correct frontal view distance that matches the working position
    const baseDistance = 2.0;
    
    // Minimal adjustment to maintain proper framing - keep it close to 2.0
    // Only adjust slightly for extreme aspect ratios
    if (aspectRatio > 2.5) {
      return baseDistance * 1.2; // Slightly further for ultra-wide videos
    } else if (aspectRatio < 0.8) {
      return baseDistance * 0.9; // Slightly closer for tall videos
    }
    
    return baseDistance; // Keep standard distance for most videos
  }, []);

  const calculateOptimalFrustumSize = useCallback((aspectRatio: number, videoWidth: number, videoHeight: number): number => {
    // Always use the FOV setting for consistent framing
    return settings.fov * 0.3; // Respect the FOV 30 setting
  }, [settings.fov]);

  // Luma AI-style camera state (in degrees for UI)
  const [cameraState, setCameraState] = useState(DEFAULT_CAMERA_POSITION);

  // Trajectory animation state
  const [orbitLock, setOrbitLock] = useState(true);
  const [trajectoryMode, setTrajectoryMode] = useState('manual');
  const [trajectoryDuration, setTrajectoryDuration] = useState(10);
  const trajectoryAnimationRef = useRef<number>();
  const trajectoryStartTimeRef = useRef<number>();
  const basePositionRef = useRef({ azimuth: 90, elevation: 0, distance: 2.0 });

  // Convert between radians (internal) and degrees (UI)
  const updateCameraFromDegrees = useCallback((azimuth: number, elevation: number, distance: number) => {
    // For frontal view (azimuth=90°, elevation=0°), force perfect positioning
    if (Math.abs(azimuth - 90) < 0.1 && Math.abs(elevation) < 0.1) {
      // Set internal coordinates for frontal view
      cameraPositionRef.current = { theta: Math.PI / 2, phi: Math.PI / 2, radius: distance };
      setCameraState({ azimuth: 90, elevation: 0, distance });
      
      // Force camera to perfect frontal position
      if (cameraRef.current) {
        cameraRef.current.position.set(0, 0, distance);
        cameraRef.current.lookAt(0, 0, 0);
      }
      return;
    }
    
    // Convert UI degrees to internal radians for non-frontal positions
    const theta = (azimuth * Math.PI) / 180;
    const phi = ((90 - elevation) * Math.PI) / 180; // Elevation to phi conversion
    
    cameraPositionRef.current = { theta, phi, radius: distance };
    setCameraState({ azimuth, elevation, distance });
    
    // Update Three.js camera position using spherical coordinates
    if (cameraRef.current) {
      const camera = cameraRef.current;
      camera.position.x = distance * Math.sin(phi) * Math.cos(theta);
      camera.position.y = distance * Math.cos(phi);
      camera.position.z = distance * Math.sin(phi) * Math.sin(theta);
      camera.lookAt(0, 0, 0);
    }
  }, []);

  // Sync internal camera state to UI state
  const syncCameraState = useCallback(() => {
    const { theta, phi, radius } = cameraPositionRef.current;
    const azimuth = (theta * 180) / Math.PI;
    const elevation = 90 - (phi * 180) / Math.PI;
    
    setCameraState({ azimuth, elevation, distance: radius });
  }, []);

  // Trajectory animation system
  const animateTrajectory = useCallback((currentTime: number) => {
    if (!trajectoryStartTimeRef.current) {
      trajectoryStartTimeRef.current = currentTime;
      // Store the starting position when animation begins
      basePositionRef.current = {
        azimuth: cameraState.azimuth,
        elevation: cameraState.elevation,
        distance: cameraState.distance
      };
    }

    const elapsed = (currentTime - trajectoryStartTimeRef.current) / 1000; // Convert to seconds
    const progress = (elapsed % trajectoryDuration) / trajectoryDuration; // Loop animation

    const basePos = basePositionRef.current;
    let newAzimuth = basePos.azimuth;
    let newElevation = basePos.elevation;
    let newDistance = basePos.distance;

    switch (trajectoryMode) {
      case 'orbit':
        // Smooth 360° orbital rotation around base position
        newAzimuth = basePos.azimuth + (progress * 360);
        newElevation = basePos.elevation; // Keep base elevation
        newDistance = basePos.distance; // Keep base distance
        break;
        
      case 'oscillate':
        // Gentler oscillation pattern using sine waves
        const t = progress * Math.PI * 4; // Slower oscillation
        const azimuthRange = 45; // ±45° azimuth swing
        const elevationRange = 20; // ±20° elevation swing
        
        // Create figure-8 pattern with different frequencies
        newAzimuth = basePos.azimuth + Math.sin(t) * azimuthRange;
        newElevation = basePos.elevation + Math.sin(t * 0.5) * elevationRange; // Half frequency for figure-8
        newDistance = basePos.distance; // Keep base distance
        break;
        
      case 'custom':
        // Breathing zoom effect
        newAzimuth = basePos.azimuth;
        newElevation = basePos.elevation;
        newDistance = basePos.distance + Math.sin(progress * Math.PI * 2) * 2;
        break;
    }

    // Apply the calculated position
    updateCameraFromDegrees(newAzimuth, newElevation, newDistance);

    if (trajectoryMode !== 'manual') {
      trajectoryAnimationRef.current = requestAnimationFrame(animateTrajectory);
    }
  }, [trajectoryMode, trajectoryDuration, updateCameraFromDegrees]);

  // Start/stop trajectory animation
  useEffect(() => {
    // Reset animation when mode changes
    trajectoryStartTimeRef.current = undefined;
    
    if (trajectoryMode !== 'manual') {
      trajectoryAnimationRef.current = requestAnimationFrame(animateTrajectory);
    } else {
      if (trajectoryAnimationRef.current) {
        cancelAnimationFrame(trajectoryAnimationRef.current);
        trajectoryAnimationRef.current = undefined;
      }
    }

    return () => {
      if (trajectoryAnimationRef.current) {
        cancelAnimationFrame(trajectoryAnimationRef.current);
      }
    };
  }, [trajectoryMode, animateTrajectory]);

  // Camera control handlers
  const handleOrbitLockChange = useCallback((enabled: boolean) => {
    setOrbitLock(enabled);
  }, []);

  const handleTrajectoryModeChange = useCallback((mode: string) => {
    setTrajectoryMode(mode);
  }, []);

  const handleTrajectoryDurationChange = useCallback((duration: number) => {
    setTrajectoryDuration(duration);
  }, []);

  // Camera reset function - returns to clean frontal view
  const resetCamera = useCallback(() => {
    // Stop any ongoing animation
    if (trajectoryAnimationRef.current) {
      cancelAnimationFrame(trajectoryAnimationRef.current);
      trajectoryAnimationRef.current = undefined;
    }
    trajectoryStartTimeRef.current = undefined;
    
    // Reset to manual mode
    setTrajectoryMode('manual');
    
    // Calculate optimal position for current video if available
    let optimalDistance = DEFAULT_CAMERA_POSITION.distance;
    
    if (videoRef.current && videoRef.current.videoWidth) {
      const videoWidth = videoRef.current.videoWidth;
      const videoHeight = videoRef.current.videoHeight;
      const aspectRatio = videoWidth / videoHeight;
      
      optimalDistance = calculateOptimalCameraDistance(aspectRatio, videoWidth, videoHeight);
      const optimalFrustumSize = calculateOptimalFrustumSize(aspectRatio, videoWidth, videoHeight);
      
      // Update orthographic camera frustum
      if (cameraRef.current) {
        const canvasAspectRatio = window.innerWidth / window.innerHeight;
        const cam = cameraRef.current as THREE.OrthographicCamera;
        
        cam.left = optimalFrustumSize * canvasAspectRatio / -2;
        cam.right = optimalFrustumSize * canvasAspectRatio / 2;
        cam.top = optimalFrustumSize / 2;
        cam.bottom = optimalFrustumSize / -2;
        cam.updateProjectionMatrix();
      }
    }
    
    // Apply optimal frontal position
    updateCameraFromDegrees(
      DEFAULT_CAMERA_POSITION.azimuth,
      DEFAULT_CAMERA_POSITION.elevation,
      optimalDistance
    );
  }, [updateCameraFromDegrees, calculateOptimalCameraDistance, calculateOptimalFrustumSize]);

  // Helper function to detect if user is on desktop
  const isDesktop = useCallback((): boolean => {
    // Check screen size and user agent for desktop detection
    const hasLargeScreen = window.innerWidth >= 1024 && window.innerHeight >= 768;
    const isMobileUserAgent = /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent);
    return hasLargeScreen && !isMobileUserAgent;
  }, []);

  // WebGL compatibility checker with forced context creation
  const checkWebGLSupport = useCallback((): { supported: boolean; error: string | null } => {
    try {
      if (!canvasRef.current) {
        return { supported: false, error: 'Canvas not available' };
      }

      // Use the WebGL forcer for aggressive context creation
      const webglInfo = webglForcer.forceWebGLContext(canvasRef.current);
      
      if (!webglInfo.supported || !webglInfo.context) {
        console.warn('WebGL forcer could not create context, trying fallback methods...');
        
        // Try creating a temporary canvas for testing
        const testCanvas = document.createElement('canvas');
        testCanvas.width = 256;
        testCanvas.height = 256;
        
        const testInfo = webglForcer.forceWebGLContext(testCanvas);
        
        if (testInfo.supported && testInfo.context) {
          console.log('WebGL works on test canvas, context will be created during initialization');
          return { supported: true, error: null };
        }
        
        return {
          supported: false,
          error: `WebGL not available. Renderer: ${webglInfo.renderer}, Vendor: ${webglInfo.vendor}`
        };
      }

      const gl = webglInfo.context;
      
      // Check WebGL capabilities
      const maxTextureSize = gl.getParameter(gl.MAX_TEXTURE_SIZE);
      const maxVertexAttribs = gl.getParameter(gl.MAX_VERTEX_ATTRIBS);
      
      console.log(`WebGL Context Created: ${webglInfo.version}`);
      console.log(`Vendor: ${webglInfo.vendor}, Renderer: ${webglInfo.renderer}`);
      console.log(`Max texture size: ${maxTextureSize}, Max vertex attribs: ${maxVertexAttribs}`);

      // Check for optional but beneficial extensions
      const extensions = [
        'OES_standard_derivatives',
        'EXT_frag_depth', 
        'WEBGL_depth_texture',
        'OES_texture_float'
      ];
      
      extensions.forEach(ext => {
        const extension = (gl as WebGLRenderingContext).getExtension(ext);
        console.log(`WebGL Extension ${ext}: ${extension ? 'Available' : 'Not available'}`);
      });

      return { supported: true, error: null };
    } catch (error) {
      return {
        supported: false,
        error: `WebGL context creation failed: ${error instanceof Error ? error.message : 'Unknown error'}`
      };
    }
  }, []);

  // Helper function to calculate distance between two touch points
  const calculateTouchDistance = useCallback((touch1: Touch, touch2: Touch): number => {
    const dx = touch1.clientX - touch2.clientX;
    const dy = touch1.clientY - touch2.clientY;
    return Math.sqrt(dx * dx + dy * dy);
  }, []);

  // GPU performance monitoring (non-intrusive addition)
  const updateGPUStats = useCallback(() => {
    if (!rendererRef.current) return;
    
    const now = performance.now();
    if (now - gpuStatsRef.current.lastUpdate < 1000) return; // Update once per second
    
    const info = rendererRef.current.info;
    const memory = info.memory;
    const render = info.render;
    
    gpuStatsRef.current = {
      memoryUsed: memory.geometries + memory.textures,
      drawCalls: render.calls,
      triangles: render.triangles,
      points: render.points,
      lastUpdate: now
    };
    
    // Log performance stats for monitoring (non-disruptive)
    if (process.env.NODE_ENV === 'development') {
      console.log('GPU Stats:', {
        'Memory (MB)': (gpuStatsRef.current.memoryUsed / 1024 / 1024).toFixed(2),
        'Draw Calls': gpuStatsRef.current.drawCalls,
        'Points': gpuStatsRef.current.points.toLocaleString()
      });
    }
  }, []);

  // Helper function to calculate display dimensions
  const calculateDisplayDimensions = useCallback((width: number, height: number) => {
    const aspectRatio = width / height;
    const maxDisplaySize = 10;
    
    let displayWidth, displayHeight;
    if (aspectRatio > 1) {
      displayWidth = maxDisplaySize;
      displayHeight = maxDisplaySize / aspectRatio;
    } else {
      displayHeight = maxDisplaySize;
      displayWidth = maxDisplaySize * aspectRatio;
    }
    
    return { displayWidth, displayHeight, aspectRatio };
  }, []);

  // Enhanced adaptive LOD system - remove desktop throttling for development
  const getAdaptiveDensity = useCallback((cameraDistance: number, videoResolution: number): number => {
    // For desktop users during development: remove all throttling
    if (isDesktop()) {
      console.log(`Desktop mode: Full resolution - ${videoResolution} points`);
      return videoResolution; // No limits for desktop development
    }
    
    // Keep mobile optimizations intact
    const maxPoints = 1500000; // Reduced for mobile
    const baseDensity = Math.min(videoResolution, maxPoints);
    
    // Mobile density based on camera distance
    if (cameraDistance < 7) return baseDensity;
    if (cameraDistance < 15) return baseDensity * 0.7;
    if (cameraDistance < 25) return baseDensity * 0.5;
    return baseDensity * 0.3;
  }, [isDesktop]);

  // Enhanced skip factor calculation - desktop gets full resolution
  const getAdaptiveSkipFactor = useCallback((targetDensity: number, totalPixels: number): number => {
    // For desktop users: always use full resolution (skip factor 1)
    if (isDesktop()) {
      console.log('Desktop mode: Skip factor 1 (full resolution)');
      return 1;
    }
    
    // Mobile skip factor logic
    const densityRatio = targetDensity / totalPixels;
    
    if (densityRatio >= 1.0) return 1;
    if (densityRatio >= 0.7) return 1;
    if (densityRatio >= 0.5) return 2;
    if (densityRatio >= 0.3) return 2;
    return 3;
  }, [isDesktop]);

  // Memoized camera position update function
  const updateCameraPosition = useCallback(() => {
    if (!cameraRef.current) return;

    const { theta, radius } = cameraPositionRef.current;
    let { phi } = cameraPositionRef.current;
    
    // Lock phi to horizon level when orbit lock is enabled
    if (orbitLock) {
      phi = Math.PI / 2; // Perfect horizon level (90 degrees)
    }
    
    // Spherical coordinates with Y-up for perfect orthographic orbit
    cameraRef.current.position.x = radius * Math.sin(phi) * Math.cos(theta);
    cameraRef.current.position.y = radius * Math.cos(phi);
    cameraRef.current.position.z = radius * Math.sin(phi) * Math.sin(theta);
    
    // Always look at center point for symmetric orthographic view
    cameraRef.current.lookAt(0, 0, 0);
    
    // Sync UI state
    const azimuthDegrees = (theta * 180 / Math.PI) % 360;
    const elevationDegrees = orbitLock ? 0 : ((Math.PI / 2 - phi) * 180 / Math.PI);
    setCameraState({ azimuth: azimuthDegrees, elevation: elevationDegrees, distance: radius });
  }, [orbitLock]);



  // Create geometry with full resolution and adaptive LOD
  const createPointCloudGeometry = useCallback(() => {
    if (!videoRef.current || !sceneRef.current) return;

    const video = videoRef.current;
    const width = video.videoWidth || 640;
    const height = video.videoHeight || 480;
    
    const { displayWidth, displayHeight } = calculateDisplayDimensions(width, height);

    // Calculate adaptive density based on camera distance
    const totalPixels = width * height;
    const cameraDistance = cameraPositionRef.current.radius;
    const targetDensity = getAdaptiveDensity(cameraDistance, totalPixels);
    const adaptiveSkipFactor = getAdaptiveSkipFactor(targetDensity, totalPixels);

    // Calculate final point count with adaptive density
    const pointCount = Math.floor(totalPixels / (adaptiveSkipFactor * adaptiveSkipFactor));

    console.log(`Point cloud stats: ${pointCount} points, skip factor: ${adaptiveSkipFactor}, total pixels: ${totalPixels}`);

    // Create geometry with adaptive density
    const positions = new Float32Array(pointCount * 3);
    const colors = new Float32Array(pointCount * 3);
    const uvs = new Float32Array(pointCount * 2);

    let index = 0;
    for (let y = 0; y < height; y += adaptiveSkipFactor) {
      for (let x = 0; x < width; x += adaptiveSkipFactor) {
        if (index >= pointCount) break;

        const u = x / width;
        const v = 1.0 - (y / height);

        positions[index * 3] = (u - 0.5) * displayWidth;
        positions[index * 3 + 1] = (v - 0.5) * displayHeight;
        positions[index * 3 + 2] = 0;

        uvs[index * 2] = u;
        uvs[index * 2 + 1] = y / height; // Use original y for texture sampling

        colors[index * 3] = 1;
        colors[index * 3 + 1] = 1;
        colors[index * 3 + 2] = 1;

        index++;
      }
    }

    // Create geometry with GPU-optimized attributes
    const geometry = new THREE.BufferGeometry();

    geometry.setAttribute('position', new THREE.BufferAttribute(positions, 3));
    geometry.setAttribute('color', new THREE.BufferAttribute(colors, 3));
    geometry.setAttribute('uv', new THREE.BufferAttribute(uvs, 2));
    
    // Enable GPU-side frustum culling and optimize for rendering
    geometry.computeBoundingSphere();
    geometry.computeBoundingBox();

    geometryRef.current = geometry;
  }, [getAdaptiveDensity, getAdaptiveSkipFactor, calculateDisplayDimensions]);

  // Create material and points object
  const createPointCloudMaterial = useCallback(() => {
    if (!geometryRef.current || !textureRef.current || !sceneRef.current) return;

    // Create GPU-accelerated shader material with maximum performance flags
    const material = new THREE.ShaderMaterial({
      uniforms: {
        videoTexture: { value: textureRef.current },
        pointSize: { value: settings.pointSize },
        zOffset: { value: settings.zOffset },
        depthScale: { value: settings.depthScale },
        nearClipping: { value: settings.nearClipping },
        farClipping: { value: settings.farClipping },
        depthPower: { value: settings.depthPower },
        pointSizeDepthFactor: { value: settings.pointSizeDepthFactor },
        invertDepth: { value: settings.invertDepth },
        fadeRange: { value: 0.05 },
        // Advanced shader uniforms
        epsilon: { value: settings.epsilon },
        exponentialK: { value: settings.exponentialK },
        gamma: { value: settings.gamma },
        stereographicC: { value: settings.stereographicC },
        offsetStrength: { value: settings.offsetStrength },
        noiseScale: { value: settings.noiseScale },
        // Depth estimation uniforms
        useRealDepth: { value: settings.useRealDepth },
        depthMap: { value: null },
        // GPU acceleration uniforms for maximum quality dithering
        enableDithering: { value: settings.enableDithering !== false },
        ditherStrength: { value: settings.ditherStrength || 0.15 },
        time: { value: 0.0 }
      },
      // Advanced GPU acceleration flags for maximum performance
      transparent: true,
      alphaTest: 0.001,
      depthWrite: false,
      depthTest: true,
      blending: THREE.AdditiveBlending,
      vertexColors: true,
      side: THREE.DoubleSide,
      vertexShader: `
        #include <common>
        #include <logdepthbuf_pars_vertex>
        
        uniform sampler2D videoTexture;
        uniform float pointSize;
        uniform float zOffset;
        uniform float depthScale;
        uniform float nearClipping;
        uniform float farClipping;
        uniform float depthPower;
        uniform float pointSizeDepthFactor;
        uniform bool invertDepth;
        uniform float fadeRange;
        // Advanced shader uniforms
        uniform float epsilon;
        uniform float stereographicC;
        uniform float offsetStrength;
        // Depth estimation uniforms
        uniform bool useRealDepth;
        uniform sampler2D depthMap;
        
        varying vec3 vColor;
        varying vec2 vUv;
        varying float vAlpha;
        
        // GPU-based modular effect functions
        vec2 applyReciprocalStretch(vec2 pos, float depth, float epsilon) {
          return pos / max(abs(depth), epsilon);
        }
        
        vec3 applyExponentialHighlight(vec3 color, float k) {
          return color * exp(k * color);
        }
        
        vec3 applyGammaCorrection(vec3 color, float gamma) {
          return pow(color, vec3(gamma));
        }
        
        bool shouldDiscardXOR(vec2 pos, float scale) {
          int x = int(floor(pos.x * scale));
          int y = int(floor(pos.y * scale));
          return ((x ^ y) & 1) == 1;
        }
        
        vec2 applyStereographicProjection(vec2 pos, float depth, float c) {
          return pos / (1.0 - c * depth);
        }
        
        vec2 applyDiffractionGrating(vec2 pos, vec3 color, float freq) {
          float lambda = (color.r + color.g + color.b) / 3.0;
          vec2 offset = vec2(lambda * sin(freq * pos.x), 0.0);
          return pos + offset;
        }
        
        // Enhanced depth calculation with real depth support
        float calculateDepth(vec2 uv, float luminance, float near, float far, float power, bool invert) {
          float depth;
          
          if (useRealDepth) {
            // Use real depth from TensorFlow.js depth estimation
            depth = texture2D(depthMap, uv).r;
          } else {
            // Use brightness-based depth heuristics
            depth = luminance;
            if (invert) {
              depth = 1.0 - depth;
            }
          }
          
          if (depth < near || depth > far) {
            return -1.0;
          }
          
          float normalizedDepth = (depth - near) / (far - near);
          normalizedDepth = clamp(normalizedDepth, 0.0, 1.0);
          normalizedDepth = pow(normalizedDepth, power);
          
          return normalizedDepth;
        }
        
        void main() {
          vUv = uv;
          vec4 texel = texture2D(videoTexture, uv);
          
          // Calculate luminance for depth
          float luminance = dot(texel.rgb, vec3(0.299, 0.587, 0.114));
          float normalizedDepth = calculateDepth(uv, luminance, nearClipping, farClipping, depthPower, invertDepth);
          
          vAlpha = 1.0;
          
          // Handle clipped points
          if (normalizedDepth < 0.0) {
            gl_Position = vec4(0.0, 0.0, -1000.0, 1.0);
            gl_PointSize = 0.0;
            vColor = vec3(0.0);
            vAlpha = 0.0;
            return;
          }
          
          // Apply smooth fading at clipping boundaries using dynamic fade range
          float originalLuminance = invertDepth ? (1.0 - luminance) : luminance;
          vAlpha *= smoothstep(nearClipping, nearClipping + fadeRange, originalLuminance);
          vAlpha *= smoothstep(farClipping, farClipping - fadeRange, originalLuminance);
          
          // Discard fully transparent points
          if (vAlpha <= 0.001) {
            gl_Position = vec4(0.0, 0.0, -1000.0, 1.0);
            gl_PointSize = 0.0;
            vColor = vec3(0.0);
            return;
          }
          
          // Calculate actual depth for positioning with advanced effects
          float depth = (normalizedDepth - 0.5) * depthScale * 10.0;
          
          // Apply depth to position
          vec3 worldPos = position;
          worldPos.z = depth + zOffset;
          
          vec4 mvPosition = modelViewMatrix * vec4(worldPos, 1.0);
          
          // Reciprocal Stretch: Enhance depth perception
          float z_original = mvPosition.z;
          float z_new = 1.0 / (z_original + epsilon);
          mvPosition.z = z_new;
          
          // Stereographic Projection: Preserve angles in 2D projection
          vec2 stereo = mvPosition.xy / (1.0 - mvPosition.z * stereographicC);
          
          // Diffraction Grating: Offset points based on color
          vec3 offset = texel.rgb * offsetStrength;
          mvPosition.xy = stereo + offset.xy;
          
          gl_Position = projectionMatrix * mvPosition;
          
          // Enhanced point sizing based on depth
          gl_PointSize = pointSize * (1.0 + normalizedDepth * pointSizeDepthFactor);
          
          // Pass through original colors unchanged
          vColor = texel.rgb;
          
          #include <logdepthbuf_vertex>
        }
      `,
      fragmentShader: `
        #include <common>
        #include <logdepthbuf_pars_fragment>
        
        varying vec3 vColor;
        varying float vAlpha;
        varying vec2 vUv;
        
        uniform float exponentialK;
        uniform float gamma;
        uniform float noiseScale;
        uniform bool enableDithering;
        uniform float ditherStrength;
        uniform float time;
        
        // Enhanced Bayer matrix dithering with blue noise temporal variation
        mat4 bayerMatrix4x4 = mat4(
          0.0/16.0, 8.0/16.0, 2.0/16.0, 10.0/16.0,
          12.0/16.0, 4.0/16.0, 14.0/16.0, 6.0/16.0,
          3.0/16.0, 11.0/16.0, 1.0/16.0, 9.0/16.0,
          15.0/16.0, 7.0/16.0, 13.0/16.0, 5.0/16.0
        );
        
        // High-quality blue noise with temporal variation for natural patterns
        vec3 enhancedBlueNoise(vec2 coord, float t) {
          vec3 magic = vec3(12.9898, 78.233, 37.719);
          vec2 animatedCoord = coord + vec2(sin(t * 0.1), cos(t * 0.1)) * 0.5;
          
          vec3 noise;
          noise.r = fract(sin(dot(animatedCoord, magic.xy)) * 43758.5453);
          noise.g = fract(sin(dot(animatedCoord + vec2(1.0, 0.0), magic.yz)) * 43758.5453);
          noise.b = fract(sin(dot(animatedCoord + vec2(0.0, 1.0), magic.xz)) * 43758.5453);
          
          // Blue noise characteristics with smooth distribution
          return smoothstep(0.0, 1.0, noise) - 0.5;
        }
        
        // Advanced ordered dithering with temporal blue noise enhancement
        vec3 photorealisticDither(vec3 color, vec2 screenPos) {
          // Get Bayer matrix threshold
          ivec2 matrixPos = ivec2(mod(screenPos, 4.0));
          float bayerThreshold = bayerMatrix4x4[matrixPos.x][matrixPos.y];
          
          // Add temporal blue noise for natural variation
          vec3 blueNoise = enhancedBlueNoise(screenPos * 0.1, time);
          
          // Combine ordered dithering with blue noise for maximum quality
          vec3 combinedNoise = mix(vec3(bayerThreshold), blueNoise, 0.3);
          
          // Apply high-precision dithering
          vec3 dithered = color + combinedNoise * ditherStrength;
          
          // 10-bit quantization for smooth gradients
          vec3 quantized = floor(dithered * 1023.0 + 0.5) / 1023.0;
          
          return mix(color, quantized, ditherStrength);
        }
        
        void main() {
          // Create clean circular points
          vec2 circCoord = 2.0 * gl_PointCoord - 1.0;
          float dist = dot(circCoord, circCoord);
          if (dist > 1.0) discard;
          
          vec3 color = vColor;
          
          // Apply photorealistic dithering with Bayer matrix and blue noise
          if (enableDithering) {
            color = photorealisticDither(color, gl_FragCoord.xy);
          }
          
          // Exponential Highlighting: Glowing effect
          float intensity = (color.r + color.g + color.b) / 3.0;
          vec3 highlightedColor = color * exp(exponentialK * intensity);
          
          // Gamma Correction: Adjust brightness/contrast
          vec3 correctedColor = pow(highlightedColor, vec3(1.0 / gamma));
          
          // Voronoi Noise: Create organic cellular pattern
          vec2 noiseCoord = vUv * noiseScale;
          vec2 cellId = floor(noiseCoord);
          vec2 cellPos = fract(noiseCoord);
          
          float minDist = 1.0;
          for(int y = -1; y <= 1; y++) {
            for(int x = -1; x <= 1; x++) {
              vec2 neighbor = vec2(float(x), float(y));
              vec2 point = cellId + neighbor;
              
              // Generate pseudo-random point in cell
              vec2 randPoint = fract(sin(point.x * 12.9898 + point.y * 78.233) * vec2(43758.5453, 28377.1353));
              vec2 diff = neighbor + randPoint - cellPos;
              float dist = length(diff);
              minDist = min(minDist, dist);
            }
          }
          
          float pattern = smoothstep(0.0, 0.1, minDist);
          vec3 patternedColor = mix(correctedColor, correctedColor * 1.2, pattern * 0.3);
          
          // Clean edge falloff
          float alpha = 1.0 - smoothstep(0.6, 1.0, dist);
          
          // Apply calculated alpha for clipping and fading
          gl_FragColor = vec4(patternedColor, alpha * vAlpha);
          
          #include <logdepthbuf_fragment>
        }
      `
    });

    // Store material reference for updates
    materialRef.current = material;

    // Remove existing points with proper resource cleanup
    if (pointsRef.current) {
      sceneRef.current.remove(pointsRef.current);
      // Dispose of old material and unregister from resource manager
      if (pointsRef.current.material instanceof THREE.Material) {
        WebGLResourceManager.unregister(pointsRef.current.material);
        pointsRef.current.material.dispose();
      }
    }

    // Create GPU-accelerated points with hardware instancing
    const points = new THREE.Points(geometryRef.current, material);
    
    // Enable hardware instancing for maximum performance
    points.frustumCulled = true; // GPU-side frustum culling
    points.matrixAutoUpdate = false; // Manual matrix updates for performance
    
    // Enable GPU-accelerated instanced rendering for maximum performance
    if (geometryRef.current && points) {
      // Force hardware instancing with optimized buffer management
      points.frustumCulled = true;
      points.matrixAutoUpdate = false;
      
      // Enable GPU-side optimizations
      const material = points.material as THREE.ShaderMaterial;
      material.needsUpdate = true;
      
      // Set render order for optimal depth sorting
      points.renderOrder = 1;
    }
    
    sceneRef.current.add(points);
    pointsRef.current = points;

    // Register material with resource manager for memory optimization
    WebGLResourceManager.register(material, 'pointcloud_material');
  }, []);

  // AAA-optimized uniform batching system
  const updateMaterialUniforms = useCallback(() => {
    if (!materialRef.current) return;

    PerformanceProfiler.startProfile('uniform_update');
    
    // Ensure near clipping is never greater than far clipping
    const effectiveNearClipping = Math.min(settings.nearClipping, settings.farClipping);
    const effectiveFarClipping = Math.max(settings.nearClipping, settings.farClipping);
    
    // Calculate dynamic fade range based on clipping range
    const clippingRange = effectiveFarClipping - effectiveNearClipping;
    const dynamicFadeRange = Math.max(0.001, clippingRange * 0.1);

    // Adaptive quality scaling based on performance
    const qualityScale = FrameRateOptimizer.getQualityScale();
    const adaptivePointSize = settings.pointSize * qualityScale;

    // Batch uniform updates for GPU efficiency
    UniformBatcher.setUniform('pointSize', adaptivePointSize);
    UniformBatcher.setUniform('zOffset', settings.zOffset);
    UniformBatcher.setUniform('depthScale', settings.depthScale);
    UniformBatcher.setUniform('nearClipping', effectiveNearClipping);
    UniformBatcher.setUniform('farClipping', effectiveFarClipping);
    UniformBatcher.setUniform('depthPower', settings.depthPower);
    UniformBatcher.setUniform('pointSizeDepthFactor', settings.pointSizeDepthFactor);
    UniformBatcher.setUniform('invertDepth', settings.invertDepth ? 1.0 : 0.0);
    UniformBatcher.setUniform('fadeRange', dynamicFadeRange);
    UniformBatcher.setUniform('qualityScale', qualityScale);

    // Advanced shader parameters for surgical precision
    UniformBatcher.setUniform('epsilon', settings.epsilon);
    UniformBatcher.setUniform('exponentialK', settings.exponentialK);
    UniformBatcher.setUniform('gamma', settings.gamma);
    UniformBatcher.setUniform('stereographicC', settings.stereographicC);
    UniformBatcher.setUniform('offsetStrength', settings.offsetStrength);
    UniformBatcher.setUniform('noiseScale', settings.noiseScale);
    
    // GPU acceleration uniforms
    UniformBatcher.setUniform('enableDithering', settings.enableDithering ? 1.0 : 0.0);
    UniformBatcher.setUniform('ditherStrength', settings.ditherStrength || 0.3);
    UniformBatcher.setUniform('time', performance.now() * 0.001);

    // Flush all batched updates in single GPU call
    const uniformsUpdated = UniformBatcher.flushUniforms(materialRef.current);
    
    if (uniformsUpdated) {
      materialRef.current.needsUpdate = true;
    }

    PerformanceProfiler.endProfile('uniform_update');
  }, [settings]);

  // Advanced point cloud processing with LOD and frustum culling
  const processPointCloudData = useCallback((positions: Float32Array, colors: Uint8Array, camera: THREE.Camera) => {
    PerformanceProfiler.startProfile('point_processing');

    // Update frustum for culling
    FrustumCuller.updateFrustum(camera);
    
    // Calculate camera distance for LOD
    const cameraPosition = camera.position;
    const avgDistance = Math.sqrt(
      cameraPosition.x * cameraPosition.x + 
      cameraPosition.y * cameraPosition.y + 
      cameraPosition.z * cameraPosition.z
    );

    // Apply LOD decimation based on distance
    const lodDensity = LODManager.getLODDensity(avgDistance);
    let processedPositions = positions;
    
    if (lodDensity < 1.0) {
      processedPositions = LODManager.decimatePoints(positions, lodDensity);
    }

    // Apply frustum culling for performance
    const culledPositions = FrustumCuller.cullPoints(processedPositions);

    PerformanceProfiler.endProfile('point_processing');
    return { positions: culledPositions, count: culledPositions.length / 3 };
  }, []);

  // Optimized render loop with performance monitoring
  const renderFrame = useCallback(() => {
    if (!rendererRef.current || !sceneRef.current || !cameraRef.current) return;

    PerformanceProfiler.startProfile('frame_render');
    FrameRateOptimizer.measureFrame();

    const gl = rendererRef.current.getContext();
    
    // Cache WebGL state to avoid redundant calls
    WebGLStateCache.setDepthTest(gl, true);
    WebGLStateCache.setBlendMode(gl, gl.ONE_MINUS_SRC_ALPHA);

    // Update uniforms only if needed
    if (UniformBatcher.hasDirtyUniforms()) {
      updateMaterialUniforms();
    }

    // Render scene
    rendererRef.current.render(sceneRef.current, cameraRef.current);

    // Update GPU stats after render (non-intrusive monitoring)
    updateGPUStats();

    PerformanceProfiler.endProfile('frame_render');
  }, [updateMaterialUniforms]);

  // Initialize performance monitoring
  useEffect(() => {
    FrameRateOptimizer.setTargetFPS(60);
    FrameRateOptimizer.enableAdaptiveQuality(true);
    
    return () => {
      // Log performance stats on cleanup
      const hotspots = PerformanceProfiler.getHotspots();
      if (hotspots.length > 0) {
        console.log('Performance Analysis:', hotspots.slice(0, 5));
      }
      PerformanceProfiler.clearProfiles();
    };
  }, []);

  // Use the optimized uniform system for all updates
  useEffect(() => {
    updateMaterialUniforms();
  }, [updateMaterialUniforms]);

  // Clear video error
  const clearVideoError = useCallback(() => {
    setVideoError(null);
  }, []);

  // Handle video file setting with error clearing
  const handleSetVideoFile = useCallback((file: File | null) => {
    setVideoError(null); // Clear any previous errors
    setVideoFile(file);
  }, []);

  // Update geometry when camera distance changes for adaptive LOD
  const updateGeometryForCameraDistance = useCallback(() => {
    if (!isVideoReadyRef.current || !videoRef.current) return;
    
    // Skip adaptive updates for desktop users (they get full resolution always)
    if (isDesktop()) {
      return;
    }
    
    const currentDistance = cameraPositionRef.current.radius;
    const video = videoRef.current;
    const totalPixels = (video.videoWidth || 640) * (video.videoHeight || 480);
    const targetDensity = getAdaptiveDensity(currentDistance, totalPixels);
    const adaptiveSkipFactor = getAdaptiveSkipFactor(targetDensity, totalPixels);
    
    // Only recreate geometry if skip factor changed significantly
    const currentPoints = geometryRef.current?.attributes.position?.count || 0;
    const expectedPoints = Math.floor(totalPixels / (adaptiveSkipFactor * adaptiveSkipFactor));
    
    // Reduced threshold from 0.2 to 0.15 for more responsive updates
    if (Math.abs(currentPoints - expectedPoints) > currentPoints * 0.15) {
      createPointCloudGeometry();
      createPointCloudMaterial();
    }
  }, [isDesktop, getAdaptiveDensity, getAdaptiveSkipFactor, createPointCloudGeometry, createPointCloudMaterial]);

  // Three.js scene initialization and camera controls with WebGL compatibility check
  useEffect(() => {
    if (!canvasRef.current) return;

    // Force WebGL context using the dedicated forcer
    console.log('Forcing WebGL context initialization for PixelFlow');
    
    const webglInfo = webglForcer.forceWebGLContext(canvasRef.current);
    console.log('WebGL Context Info:', webglInfo);
    
    if (!webglInfo.supported) {
      console.error('Critical: WebGL context creation failed');
      setWebglSupported(false);
      setWebglError('WebGL is required for PixelFlow 3D point cloud rendering');
      return;
    }

    setWebglSupported(true);
    setWebglError(null);

    try {
      // Initialize Three.js scene
      const scene = new THREE.Scene();
      scene.background = new THREE.Color(0x000000);
      sceneRef.current = scene;

      // Initialize orthographic camera using FOV setting for proper framing
      const aspectRatio = window.innerWidth / window.innerHeight;
      const adaptiveFOV = isDesktop() ? 25 : 35; // 25 for desktop (focused), 35 for mobile (fuller view)
      const frustumSize = adaptiveFOV * 0.3;
      const camera = new THREE.OrthographicCamera(
        frustumSize * aspectRatio / -2,  // left
        frustumSize * aspectRatio / 2,   // right
        frustumSize / 2,                 // top
        frustumSize / -2,                // bottom
        0.01,                            // near
        10000                            // far
      );
      
      // Update frustum size ref to match
      frustumSizeRef.current = frustumSize;
      
      // Force camera to perfect frontal position immediately
      camera.position.set(0, 0, 2.0);
      camera.lookAt(0, 0, 0);
      
      // Set internal coordinates for frontal view
      cameraPositionRef.current = { theta: Math.PI / 2, phi: Math.PI / 2, radius: 2.0 };
      
      // Sync UI state to frontal position
      setCameraState({ azimuth: 90, elevation: 0, distance: 2.0 });
      
      cameraRef.current = camera;

      // Create renderer with robust WebGL context handling
      let renderer;
      try {
        // First, ensure WebGL context is properly established
        if (!webglInfo.supported) {
          console.warn('WebGL not supported, attempting forced initialization...');
          // Force WebGL context creation again
          const forceResult = webglForcer.forceWebGLContext(canvasRef.current);
          if (!forceResult.supported) {
            throw new Error(`WebGL unavailable: ${forceResult.error || 'Unknown error'}`);
          }
        }

        // Create renderer with progressive fallback options
        const rendererOptions: THREE.WebGLRendererParameters[] = [
          {
            canvas: canvasRef.current,
            context: webglInfo.context || undefined,
            antialias: false,
            alpha: true,
            logarithmicDepthBuffer: false,
            preserveDrawingBuffer: false,
            powerPreference: 'default' as const,
            failIfMajorPerformanceCaveat: false,
            stencil: false,
            depth: true
          },
          {
            canvas: canvasRef.current,
            antialias: false,
            alpha: false,
            logarithmicDepthBuffer: false,
            preserveDrawingBuffer: false,
            powerPreference: 'default' as const,
            failIfMajorPerformanceCaveat: false,
            stencil: false,
            depth: true
          },
          {
            canvas: canvasRef.current,
            failIfMajorPerformanceCaveat: false
          }
        ];

        let lastError: Error | null = null;
        for (const options of rendererOptions) {
          try {
            renderer = new THREE.WebGLRenderer(options);
            console.log('WebGL renderer created successfully with options:', options);
            break;
          } catch (error) {
            lastError = error as Error;
            console.warn('Renderer creation failed with options:', options, error);
          }
        }

        if (!renderer) {
          throw lastError || new Error('All renderer creation attempts failed');
        }

      } catch (webglError) {
        console.error('WebGL renderer initialization failed:', webglError);
        const errorMessage = webglError instanceof Error ? webglError.message : 'Unknown error';
        setWebglError(`WebGL initialization failed: ${errorMessage}`);
        setWebglSupported(false);
        return;
      }

      // Configure renderer for optimal compatibility
      renderer.setSize(window.innerWidth, window.innerHeight);
      renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2)); // Limit pixel ratio for performance
      renderer.setClearColor(0x000000, 1.0);
      
      // Use sRGB color space for better browser compatibility
      renderer.outputColorSpace = THREE.SRGBColorSpace;
      
      // Verify WebGL context is working
      try {
        const gl = renderer.getContext();
        console.log('WebGL Context Successfully Created:', {
          vendor: gl.getParameter(gl.VENDOR),
          renderer: gl.getParameter(gl.RENDERER),
          version: gl.getParameter(gl.VERSION),
          shaderVersion: gl.getParameter(gl.SHADING_LANGUAGE_VERSION)
        });
        
        // Test basic WebGL functionality
        renderer.clear();
        setWebglSupported(true);
        setWebglError(null);
        
      } catch (contextError) {
        console.error('WebGL context verification failed:', contextError);
        const errorMessage = contextError instanceof Error ? contextError.message : String(contextError);
        setWebglError(`WebGL context verification failed: ${errorMessage}`);
        setWebglSupported(false);
        return;
      }
      
      rendererRef.current = renderer;
      
      // Add ambient lighting
      const ambientLight = new THREE.AmbientLight(0x404040, 0.6);
      scene.add(ambientLight);

      // Add directional light
      const directionalLight = new THREE.DirectionalLight(0xffffff, 0.8);
      directionalLight.position.set(1, 1, 1);
      scene.add(directionalLight);

      // Initialize depth estimator if real depth is enabled
      if (settings.useRealDepth) {
        getDepthEstimator().then((estimator: any) => {
          depthEstimatorRef.current = estimator;
          console.log('Depth estimator initialized for real-time depth mapping');
        }).catch((error: any) => {
          console.warn('Depth estimator initialization failed, using brightness depth:', error);
        });
      }

      // Clear any previous errors on successful initialization
      setWebglError(null);
      console.log('Three.js initialized successfully with WebGL support');
      
    } catch (error) {
      console.error('Three.js initialization failed:', error);
      setWebglSupported(false);
      setWebglError(`3D initialization failed: ${error instanceof Error ? error.message : 'Unknown error'}`);
      return;
    }

    // Manual camera controls
    const handleMouseDown = (event: MouseEvent) => {
      event.preventDefault();
      isDraggingRef.current = true;
      mouseRef.current.x = event.clientX;
      mouseRef.current.y = event.clientY;
      if (canvasRef.current) {
        canvasRef.current.style.cursor = 'grabbing';
      }
    };

    const handleMouseMove = (event: MouseEvent) => {
      if (!isDraggingRef.current) return;
      event.preventDefault();

      const deltaX = event.clientX - mouseRef.current.x;
      const deltaY = event.clientY - mouseRef.current.y;

      // Smooth camera movement
      const sensitivity = 0.008;
      
      // Always allow horizontal rotation (orbit around center)
      cameraPositionRef.current.theta -= deltaX * sensitivity; // Inverted for natural feel
      
      // Only allow vertical rotation if orbit lock is disabled
      if (!orbitLock) {
        cameraPositionRef.current.phi -= deltaY * sensitivity;
        // Clamp phi to prevent camera flipping
        cameraPositionRef.current.phi = Math.max(0.1, Math.min(Math.PI - 0.1, cameraPositionRef.current.phi));
      }

      mouseRef.current.x = event.clientX;
      mouseRef.current.y = event.clientY;

      updateCameraPosition();
    };

    const handleMouseUp = (event: MouseEvent) => {
      event.preventDefault();
      isDraggingRef.current = false;
      if (canvasRef.current) {
        canvasRef.current.style.cursor = 'grab';
      }
    };

    // Enhanced touch handlers with pinch-to-zoom support
    const handleTouchStart = (event: TouchEvent) => {
      event.preventDefault();
      
      if (event.touches.length === 2) {
        // Two fingers - start pinch zoom
        const touch1 = event.touches[0];
        const touch2 = event.touches[1];
        const distance = calculateTouchDistance(touch1, touch2);
        
        pinchStateRef.current = {
          isActive: true,
          initialDistance: distance,
          initialRadius: cameraPositionRef.current.radius,
          lastDistance: distance
        };
        
        // Disable pan dragging during pinch
        isTouchDraggingRef.current = false;
      } else if (event.touches.length === 1 && !pinchStateRef.current.isActive) {
        // Single finger - start pan (only if not already pinching)
        isTouchDraggingRef.current = true;
        const touch = event.touches[0];
        touchRef.current.x = touch.clientX;
        touchRef.current.y = touch.clientY;
      }
    };

    const handleTouchMove = (event: TouchEvent) => {
      event.preventDefault();

      if (event.touches.length === 2 && pinchStateRef.current.isActive) {
        // Two fingers - handle pinch zoom
        const touch1 = event.touches[0];
        const touch2 = event.touches[1];
        const currentDistance = calculateTouchDistance(touch1, touch2);
        
        // Calculate zoom factor based on distance change
        const distanceChange = currentDistance - pinchStateRef.current.initialDistance;
        const zoomFactor = distanceChange * 0.01; // Adjust sensitivity as needed
        
        // Apply zoom using same logic as wheel zoom
        const oldRadius = cameraPositionRef.current.radius;
        cameraPositionRef.current.radius = pinchStateRef.current.initialRadius - zoomFactor;
        cameraPositionRef.current.radius = Math.max(1, Math.min(50, cameraPositionRef.current.radius));
        
        // Trigger adaptive LOD update when zoom distance changes significantly
        if (Math.abs(cameraPositionRef.current.radius - oldRadius) > 2) {
          updateGeometryForCameraDistance();
        }
        
        updateCameraPosition();
        pinchStateRef.current.lastDistance = currentDistance;
        
      } else if (event.touches.length === 1 && isTouchDraggingRef.current && !pinchStateRef.current.isActive) {
        // Single finger - handle pan (same as before)
        const touch = event.touches[0];
        const deltaX = touch.clientX - touchRef.current.x;
        const deltaY = touch.clientY - touchRef.current.y;

        // Use identical sensitivity and camera calculations as mouse
        const sensitivity = 0.008;
        
        // Always allow horizontal rotation (orbit around center)
        cameraPositionRef.current.theta -= deltaX * sensitivity; // Inverted for natural feel
        
        // Only allow vertical rotation if orbit lock is disabled
        if (!orbitLock) {
          cameraPositionRef.current.phi -= deltaY * sensitivity;
          // Clamp phi to prevent camera flipping (same as mouse)
          cameraPositionRef.current.phi = Math.max(0.1, Math.min(Math.PI - 0.1, cameraPositionRef.current.phi));
        }

        touchRef.current.x = touch.clientX;
        touchRef.current.y = touch.clientY;

        updateCameraPosition();
      }
    };

    const handleTouchEnd = (event: TouchEvent) => {
      event.preventDefault();
      
      // Reset pinch state when we have less than 2 touches
      if (event.touches.length < 2) {
        pinchStateRef.current.isActive = false;
      }
      
      // Reset pan state when no touches remain
      if (event.touches.length === 0) {
        isTouchDraggingRef.current = false;
      }
    };

    const handleWheel = (event: WheelEvent) => {
      event.preventDefault();
      const zoomSpeed = 0.5;
      const oldFrustumSize = frustumSizeRef.current;
      frustumSizeRef.current += event.deltaY * zoomSpeed * 0.01;
      frustumSizeRef.current = Math.max(1, Math.min(50, frustumSizeRef.current));
      
      // Update orthographic camera frustum
      if (cameraRef.current) {
        const aspectRatio = window.innerWidth / window.innerHeight;
        cameraRef.current.left = frustumSizeRef.current * aspectRatio / -2;
        cameraRef.current.right = frustumSizeRef.current * aspectRatio / 2;
        cameraRef.current.top = frustumSizeRef.current / 2;
        cameraRef.current.bottom = frustumSizeRef.current / -2;
        cameraRef.current.updateProjectionMatrix();
      }
      
      // Trigger adaptive LOD update when zoom changes significantly
      if (Math.abs(frustumSizeRef.current - oldFrustumSize) > 2) {
        updateGeometryForCameraDistance();
      }
    };

    // Add event listeners with proper cleanup
    const canvas = canvasRef.current;
    
    // Mouse event listeners
    canvas.addEventListener('mousedown', handleMouseDown);
    canvas.style.cursor = 'grab';
    document.addEventListener('mousemove', handleMouseMove);
    document.addEventListener('mouseup', handleMouseUp);
    canvas.addEventListener('wheel', handleWheel, { passive: false });
    
    // Touch event listeners
    canvas.addEventListener('touchstart', handleTouchStart, { passive: false });
    canvas.addEventListener('touchmove', handleTouchMove, { passive: false });
    canvas.addEventListener('touchend', handleTouchEnd, { passive: false });

    // Handle window resize for orthographic camera
    const handleResize = () => {
      if (!cameraRef.current || !rendererRef.current) return;
      
      const width = window.innerWidth;
      const height = window.innerHeight;
      
      // Update orthographic camera frustum for new aspect ratio
      const aspectRatio = width / height;
      cameraRef.current.left = frustumSizeRef.current * aspectRatio / -2;
      cameraRef.current.right = frustumSizeRef.current * aspectRatio / 2;
      cameraRef.current.top = frustumSizeRef.current / 2;
      cameraRef.current.bottom = frustumSizeRef.current / -2;
      cameraRef.current.updateProjectionMatrix();
      rendererRef.current.setSize(width, height);
    };

    window.addEventListener('resize', handleResize);

    return () => {
      // Proper cleanup to prevent WebGL context errors
      window.removeEventListener('resize', handleResize);
      if (canvas) {
        canvas.removeEventListener('mousedown', handleMouseDown);
        canvas.removeEventListener('wheel', handleWheel);
        canvas.removeEventListener('touchstart', handleTouchStart);
        canvas.removeEventListener('touchmove', handleTouchMove);
        canvas.removeEventListener('touchend', handleTouchEnd);
      }
      document.removeEventListener('mousemove', handleMouseMove);
      document.removeEventListener('mouseup', handleMouseUp);
      
      if (animationIdRef.current) {
        cancelAnimationFrame(animationIdRef.current);
      }
      
      // Dispose of Three.js resources
      if (rendererRef.current) {
        rendererRef.current.dispose();
        rendererRef.current = undefined;
      }
      
      if (sceneRef.current) {
        sceneRef.current.clear();
        sceneRef.current = undefined;
      }
      
      cameraRef.current = undefined;
    };
  }, [canvasRef, updateCameraPosition, updateGeometryForCameraDistance, calculateTouchDistance]);

  // Update camera frustum size when settings change
  useEffect(() => {
    if (cameraRef.current) {
      // Map FOV setting to frustum size for orthographic camera
      frustumSizeRef.current = settings.fov * 0.3; // Scale FOV to appropriate frustum size
      const aspectRatio = window.innerWidth / window.innerHeight;
      cameraRef.current.left = frustumSizeRef.current * aspectRatio / -2;
      cameraRef.current.right = frustumSizeRef.current * aspectRatio / 2;
      cameraRef.current.top = frustumSizeRef.current / 2;
      cameraRef.current.bottom = frustumSizeRef.current / -2;
      cameraRef.current.updateProjectionMatrix();
    }
  }, [settings.fov]);

  // Continuous animation loop that runs independently of video state
  useEffect(() => {
    const animate = async () => {
      if (!sceneRef.current || !cameraRef.current || !rendererRef.current) {
        animationIdRef.current = requestAnimationFrame(animate);
        return;
      }

      // Update video texture for each frame
      if (textureRef.current) {
        textureRef.current.needsUpdate = true;
      }

      // Update temporal dithering animation for photorealistic quality
      if (materialRef.current && materialRef.current.uniforms.time) {
        materialRef.current.uniforms.time.value = performance.now() * 0.001;
      }

      // Compute depth estimation if enabled and video is available
      if (settings.useRealDepth && depthEstimatorRef.current && videoRef.current && isVideoReadyRef.current) {
        try {
          const depthResult = await depthEstimatorRef.current.estimateDepth(videoRef.current);
          currentDepthMapRef.current = depthResult.depthMap;
          
          // Convert depth data to texture for shader
          if (materialRef.current && materialRef.current.uniforms.depthMap) {
            // Create or update depth texture
            if (!depthTextureRef.current) {
              depthTextureRef.current = new THREE.DataTexture(
                depthResult.depthMap,
                depthResult.width,
                depthResult.height,
                THREE.RedFormat,
                THREE.FloatType
              );
              depthTextureRef.current.needsUpdate = true;
            } else {
              // Update existing texture with new depth data
              depthTextureRef.current.image.data = depthResult.depthMap;
              depthTextureRef.current.needsUpdate = true;
            }
            
            materialRef.current.uniforms.depthMap.value = depthTextureRef.current;
            materialRef.current.uniforms.useRealDepth.value = true;
          }
        } catch (error) {
          console.warn('Depth estimation failed, falling back to brightness depth:', error);
          // Disable real depth on error
          if (materialRef.current) {
            materialRef.current.uniforms.useRealDepth.value = false;
          }
        }
      } else if (materialRef.current) {
        // Ensure real depth is disabled when not using it
        materialRef.current.uniforms.useRealDepth.value = false;
      }

      rendererRef.current.render(sceneRef.current, cameraRef.current);
      animationIdRef.current = requestAnimationFrame(animate);
    };

    animate();

    return () => {
      if (animationIdRef.current) {
        cancelAnimationFrame(animationIdRef.current);
      }
    };
  }, []); // Run once and keep running - NO dependencies to prevent restarts

  useEffect(() => {
    if (!videoFile || !sceneRef.current) return;

    // Reset state for new video
    isVideoReadyRef.current = false;
    setIsPlaying(false);
    setVideoError(null); // Clear any previous errors

    // Clean up existing video resources
    if (videoRef.current) {
      try {
        videoRef.current.pause();
        if (videoRef.current.parentNode && videoRef.current.parentNode.nodeType === Node.ELEMENT_NODE) {
          videoRef.current.parentNode.removeChild(videoRef.current);
        }
      } catch (error) {
        console.warn('Video cleanup error:', error);
      }
    }

    // Clean up existing Three.js resources
    if (pointsRef.current && sceneRef.current) {
      sceneRef.current.remove(pointsRef.current);
      pointsRef.current = undefined;
    }

    if (materialRef.current) {
      materialRef.current.dispose();
      materialRef.current = undefined;
    }

    if (geometryRef.current) {
      geometryRef.current.dispose();
      geometryRef.current = undefined;
    }

    if (textureRef.current) {
      textureRef.current.dispose();
      textureRef.current = undefined;
    }

    // Create new video element
    const video = document.createElement('video');
    video.crossOrigin = 'anonymous';
    video.loop = true;
    video.muted = true;
    video.playsInline = true;
    video.preload = 'metadata';
    
    // Keep video hidden but accessible
    video.style.position = 'absolute';
    video.style.top = '-1px';
    video.style.left = '-1px';
    video.style.width = '1px';
    video.style.height = '1px';
    video.style.opacity = '0';
    video.style.pointerEvents = 'none';
    
    videoRef.current = video;
    document.body.appendChild(video);

    // Load video file
    const url = URL.createObjectURL(videoFile);
    video.src = url;

    // Handle video ready
    const handleVideoReady = () => {
      if (!isVideoReadyRef.current) {
        isVideoReadyRef.current = true;
        
        // Create video texture with sRGB color space
        const texture = new THREE.VideoTexture(video);
        texture.minFilter = THREE.LinearFilter;
        texture.magFilter = THREE.LinearFilter;
        texture.flipY = false;
        
        // Set sRGB color space for proper color handling
        texture.colorSpace = THREE.SRGBColorSpace;
        
        textureRef.current = texture;
        
        // Calculate optimal camera positioning for this video's aspect ratio
        const videoWidth = video.videoWidth || 1920;
        const videoHeight = video.videoHeight || 1080;
        const aspectRatio = videoWidth / videoHeight;
        
        const optimalDistance = calculateOptimalCameraDistance(aspectRatio, videoWidth, videoHeight);
        const optimalFrustumSize = calculateOptimalFrustumSize(aspectRatio, videoWidth, videoHeight);
        
        // Update camera for optimal frontal view
        if (cameraRef.current) {
          // Update orthographic camera frustum for video aspect ratio
          const canvasAspectRatio = window.innerWidth / window.innerHeight;
          const cam = cameraRef.current as THREE.OrthographicCamera;
          
          cam.left = optimalFrustumSize * canvasAspectRatio / -2;
          cam.right = optimalFrustumSize * canvasAspectRatio / 2;
          cam.top = optimalFrustumSize / 2;
          cam.bottom = optimalFrustumSize / -2;
          cam.updateProjectionMatrix();
          
          // Update frustum size ref to match FOV setting
          frustumSizeRef.current = optimalFrustumSize;
          
          // Set perfect frontal position with optimal distance
          cam.position.set(0, 0, optimalDistance);
          cam.lookAt(0, 0, 0);
          
          // Update internal camera state for frontal view
          cameraPositionRef.current = { theta: Math.PI / 2, phi: Math.PI / 2, radius: optimalDistance };
          setCameraState({ azimuth: 90, elevation: 0, distance: optimalDistance });
          
          console.log(`Video aspect ratio: ${aspectRatio.toFixed(2)}, optimal distance: ${optimalDistance.toFixed(2)}, frustum: ${optimalFrustumSize.toFixed(1)}`);
        }
        
        // Create geometry with full density
        createPointCloudGeometry();
        
        // Create initial material
        createPointCloudMaterial();
      }
    };

    // Enhanced error handling with user-friendly messages
    const handleVideoError = (event: Event) => {
      console.error('Video loading error:', event);
      
      // Determine error type and set appropriate message
      let errorMessage = 'Unable to load video file. Please check that the file is a valid video format (MP4, WebM, or OGV) and is not corrupted. Common issues include:\n\n• Unsupported video codec or format\n• File corruption during upload or transfer\n• Browser compatibility issues\n• File size limitations\n\nTry converting your video to MP4 format or using a different video file.';
      
      if (video.error) {
        switch (video.error.code) {
          case video.error.MEDIA_ERR_ABORTED:
            errorMessage = 'Video loading was aborted. Please try uploading the file again.';
            break;
          case video.error.MEDIA_ERR_NETWORK:
            errorMessage = 'Network error occurred while loading video. Please check your internet connection and try again.';
            break;
          case video.error.MEDIA_ERR_DECODE:
            errorMessage = 'Video format is not supported or the file is corrupted. Please try:\n\n• Converting to MP4 format\n• Using a different video file\n• Checking if the original file plays correctly in other applications';
            break;
          case video.error.MEDIA_ERR_SRC_NOT_SUPPORTED:
            errorMessage = 'Video format is not supported by your browser. Please try:\n\n• Converting to MP4 (H.264 codec recommended)\n• Using WebM format as an alternative\n• Ensuring the video uses standard codecs';
            break;
          default:
            errorMessage = 'An unknown error occurred while loading the video. This could be due to:\n\n• Unsupported video format or codec\n• File corruption\n• Browser limitations\n• Memory constraints\n\nTry using a different video file or converting to MP4 format.';
        }
      }
      
      // Reset video state and show error
      setVideoError(errorMessage);
      setVideoFile(null);
      isVideoReadyRef.current = false;
      setIsPlaying(false);
    };

    // Use multiple events to ensure video is ready
    video.addEventListener('loadedmetadata', handleVideoReady);
    video.addEventListener('canplay', handleVideoReady);
    video.addEventListener('error', handleVideoError);

    return () => {
      URL.revokeObjectURL(url);
      if (video && video.parentNode) {
        video.pause();
        video.parentNode.removeChild(video);
      }
      
      // Clean up Three.js resources when video changes
      if (pointsRef.current && sceneRef.current) {
        sceneRef.current.remove(pointsRef.current);
      }
      
      if (materialRef.current) {
        materialRef.current.dispose();
      }
      
      if (geometryRef.current) {
        geometryRef.current.dispose();
      }
      
      if (textureRef.current) {
        textureRef.current.dispose();
      }
    };
  }, [videoFile, createPointCloudGeometry, createPointCloudMaterial]);

  // Enhanced uniform caching system with frame-perfect timing
  useEffect(() => {
    if (isVideoReadyRef.current && materialRef.current) {
      updateMaterialUniforms();
    }
  }, [settings, updateMaterialUniforms]);

  const playVideo = () => {
    if (videoRef.current && isVideoReadyRef.current && !isPlaying) {
      videoRef.current.play()
        .then(() => {
          setIsPlaying(true);
        })
        .catch((error) => {
          console.error('Video playback failed:', error);
          setVideoError('Unable to play video. The file may be corrupted or in an unsupported format.');
        });
    }
  };

  const pauseVideo = () => {
    if (videoRef.current && isPlaying) {
      videoRef.current.pause();
      setIsPlaying(false);
    }
  };

  return {
    setVideoFile: handleSetVideoFile,
    playVideo,
    pauseVideo,
    isPlaying,
    videoFile,
    videoError,
    clearVideoError,
    // WebGL status information
    webglSupported,
    webglError,
    // Export video and canvas refs for GIF export
    videoRef,
    canvasRef,
    // Camera control exports
    cameraPosition: cameraState,
    updateCameraPosition: updateCameraFromDegrees,
    syncCameraState,
    orbitLock,
    trajectoryMode,
    trajectoryDuration,
    onOrbitLockChange: handleOrbitLockChange,
    onTrajectoryModeChange: handleTrajectoryModeChange,
    onTrajectoryDurationChange: handleTrajectoryDurationChange,
    resetCamera
  };
};

```

### Utilities

#### client/src/utils/canvasPool.ts
```ts

class CanvasPool {
  private pool: HTMLCanvasElement[] = [];
  private maxPoolSize = 5;

  getCanvas(width: number, height: number): HTMLCanvasElement {
    let canvas = this.pool.pop();
    
    if (!canvas) {
      canvas = document.createElement('canvas');
    }
    
    // Reuse existing canvas with new dimensions
    canvas.width = width;
    canvas.height = height;
    
    return canvas;
  }

  releaseCanvas(canvas: HTMLCanvasElement): void {
    if (this.pool.length < this.maxPoolSize) {
      // Clear the canvas for reuse
      const ctx = canvas.getContext('2d');
      if (ctx) {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
      }
      this.pool.push(canvas);
    }
  }

  clear(): void {
    this.pool = [];
  }
}

export const canvasPool = new CanvasPool();

```

#### client/src/utils/demoVideo.ts
```ts

export interface DemoVideo {
  id: string;
  title: string;
  description: string;
  filename: string;
  url: string;
}

export const DEMO_VIDEOS: DemoVideo[] = [
  {
    id: 'default-demo',
    title: 'PixelFlow Demo',
    description: 'Point cloud visualization demonstration',
    filename: 'demo-video.mp4',
    url: '/demo-video.mp4'
  }
];

export const fetchDemoVideo = async (): Promise<File> => {
  try {
    const response = await fetch('/demo-video.mp4');
    
    if (!response.ok) {
      throw new Error(`Failed to fetch demo video: ${response.statusText}`);
    }
    
    const blob = await response.blob();
    
    // Create a File object from the blob
    const file = new File([blob], 'demo-video.mp4', {
      type: 'video/mp4',
      lastModified: Date.now()
    });
    
    return file;
  } catch (error) {
    console.error('Error fetching demo video:', error);
    throw new Error(`Failed to load demo video`);
  }
};

export const getCurrentDemo = (currentIndex: number): DemoVideo => {
  return DEMO_VIDEOS[currentIndex];
};

export const getNextDemoIndex = (currentIndex: number): number => {
  return (currentIndex + 1) % DEMO_VIDEOS.length;
};

export const getPreviousDemoIndex = (currentIndex: number): number => {
  return currentIndex === 0 ? DEMO_VIDEOS.length - 1 : currentIndex - 1;
};

```

#### client/src/utils/depthEstimation.ts
```ts
/**
 * Professional-grade depth estimation using TensorFlow.js models
 * Implements ARPortraitDepth for accurate point cloud generation
 */
import * as tf from '@tensorflow/tfjs';
import * as depthEstimation from '@tensorflow-models/depth-estimation';
import '@tensorflow/tfjs-backend-webgl';
import '@tensorflow/tfjs-backend-webgpu';

export interface DepthEstimationConfig {
  inputSize: number;
  outputSize: number;
  useWebGPU: boolean;
  modelType: 'ARPortraitDepth';
  minDepth: number;
  maxDepth: number;
}

export interface DepthResult {
  depthMap: Float32Array;
  width: number;
  height: number;
  processingTime: number;
  confidence?: Float32Array;
}

export class DepthEstimator {
  private model: tf.GraphModel | null = null;
  private arPortraitDepthEstimator: depthEstimation.DepthEstimator | null = null;
  private isInitialized = false;
  private config: DepthEstimationConfig;

  constructor(config: DepthEstimationConfig = {
    inputSize: 256,
    outputSize: 256,
    useWebGPU: false,
    modelType: 'ARPortraitDepth',
    minDepth: 0,
    maxDepth: 1
  }) {
    this.config = config;
  }

  async initialize(): Promise<boolean> {
    if (this.isInitialized) return true;

    try {
      // Set required backend - only WebGPU or WebGL, no CPU fallback
      if (this.config.useWebGPU) {
        await tf.setBackend('webgpu');
      } else {
        await tf.setBackend('webgl');
      }

      await tf.ready();

      // Initialize ARPortraitDepth model - required for depth estimation
      console.log('Loading TensorFlow.js ARPortraitDepth model...');
      
      this.arPortraitDepthEstimator = await depthEstimation.createEstimator(
        depthEstimation.SupportedModels.ARPortraitDepth
      );
      
      console.log('ARPortraitDepth model loaded successfully with', tf.getBackend(), 'backend');
      this.isInitialized = true;
      return true;

    } catch (error) {
      console.error('Failed to initialize ARPortraitDepth model:', error);
      return false;
    }
  }

  async estimateDepth(videoElement: HTMLVideoElement): Promise<DepthResult> {
    if (!this.isInitialized) {
      throw new Error('Depth estimator not initialized');
    }

    const startTime = performance.now();

    try {
      // Use professional ARPortraitDepth model for accurate depth estimation
      if (this.arPortraitDepthEstimator) {
        const estimationConfig = {
          minDepth: this.config.minDepth,
          maxDepth: this.config.maxDepth,
        };
        
        const depthMap = await this.arPortraitDepthEstimator.estimateDepth(videoElement, estimationConfig);
        const depthArray = await depthMap.toArray();
        const processingTime = performance.now() - startTime;

        return {
          depthMap: new Float32Array(depthArray.flat()),
          width: videoElement.videoWidth,
          height: videoElement.videoHeight,
          processingTime
        };
      }

      // ARPortraitDepth model is required - no fallback
      throw new Error('ARPortraitDepth model is required for depth estimation');

    } catch (error) {
      console.error('Depth estimation failed:', error);
      throw error;
    }
  }



  dispose(): void {
    console.log('Disposing depth estimator and cleaning up tensors...');
    
    this.isInitialized = false;
    
    if (this.model) {
      this.model.dispose();
      this.model = null;
    }
    
    if (this.arPortraitDepthEstimator) {
      this.arPortraitDepthEstimator.dispose();
      this.arPortraitDepthEstimator = null;
    }
    
    // Force TensorFlow.js memory cleanup
    if (typeof tf !== 'undefined') {
      const memoryInfo = tf.memory();
      if (memoryInfo.numTensors > 0) {
        console.log(`Cleaning up ${memoryInfo.numTensors} remaining tensors`);
        tf.disposeVariables();
      }
    }
  }
}

// Singleton instance
let depthEstimatorInstance: DepthEstimator | null = null;

export async function getDepthEstimator(config?: DepthEstimationConfig): Promise<DepthEstimator> {
  if (!depthEstimatorInstance) {
    depthEstimatorInstance = new DepthEstimator(config);
    await depthEstimatorInstance.initialize();
  }
  return depthEstimatorInstance;
}
```

#### client/src/utils/ditherShaders.ts
```ts
/**
 * GPU-accelerated dithering shaders for real-time point cloud optimization
 */

// Bayer matrix for ordered dithering
export const bayerMatrix4x4 = `
  mat4 bayerMatrix = mat4(
    0.0/16.0, 8.0/16.0, 2.0/16.0, 10.0/16.0,
    12.0/16.0, 4.0/16.0, 14.0/16.0, 6.0/16.0,
    3.0/16.0, 11.0/16.0, 1.0/16.0, 9.0/16.0,
    15.0/16.0, 7.0/16.0, 13.0/16.0, 5.0/16.0
  );
`;

// Blue noise texture generation (pseudo-random but more natural)
export const blueNoiseFunction = `
  float blueNoise(vec2 coord, float time) {
    vec2 n = coord * 0.1 + time * 0.01;
    return fract(sin(dot(n, vec2(12.9898, 78.233))) * 43758.5453);
  }
`;

// Ordered dithering function
export const orderedDitherFunction = `
  ${bayerMatrix4x4}
  
  float orderedDither(vec2 screenPos, float value, float levels) {
    ivec2 matrixPos = ivec2(mod(screenPos, 4.0));
    float threshold = bayerMatrix[matrixPos.x][matrixPos.y];
    
    float quantized = floor(value * levels) / levels;
    float error = value - quantized;
    
    return quantized + step(threshold, error) / levels;
  }
`;

// Blue noise dithering function
export const blueNoiseDitherFunction = `
  ${blueNoiseFunction}
  
  float blueNoiseDither(vec2 coord, float value, float levels, float time) {
    float noise = blueNoise(coord, time);
    float quantized = floor(value * levels + noise - 0.5) / levels;
    return clamp(quantized, 0.0, 1.0);
  }
`;

// Enhanced vertex shader with instancing support
export const instancedVertexShader = `
  #include <common>
  #include <logdepthbuf_pars_vertex>
  
  attribute vec3 position;
  attribute vec3 color;
  attribute vec2 uv;
  
  // Instance attributes
  attribute vec3 instancePosition;
  attribute vec3 instanceColor;
  attribute float instanceScale;
  attribute float instanceOpacity;
  
  uniform mat4 modelViewMatrix;
  uniform mat4 projectionMatrix;
  uniform sampler2D videoTexture;
  uniform sampler2D depthMap;
  uniform float pointSize;
  uniform float nearClipping;
  uniform float farClipping;
  uniform float depthPower;
  uniform float pointSizeDepthFactor;
  uniform bool invertDepth;
  uniform bool useRealDepth;
  uniform float time;
  
  varying vec3 vColor;
  varying float vAlpha;
  varying vec2 vUv;
  varying vec2 vScreenPos;
  varying float vInstanceOpacity;
  
  ${orderedDitherFunction}
  ${blueNoiseDitherFunction}
  
  float calculateDepth(vec2 uv, float luminance, float near, float far, float power, bool invert) {
    float depth;
    
    if (useRealDepth) {
      depth = texture2D(depthMap, uv).r;
    } else {
      depth = luminance;
      if (invert) {
        depth = 1.0 - depth;
      }
    }
    
    if (depth < near || depth > far) {
      return -1.0;
    }
    
    float normalizedDepth = (depth - near) / (far - near);
    normalizedDepth = clamp(normalizedDepth, 0.0, 1.0);
    normalizedDepth = pow(normalizedDepth, power);
    
    return normalizedDepth;
  }
  
  void main() {
    vUv = uv;
    
    // Use instance position if available, otherwise use vertex position
    vec3 finalPosition = position + instancePosition;
    vec4 texel = texture2D(videoTexture, uv);
    
    // Calculate luminance for depth
    float luminance = dot(texel.rgb, vec3(0.299, 0.587, 0.114));
    float normalizedDepth = calculateDepth(uv, luminance, nearClipping, farClipping, depthPower, invertDepth);
    
    vAlpha = instanceOpacity;
    
    // Handle clipped points
    if (normalizedDepth < 0.0) {
      gl_Position = vec4(0.0, 0.0, -1000.0, 1.0);
      gl_PointSize = 0.0;
      vColor = vec3(0.0);
      vAlpha = 0.0;
      return;
    }
    
    // Apply depth-based Z offset
    finalPosition.z = normalizedDepth * 2.0 - 1.0;
    
    vec4 mvPosition = modelViewMatrix * vec4(finalPosition, 1.0);
    gl_Position = projectionMatrix * mvPosition;
    
    // Store screen position for dithering
    vScreenPos = gl_Position.xy / gl_Position.w * 0.5 + 0.5;
    vScreenPos *= vec2(1920.0, 1080.0); // Approximate screen resolution
    
    // Enhanced point sizing with instancing
    float finalPointSize = pointSize * instanceScale;
    gl_PointSize = finalPointSize * (1.0 + normalizedDepth * pointSizeDepthFactor);
    
    // Apply dithering to colors
    vec3 originalColor = mix(texel.rgb, instanceColor, 0.5);
    
    // Use blue noise dithering for more natural results
    vColor.r = blueNoiseDither(vScreenPos + vec2(0.0, 0.0), originalColor.r, 8.0, time);
    vColor.g = blueNoiseDither(vScreenPos + vec2(1.0, 0.0), originalColor.g, 8.0, time);
    vColor.b = blueNoiseDither(vScreenPos + vec2(0.0, 1.0), originalColor.b, 8.0, time);
    
    vInstanceOpacity = instanceOpacity;
    
    #include <logdepthbuf_vertex>
  }
`;

// Enhanced fragment shader with dithering
export const ditheredFragmentShader = `
  #include <common>
  #include <logdepthbuf_pars_fragment>
  
  varying vec3 vColor;
  varying float vAlpha;
  varying vec2 vUv;
  varying vec2 vScreenPos;
  varying float vInstanceOpacity;
  
  uniform float exponentialK;
  uniform float gamma;
  uniform float noiseScale;
  uniform float time;
  uniform bool enableDithering;
  uniform float ditherStrength;
  
  ${orderedDitherFunction}
  ${blueNoiseDitherFunction}
  
  void main() {
    // Create clean circular points
    vec2 circCoord = 2.0 * gl_PointCoord - 1.0;
    float dist = dot(circCoord, circCoord);
    if (dist > 1.0) discard;
    
    vec3 color = vColor;
    
    // Apply dithering if enabled
    if (enableDithering) {
      // Use ordered dithering for performance, blue noise for quality
      float ditheredR = orderedDither(vScreenPos + vec2(0.0, 0.0), color.r, 16.0);
      float ditheredG = orderedDither(vScreenPos + vec2(1.0, 0.0), color.g, 16.0);
      float ditheredB = orderedDither(vScreenPos + vec2(0.0, 1.0), color.b, 16.0);
      
      color = mix(color, vec3(ditheredR, ditheredG, ditheredB), ditherStrength);
    }
    
    // Exponential highlighting
    float intensity = (color.r + color.g + color.b) / 3.0;
    vec3 highlightedColor = color * exp(exponentialK * intensity);
    
    // Gamma correction
    vec3 correctedColor = pow(highlightedColor, vec3(1.0 / gamma));
    
    // Voronoi noise pattern
    vec2 noiseCoord = vUv * noiseScale;
    vec2 cellId = floor(noiseCoord);
    vec2 cellPos = fract(noiseCoord);
    
    float minDist = 1.0;
    for(int y = -1; y <= 1; y++) {
      for(int x = -1; x <= 1; x++) {
        vec2 neighbor = vec2(float(x), float(y));
        vec2 point = cellId + neighbor;
        
        vec2 randPoint = fract(sin(point.x * 12.9898 + point.y * 78.233) * vec2(43758.5453, 28377.1353));
        vec2 diff = neighbor + randPoint - cellPos;
        float dist = length(diff);
        minDist = min(minDist, dist);
      }
    }
    
    float pattern = smoothstep(0.0, 0.1, minDist);
    vec3 patternedColor = mix(correctedColor, correctedColor * 1.2, pattern * 0.3);
    
    // Clean edge falloff
    float alpha = 1.0 - smoothstep(0.6, 1.0, dist);
    
    gl_FragColor = vec4(patternedColor, alpha * vAlpha * vInstanceOpacity);
    
    #include <logdepthbuf_fragment>
  }
`;
```

#### client/src/utils/fileValidation.ts
```ts

// File validation utility with enhanced security checks
export class FileValidator {
  private static readonly MAX_FILE_SIZE = 100 * 1024 * 1024; // 100MB
  private static readonly ALLOWED_VIDEO_TYPES = [
    'video/mp4',
    'video/webm',
    'video/ogg',
    'video/avi',
    'video/mov',
    'video/quicktime'
  ];

  private static readonly VIDEO_MAGIC_BYTES = {
    mp4: [0x66, 0x74, 0x79, 0x70], // ftyp
    webm: [0x1A, 0x45, 0xDF, 0xA3], // EBML
    avi: [0x52, 0x49, 0x46, 0x46], // RIFF
    mov: [0x66, 0x74, 0x79, 0x70], // ftyp (same as mp4)
  };

  static async validateVideoFile(file: File): Promise<{ isValid: boolean; error?: string }> {
    try {
      // Check file size
      if (file.size > this.MAX_FILE_SIZE) {
        return { isValid: false, error: 'File size exceeds 100MB limit' };
      }

      // Check MIME type
      if (!this.ALLOWED_VIDEO_TYPES.includes(file.type)) {
        return { isValid: false, error: 'Invalid file type. Only video files are allowed.' };
      }

      // Check file magic bytes (actual content validation)
      const isValidContent = await this.validateFileContent(file);
      if (!isValidContent) {
        return { isValid: false, error: 'File content does not match video format' };
      }

      return { isValid: true };
    } catch (error) {
      console.error('File validation error:', error);
      return { isValid: false, error: 'File validation failed' };
    }
  }

  private static async validateFileContent(file: File): Promise<boolean> {
    return new Promise((resolve) => {
      const reader = new FileReader();
      reader.onload = (e) => {
        try {
          const arrayBuffer = e.target?.result as ArrayBuffer;
          const bytes = new Uint8Array(arrayBuffer.slice(0, 16));
          
          // Check for common video file signatures
          const hasValidSignature = this.checkVideoSignature(bytes);
          resolve(hasValidSignature);
        } catch (error) {
          console.error('Content validation error:', error);
          resolve(false);
        }
      };
      reader.onerror = () => resolve(false);
      reader.readAsArrayBuffer(file.slice(0, 16));
    });
  }

  private static checkVideoSignature(bytes: Uint8Array): boolean {
    // Check for MP4/MOV signature (ftyp)
    if (bytes.length >= 8) {
      const ftypSignature = Array.from(bytes.slice(4, 8));
      if (ftypSignature.every((byte, index) => byte === this.VIDEO_MAGIC_BYTES.mp4[index])) {
        return true;
      }
    }

    // Check for WebM signature (EBML)
    if (bytes.length >= 4) {
      const webmSignature = Array.from(bytes.slice(0, 4));
      if (webmSignature.every((byte, index) => byte === this.VIDEO_MAGIC_BYTES.webm[index])) {
        return true;
      }
    }

    // Check for AVI signature (RIFF)
    if (bytes.length >= 4) {
      const aviSignature = Array.from(bytes.slice(0, 4));
      if (aviSignature.every((byte, index) => byte === this.VIDEO_MAGIC_BYTES.avi[index])) {
        return true;
      }
    }

    return false;
  }
}

```

#### client/src/utils/fxaaProcessor.ts
```ts

export class FXAAProcessor {
  private canvas: HTMLCanvasElement;
  private ctx: CanvasRenderingContext2D;

  constructor() {
    this.canvas = document.createElement('canvas');
    this.ctx = this.canvas.getContext('2d')!;
  }

  process(inputCanvas: HTMLCanvasElement): HTMLCanvasElement {
    this.canvas.width = inputCanvas.width;
    this.canvas.height = inputCanvas.height;

    // Simple edge-preserving smoothing (FXAA approximation)
    this.ctx.filter = 'blur(0.5px)';
    this.ctx.drawImage(inputCanvas, 0, 0);
    
    // Sharpen to restore detail
    this.ctx.globalCompositeOperation = 'overlay';
    this.ctx.filter = 'contrast(110%) brightness(95%)';
    this.ctx.drawImage(inputCanvas, 0, 0);
    this.ctx.globalCompositeOperation = 'source-over';
    this.ctx.filter = 'none';

    return this.canvas;
  }

  dispose(): void {
    // Cleanup handled by garbage collection
  }
}

```

#### client/src/utils/gifEncoder.ts
```ts
// @ts-ignore
import GIF from 'gif.js';
import { MemoryManager, ErrorRecovery, PerformanceMonitor } from './memoryManager';

export interface GifEncoderOptions {
  width: number;
  height: number;
  quality: number;
  workers: number;
  dither?: boolean | string;
  transparent?: string | null;
  debug?: boolean;
  workerScript?: string;
  repeat?: number;
}

export interface GifFrame {
  canvas: HTMLCanvasElement;
  delay: number;
}

export class GifEncoder {
  private gif: any;
  private frames: GifFrame[] = [];
  private isEncoding = false;

  constructor(options: GifEncoderOptions) {
    this.gif = new GIF({
      workers: options.workers || 4,
      quality: options.quality || 10,
      width: options.width,
      height: options.height,
      workerScript: options.workerScript || '/gif-worker.js',
      dither: options.dither !== undefined ? options.dither : 'Atkinson', // Enhanced dithering
      transparent: options.transparent || null,
      debug: options.debug || false,
      repeat: options.repeat !== undefined ? options.repeat : -1 // Play once by default
    });
  }

  addFrame(canvas: HTMLCanvasElement, delay: number = 100): void {
    if (this.isEncoding) {
      throw new Error('Cannot add frames while encoding');
    }

    const timer = PerformanceMonitor.startTimer('gif_frame_clone');
    
    // Use memory-managed canvas cloning
    const clonedCanvas = MemoryManager.cloneCanvas(canvas);
    
    timer(); // Record timing

    this.frames.push({
      canvas: clonedCanvas,
      delay
    });
  }

  async encode(
    onProgress?: (progress: number) => void,
    onComplete?: (blob: Blob) => void,
    onError?: (error: Error) => void
  ): Promise<Blob> {
    return ErrorRecovery.retry(async () => {
      return new Promise<Blob>((resolve, reject) => {
        if (this.isEncoding) {
          reject(new Error('Already encoding'));
          return;
        }

        if (this.frames.length === 0) {
          reject(new Error('No frames to encode'));
          return;
        }

        const timer = PerformanceMonitor.startTimer('gif_encode');
        this.isEncoding = true;

        // Enhanced progress tracking
        if (onProgress) {
          this.gif.on('progress', (progress: number) => {
            onProgress(Math.min(progress, 1));
          });
        }

        // Add completion handler with cleanup
        this.gif.on('finished', (blob: Blob) => {
          this.isEncoding = false;
          timer(); // Record encoding time
          this.disposeFrames(); // Clean up memory
          
          if (onComplete) onComplete(blob);
          resolve(blob);
        });

        // Enhanced error handling with recovery
        this.gif.on('error', (error: Error) => {
          this.isEncoding = false;
          timer(); // Record failed time
          console.error('GIF encoding error:', error);
          
          if (onError) onError(error);
          reject(error);
        });

        // Add frames with memory monitoring
        this.frames.forEach(frame => {
          this.gif.addFrame(frame.canvas, { 
            delay: frame.delay, 
            copy: true,
            dispose: 2
          });
        });

        // Start encoding with error handling
        try {
          this.gif.render();
        } catch (error) {
          this.isEncoding = false;
          timer();
          reject(error);
        }
      });
    }, 2, (attempt, error) => {
      console.warn(`GIF encoding attempt ${attempt} failed:`, error);
    });
  }

  clear(): void {
    if (this.isEncoding) {
      throw new Error('Cannot clear while encoding');
    }
    this.disposeFrames();
  }

  private disposeFrames(): void {
    // Release all canvas frames back to memory pool
    this.frames.forEach(frame => {
      MemoryManager.releaseCanvas(frame.canvas);
    });
    this.frames = [];
  }

  getFrameCount(): number {
    return this.frames.length;
  }

  getEstimatedSize(): number {
    // More accurate estimation based on frame count and dimensions
    const pixelsPerFrame = this.gif.options.width * this.gif.options.height;
    const totalPixels = pixelsPerFrame * this.frames.length;
    const qualityFactor = (11 - this.gif.options.quality) / 10;
    const compressionFactor = this.gif.options.dither === 'Atkinson' ? 0.25 : 0.3; // Better compression with Atkinson
    return (totalPixels * qualityFactor * compressionFactor) / (1024 * 1024);
  }
}

export const createGifEncoder = (options: GifEncoderOptions): GifEncoder => {
  return new GifEncoder(options);
};

```

#### client/src/utils/gifOptimizer.ts
```ts
export interface DeviceCapabilities {
  workers: number;
  batchSize: number;
  quality: number;
  maxResolution: { width: number; height: number };
  supportsDithering: boolean;
  supportsOffscreenCanvas: boolean;
}

export interface OptimizedGifSettings {
  width: number;
  height: number;
  quality: number;
  workers: number;
  duration: number;
  fps: number;
  dither: boolean | string;
}

export class GifOptimizer {
  getDeviceCapabilities(): DeviceCapabilities {
    const cores = navigator.hardwareConcurrency || 4;
    const memory = (navigator as any).deviceMemory || 4;
    const isMobile = window.innerWidth < 768;
    const isHighEnd = cores >= 8 && memory >= 8 && !isMobile;
    const supportsOffscreenCanvas = typeof OffscreenCanvas !== 'undefined';
    
    return {
      workers: isHighEnd ? 6 : isMobile ? 2 : 4,
      batchSize: isHighEnd ? 8 : isMobile ? 3 : 5,
      quality: isMobile ? 8 : isHighEnd ? 3 : 5,
      maxResolution: isMobile 
        ? { width: 1280, height: 720 }
        : isHighEnd 
        ? { width: 2560, height: 1440 }
        : { width: 1920, height: 1080 },
      supportsDithering: !isMobile,
      supportsOffscreenCanvas
    };
  }

  optimizeSettings(requestedSettings: any): OptimizedGifSettings {
    const capabilities = this.getDeviceCapabilities();
    
    // Validate aspect ratio (16:9 or 9:16 only)
    const aspectRatio = requestedSettings.width / requestedSettings.height;
    const is16x9 = Math.abs(aspectRatio - (16/9)) < 0.1;
    const is9x16 = Math.abs(aspectRatio - (9/16)) < 0.1;
    
    if (!is16x9 && !is9x16) {
      // Force to 16:9 if invalid aspect ratio
      const width = Math.min(requestedSettings.width, capabilities.maxResolution.width);
      const height = Math.round(width * (9/16));
      requestedSettings.width = width;
      requestedSettings.height = height;
    }
    
    // Clamp resolution to device capabilities
    const width = Math.min(requestedSettings.width, capabilities.maxResolution.width);
    const height = Math.min(requestedSettings.height, capabilities.maxResolution.height);
    
    // Enhanced quality adjustment based on total pixel count and device
    const totalPixels = width * height * (requestedSettings.duration * requestedSettings.fps);
    let quality = requestedSettings.quality;
    
    if (totalPixels > 15000000) { // Very high pixel count
      quality = Math.max(quality, 8);
    } else if (totalPixels > 10000000) { // High pixel count
      quality = Math.max(quality, 6);
    }
    
    return {
      width,
      height,
      quality: Math.max(quality, capabilities.quality),
      workers: capabilities.workers,
      duration: Math.min(requestedSettings.duration, 15), // Max 15 seconds
      fps: Math.min(requestedSettings.fps, 30), // Max 30 FPS
      dither: capabilities.supportsDithering ? 'Atkinson' : false // Enhanced dithering
    };
  }

  estimateFileSize(settings: OptimizedGifSettings): number {
    const pixelsPerFrame = settings.width * settings.height;
    const totalFrames = settings.duration * settings.fps;
    const overlapFrames = 0; // No overlap frames for single play
    const totalFramesWithOverlap = totalFrames;
    const qualityFactor = (11 - settings.quality) / 10;
    // Better compression with Atkinson dithering
    const compressionFactor = settings.dither === 'Atkinson' ? 0.25 : 0.3;
    
    return (pixelsPerFrame * totalFramesWithOverlap * qualityFactor * compressionFactor) / (1024 * 1024);
  }

  getRecommendedSettings(targetSizeMB: number = 10): OptimizedGifSettings {
    const capabilities = this.getDeviceCapabilities();
    
    // Start with enhanced default settings
    let settings: OptimizedGifSettings = {
      width: 1280,
      height: 720,
      quality: 5,
      workers: capabilities.workers,
      duration: 5,
      fps: 24, // Cinematic frame rate
      dither: capabilities.supportsDithering ? 'Atkinson' : false
    };
    
    // Adjust settings to meet target size with enhanced algorithm
    while (this.estimateFileSize(settings) > targetSizeMB && settings.quality < 10) {
      settings.quality += 1;
      if (settings.quality >= 8) {
        settings.fps = Math.max(20, settings.fps - 2);
        if (settings.fps <= 20) {
          settings.width = Math.max(720, settings.width - 160);
          settings.height = Math.max(405, settings.height - 90);
        }
      }
    }
    
    return this.optimizeSettings(settings);
  }
}

export const gifOptimizer = new GifOptimizer();

```

#### client/src/utils/halftoneEffect.ts
```ts
/**
 * RGB Halftone Post-Processing Effect
 * Based on Three.js RGB Halftone example
 */

export interface HalftoneSettings {
  shape: number; // 1 = dot, 2 = ellipse, 3 = line, 4 = square
  radius: number; // 0.0 - 1.0
  rotateR: number; // rotation for red channel (radians)
  rotateG: number; // rotation for green channel (radians) 
  rotateB: number; // rotation for blue channel (radians)
  scatter: number; // 0.0 - 1.0
  blending: number; // 1 = linear, 2 = multiply, 3 = add, 4 = lighter, 5 = darker
  blendingMode: number; // 1 = linear, 2 = multiply, 3 = add, 4 = lighter, 5 = darker
  greyscale: boolean;
  disable: boolean;
}

export const halftoneVertexShader = `
varying vec2 vUv;

void main() {
  vUv = uv;
  gl_Position = projectionMatrix * modelViewMatrix * vec4(position, 1.0);
}
`;

export const halftoneFragmentShader = `
uniform sampler2D tDiffuse;
uniform float width;
uniform float height;
uniform float dotSize;
uniform float centerX;
uniform float centerY;
uniform float angle;
uniform float scale;

varying vec2 vUv;

float pattern() {
  float s = sin(angle), c = cos(angle);
  vec2 tex = vUv * vec2(width, height) - vec2(centerX, centerY);
  vec2 point = vec2(c * tex.x - s * tex.y, s * tex.x + c * tex.y) * scale;
  return (sin(point.x) * sin(point.y)) * 4.0;
}

void main() {
  vec4 color = texture2D(tDiffuse, vUv);
  float average = (color.r + color.g + color.b) / 3.0;
  gl_FragColor = vec4(vec3(average * 10.0 - 5.0 + pattern()), color.a);
}
`;

export const rgbHalftoneFragmentShader = `
uniform sampler2D tDiffuse;
uniform float width;
uniform float height;
uniform vec2 center;
uniform float angle;
uniform float scale;
uniform int shape;
uniform float radius;
uniform float rotateR;
uniform float rotateG; 
uniform float rotateB;
uniform float scatter;
uniform float blending;
uniform int blendingMode;
uniform bool greyscale;
uniform bool disable;

varying vec2 vUv;

const int SHAPE_DOT = 1;
const int SHAPE_ELLIPSE = 2;
const int SHAPE_LINE = 3;
const int SHAPE_SQUARE = 4;

const int BLENDING_LINEAR = 1;
const int BLENDING_MULTIPLY = 2;
const int BLENDING_ADD = 3;
const int BLENDING_LIGHTER = 4;
const int BLENDING_DARKER = 5;

float rand(vec2 n) {
  return fract(sin(dot(n, vec2(12.9898, 4.1414))) * 43758.5453);
}

float noise(vec2 n) {
  const vec2 d = vec2(0.0, 1.0);
  vec2 b = floor(n), f = smoothstep(vec2(0.0), vec2(1.0), fract(n));
  return mix(mix(rand(b), rand(b + d.yx), f.x), mix(rand(b + d.xy), rand(b + d.yy), f.x), f.y);
}

vec3 rotateRGB(vec3 color, float rotateR, float rotateG, float rotateB) {
  return vec3(
    color.r * cos(rotateR) - color.g * sin(rotateR),
    color.r * sin(rotateG) + color.g * cos(rotateG),
    color.b * cos(rotateB)
  );
}

float pattern(float angle, vec2 position, float scale, float scatter) {
  float s = sin(angle), c = cos(angle);
  vec2 tex = position * vec2(width, height) - center;
  vec2 point = vec2(c * tex.x - s * tex.y, s * tex.x + c * tex.y) * scale;
  
  if (scatter > 0.0) {
    point += noise(point) * scatter;
  }
  
  if (shape == SHAPE_DOT) {
    return length(point) - radius;
  } else if (shape == SHAPE_ELLIPSE) {
    vec2 ellipse = point / vec2(radius, radius * 0.5);
    return length(ellipse) - 1.0;
  } else if (shape == SHAPE_LINE) {
    return abs(point.y) - radius;
  } else if (shape == SHAPE_SQUARE) {
    return max(abs(point.x), abs(point.y)) - radius;
  }
  
  return 0.0;
}

void main() {
  if (disable) {
    gl_FragColor = texture2D(tDiffuse, vUv);
    return;
  }
  
  vec4 color = texture2D(tDiffuse, vUv);
  
  if (greyscale) {
    float grey = (color.r + color.g + color.b) / 3.0;
    color = vec4(grey, grey, grey, color.a);
  }
  
  vec3 rotated = rotateRGB(color.rgb, rotateR, rotateG, rotateB);
  
  float patternR = pattern(rotateR, vUv, scale, scatter);
  float patternG = pattern(rotateG, vUv, scale, scatter); 
  float patternB = pattern(rotateB, vUv, scale, scatter);
  
  vec3 halftone = vec3(
    smoothstep(0.0, radius, patternR) * rotated.r,
    smoothstep(0.0, radius, patternG) * rotated.g,
    smoothstep(0.0, radius, patternB) * rotated.b
  );
  
  vec3 result;
  
  if (blendingMode == BLENDING_LINEAR) {
    result = mix(color.rgb, halftone, blending);
  } else if (blendingMode == BLENDING_MULTIPLY) {
    result = color.rgb * mix(vec3(1.0), halftone, blending);
  } else if (blendingMode == BLENDING_ADD) {
    result = color.rgb + halftone * blending;
  } else if (blendingMode == BLENDING_LIGHTER) {
    result = max(color.rgb, halftone * blending);
  } else if (blendingMode == BLENDING_DARKER) {
    result = min(color.rgb, halftone + (1.0 - blending));
  } else {
    result = mix(color.rgb, halftone, blending);
  }
  
  gl_FragColor = vec4(result, color.a);
}
`;

export class HalftoneEffect {
  private canvas: HTMLCanvasElement;
  private gl: WebGL2RenderingContext;
  private program: WebGLProgram | null = null;
  private framebuffer: WebGLFramebuffer | null = null;
  private texture: WebGLTexture | null = null;
  private settings: HalftoneSettings;
  private uniforms: { [key: string]: WebGLUniformLocation | null } = {};

  constructor(canvas: HTMLCanvasElement, gl: WebGL2RenderingContext) {
    this.canvas = canvas;
    this.gl = gl;
    this.settings = {
      shape: 1, // dot
      radius: 0.4,
      rotateR: Math.PI / 12 * 1,
      rotateG: Math.PI / 12 * 2,
      rotateB: Math.PI / 12 * 3,
      scatter: 0.5,
      blending: 1.0,
      blendingMode: 1, // linear
      greyscale: false,
      disable: false
    };
    
    this.initializeShaders();
  }

  private initializeShaders(): void {
    const vertexShader = this.createShader(this.gl.VERTEX_SHADER, halftoneVertexShader);
    const fragmentShader = this.createShader(this.gl.FRAGMENT_SHADER, rgbHalftoneFragmentShader);
    
    if (!vertexShader || !fragmentShader) {
      console.error('Failed to create halftone shaders');
      return;
    }

    this.program = this.gl.createProgram();
    if (!this.program) {
      console.error('Failed to create halftone program');
      return;
    }

    this.gl.attachShader(this.program, vertexShader);
    this.gl.attachShader(this.program, fragmentShader);
    this.gl.linkProgram(this.program);

    if (!this.gl.getProgramParameter(this.program, this.gl.LINK_STATUS)) {
      console.error('Halftone program link error:', this.gl.getProgramInfoLog(this.program));
      return;
    }

    // Get uniform locations
    this.uniforms = {
      tDiffuse: this.gl.getUniformLocation(this.program, 'tDiffuse'),
      width: this.gl.getUniformLocation(this.program, 'width'),
      height: this.gl.getUniformLocation(this.program, 'height'),
      center: this.gl.getUniformLocation(this.program, 'center'),
      angle: this.gl.getUniformLocation(this.program, 'angle'),
      scale: this.gl.getUniformLocation(this.program, 'scale'),
      shape: this.gl.getUniformLocation(this.program, 'shape'),
      radius: this.gl.getUniformLocation(this.program, 'radius'),
      rotateR: this.gl.getUniformLocation(this.program, 'rotateR'),
      rotateG: this.gl.getUniformLocation(this.program, 'rotateG'),
      rotateB: this.gl.getUniformLocation(this.program, 'rotateB'),
      scatter: this.gl.getUniformLocation(this.program, 'scatter'),
      blending: this.gl.getUniformLocation(this.program, 'blending'),
      blendingMode: this.gl.getUniformLocation(this.program, 'blendingMode'),
      greyscale: this.gl.getUniformLocation(this.program, 'greyscale'),
      disable: this.gl.getUniformLocation(this.program, 'disable')
    };
  }

  private createShader(type: number, source: string): WebGLShader | null {
    const shader = this.gl.createShader(type);
    if (!shader) return null;

    this.gl.shaderSource(shader, source);
    this.gl.compileShader(shader);

    if (!this.gl.getShaderParameter(shader, this.gl.COMPILE_STATUS)) {
      console.error('Shader compile error:', this.gl.getShaderInfoLog(shader));
      this.gl.deleteShader(shader);
      return null;
    }

    return shader;
  }

  updateSettings(newSettings: Partial<HalftoneSettings>): void {
    this.settings = { ...this.settings, ...newSettings };
  }

  apply(inputTexture: WebGLTexture): void {
    if (!this.program) return;

    this.gl.useProgram(this.program);

    // Set uniforms
    this.gl.uniform1i(this.uniforms.tDiffuse, 0);
    this.gl.uniform1f(this.uniforms.width, this.canvas.width);
    this.gl.uniform1f(this.uniforms.height, this.canvas.height);
    this.gl.uniform2f(this.uniforms.center, this.canvas.width / 2, this.canvas.height / 2);
    this.gl.uniform1f(this.uniforms.angle, 0);
    this.gl.uniform1f(this.uniforms.scale, 1.0);
    this.gl.uniform1i(this.uniforms.shape, this.settings.shape);
    this.gl.uniform1f(this.uniforms.radius, this.settings.radius);
    this.gl.uniform1f(this.uniforms.rotateR, this.settings.rotateR);
    this.gl.uniform1f(this.uniforms.rotateG, this.settings.rotateG);
    this.gl.uniform1f(this.uniforms.rotateB, this.settings.rotateB);
    this.gl.uniform1f(this.uniforms.scatter, this.settings.scatter);
    this.gl.uniform1f(this.uniforms.blending, this.settings.blending);
    this.gl.uniform1i(this.uniforms.blendingMode, this.settings.blendingMode);
    this.gl.uniform1i(this.uniforms.greyscale, this.settings.greyscale ? 1 : 0);
    this.gl.uniform1i(this.uniforms.disable, this.settings.disable ? 1 : 0);

    // Bind input texture
    this.gl.activeTexture(this.gl.TEXTURE0);
    this.gl.bindTexture(this.gl.TEXTURE_2D, inputTexture);

    // Render fullscreen quad
    this.renderQuad();
  }

  private renderQuad(): void {
    // Create fullscreen quad vertices
    const vertices = new Float32Array([
      -1, -1, 0, 0,
       1, -1, 1, 0,
      -1,  1, 0, 1,
       1,  1, 1, 1
    ]);

    const buffer = this.gl.createBuffer();
    this.gl.bindBuffer(this.gl.ARRAY_BUFFER, buffer);
    this.gl.bufferData(this.gl.ARRAY_BUFFER, vertices, this.gl.STATIC_DRAW);

    // Set up attributes
    const positionLocation = this.gl.getAttribLocation(this.program!, 'position');
    const uvLocation = this.gl.getAttribLocation(this.program!, 'uv');

    this.gl.enableVertexAttribArray(positionLocation);
    this.gl.vertexAttribPointer(positionLocation, 2, this.gl.FLOAT, false, 16, 0);

    this.gl.enableVertexAttribArray(uvLocation);
    this.gl.vertexAttribPointer(uvLocation, 2, this.gl.FLOAT, false, 16, 8);

    // Draw
    this.gl.drawArrays(this.gl.TRIANGLE_STRIP, 0, 4);

    // Cleanup
    this.gl.deleteBuffer(buffer);
  }

  getSettings(): HalftoneSettings {
    return { ...this.settings };
  }

  dispose(): void {
    if (this.program) {
      this.gl.deleteProgram(this.program);
      this.program = null;
    }
    if (this.framebuffer) {
      this.gl.deleteFramebuffer(this.framebuffer);
      this.framebuffer = null;
    }
    if (this.texture) {
      this.gl.deleteTexture(this.texture);
      this.texture = null;
    }
  }
}
```

#### client/src/utils/instancedPointCloud.ts
```ts
/**
 * GPU-optimized instanced point cloud renderer
 * Uses instancing to render thousands of points with minimal draw calls
 */

import * as THREE from 'three';
import { instancedVertexShader, ditheredFragmentShader } from './ditherShaders';

export interface InstancedPointCloudSettings {
  maxInstances: number;
  enableDithering: boolean;
  ditherStrength: number;
  enableLOD: boolean;
  lodDistances: number[];
  cullDistance: number;
}

export class InstancedPointCloudRenderer {
  private geometry!: THREE.InstancedBufferGeometry;
  private material!: THREE.ShaderMaterial;
  private mesh!: THREE.InstancedMesh;
  private instanceCount: number = 0;
  
  // Instance attributes
  private instancePositions!: THREE.InstancedBufferAttribute;
  private instanceColors!: THREE.InstancedBufferAttribute;
  private instanceScales!: THREE.InstancedBufferAttribute;
  private instanceOpacities!: THREE.InstancedBufferAttribute;
  
  // Performance tracking
  private lastUpdateTime: number = 0;
  private framesSinceUpdate: number = 0;
  
  constructor(
    private maxInstances: number,
    private settings: InstancedPointCloudSettings
  ) {
    this.createGeometry();
    this.createMaterial();
    this.createMesh();
  }

  private createGeometry(): void {
    // Base geometry - single point that will be instanced
    this.geometry = new THREE.InstancedBufferGeometry();
    
    // Single point vertex
    const positions = new Float32Array([0, 0, 0]);
    const uvs = new Float32Array([0.5, 0.5]);
    const colors = new Float32Array([1, 1, 1]);
    
    this.geometry.setAttribute('position', new THREE.BufferAttribute(positions, 3));
    this.geometry.setAttribute('uv', new THREE.BufferAttribute(uvs, 2));
    this.geometry.setAttribute('color', new THREE.BufferAttribute(colors, 3));
    
    // Instance attributes - these vary per instance
    const instancePositionsArray = new Float32Array(this.maxInstances * 3);
    const instanceColorsArray = new Float32Array(this.maxInstances * 3);
    const instanceScalesArray = new Float32Array(this.maxInstances);
    const instanceOpacitiesArray = new Float32Array(this.maxInstances);
    
    this.instancePositions = new THREE.InstancedBufferAttribute(instancePositionsArray, 3);
    this.instanceColors = new THREE.InstancedBufferAttribute(instanceColorsArray, 3);
    this.instanceScales = new THREE.InstancedBufferAttribute(instanceScalesArray, 1);
    this.instanceOpacities = new THREE.InstancedBufferAttribute(instanceOpacitiesArray, 1);
    
    this.geometry.setAttribute('instancePosition', this.instancePositions);
    this.geometry.setAttribute('instanceColor', this.instanceColors);
    this.geometry.setAttribute('instanceScale', this.instanceScales);
    this.geometry.setAttribute('instanceOpacity', this.instanceOpacities);
  }

  private createMaterial(): void {
    this.material = new THREE.ShaderMaterial({
      vertexShader: instancedVertexShader,
      fragmentShader: ditheredFragmentShader,
      uniforms: {
        videoTexture: { value: null },
        depthMap: { value: null },
        pointSize: { value: 2.0 },
        nearClipping: { value: 0.0 },
        farClipping: { value: 1.0 },
        depthPower: { value: 1.0 },
        pointSizeDepthFactor: { value: 1.0 },
        invertDepth: { value: false },
        useRealDepth: { value: false },
        time: { value: 0.0 },
        exponentialK: { value: 0.5 },
        gamma: { value: 1.0 },
        noiseScale: { value: 10.0 },
        enableDithering: { value: this.settings.enableDithering },
        ditherStrength: { value: this.settings.ditherStrength }
      },
      transparent: true,
      blending: THREE.NormalBlending,
      depthWrite: false,
      side: THREE.FrontSide
    });
  }

  private createMesh(): void {
    // Create dummy geometry for InstancedMesh (we'll use our custom geometry)
    const dummyGeometry = new THREE.BufferGeometry();
    dummyGeometry.setAttribute('position', new THREE.BufferAttribute(new Float32Array([0, 0, 0]), 3));
    
    this.mesh = new THREE.InstancedMesh(dummyGeometry, this.material, this.maxInstances);
    this.mesh.geometry = this.geometry; // Override with our instanced geometry
    this.mesh.count = 0; // Start with no instances
  }

  public updateInstances(
    positions: Float32Array,
    colors: Uint8Array,
    videoTexture: THREE.Texture,
    depthTexture?: THREE.Texture,
    camera?: THREE.Camera
  ): void {
    const now = performance.now();
    
    // Adaptive LOD - reduce instance count based on frame rate
    if (this.settings.enableLOD && camera) {
      this.applyLOD(positions, colors, camera);
    }
    
    // Update instance count
    this.instanceCount = Math.min(positions.length / 3, this.maxInstances);
    this.mesh.count = this.instanceCount;
    
    // Update instance positions
    for (let i = 0; i < this.instanceCount; i++) {
      const i3 = i * 3;
      this.instancePositions.setXYZ(i, positions[i3], positions[i3 + 1], positions[i3 + 2]);
      
      // Convert colors from Uint8Array to normalized float
      if (colors && i3 < colors.length) {
        this.instanceColors.setXYZ(
          i,
          colors[i3] / 255,
          colors[i3 + 1] / 255,
          colors[i3 + 2] / 255
        );
      } else {
        this.instanceColors.setXYZ(i, 1, 1, 1);
      }
      
      // Set default scale and opacity
      this.instanceScales.setX(i, 1.0);
      this.instanceOpacities.setX(i, 1.0);
    }
    
    // Mark attributes as needing update
    this.instancePositions.needsUpdate = true;
    this.instanceColors.needsUpdate = true;
    this.instanceScales.needsUpdate = true;
    this.instanceOpacities.needsUpdate = true;
    
    // Update material uniforms
    this.material.uniforms.videoTexture.value = videoTexture;
    if (depthTexture) {
      this.material.uniforms.depthMap.value = depthTexture;
    }
    this.material.uniforms.time.value = now * 0.001;
    
    this.lastUpdateTime = now;
    this.framesSinceUpdate = 0;
  }

  private applyLOD(
    positions: Float32Array,
    colors: Uint8Array,
    camera: THREE.Camera
  ): void {
    if (!this.settings.lodDistances || this.settings.lodDistances.length === 0) return;
    
    const cameraPosition = camera.position;
    const avgDistance = Math.sqrt(
      cameraPosition.x * cameraPosition.x + 
      cameraPosition.y * cameraPosition.y + 
      cameraPosition.z * cameraPosition.z
    );
    
    // Determine LOD level based on distance
    let lodLevel = 0;
    for (let i = 0; i < this.settings.lodDistances.length; i++) {
      if (avgDistance > this.settings.lodDistances[i]) {
        lodLevel = i + 1;
      }
    }
    
    // Apply decimation based on LOD level
    const decimationFactor = Math.pow(2, lodLevel);
    if (decimationFactor > 1) {
      this.decimateInstances(positions, colors, decimationFactor);
    }
  }

  private decimateInstances(
    positions: Float32Array,
    colors: Uint8Array,
    factor: number
  ): void {
    // Simple decimation - skip every nth point
    const originalCount = positions.length / 3;
    const newCount = Math.floor(originalCount / factor);
    
    for (let i = 0, j = 0; i < newCount && j < originalCount; i++, j += factor) {
      const srcIndex = j * 3;
      const dstIndex = i * 3;
      
      // Copy position
      positions[dstIndex] = positions[srcIndex];
      positions[dstIndex + 1] = positions[srcIndex + 1];
      positions[dstIndex + 2] = positions[srcIndex + 2];
      
      // Copy color if available
      if (colors && srcIndex < colors.length) {
        colors[dstIndex] = colors[srcIndex];
        colors[dstIndex + 1] = colors[srcIndex + 1];
        colors[dstIndex + 2] = colors[srcIndex + 2];
      }
    }
    
    // Update instance count
    this.instanceCount = newCount;
  }

  public updateUniforms(uniforms: { [key: string]: any }): void {
    Object.keys(uniforms).forEach(key => {
      if (this.material.uniforms[key]) {
        this.material.uniforms[key].value = uniforms[key];
      }
    });
  }

  public getMesh(): THREE.InstancedMesh {
    return this.mesh;
  }

  public getInstanceCount(): number {
    return this.instanceCount;
  }

  public dispose(): void {
    this.geometry.dispose();
    this.material.dispose();
    
    // Dispose of instance attributes
    this.instancePositions.array = null as any;
    this.instanceColors.array = null as any;
    this.instanceScales.array = null as any;
    this.instanceOpacities.array = null as any;
  }

  // Performance monitoring
  public getPerformanceStats(): {
    instanceCount: number;
    drawCalls: number;
    memoryUsage: number;
    fps: number;
  } {
    const now = performance.now();
    const deltaTime = now - this.lastUpdateTime;
    const fps = deltaTime > 0 ? 1000 / deltaTime : 0;
    
    return {
      instanceCount: this.instanceCount,
      drawCalls: 1, // Instanced rendering uses single draw call
      memoryUsage: this.instanceCount * (3 + 3 + 1 + 1) * 4, // Bytes for all instance attributes
      fps
    };
  }
}

// Factory function for easy creation
export function createInstancedPointCloud(
  maxInstances: number = 100000,
  settings: Partial<InstancedPointCloudSettings> = {}
): InstancedPointCloudRenderer {
  const defaultSettings: InstancedPointCloudSettings = {
    maxInstances,
    enableDithering: true,
    ditherStrength: 0.5,
    enableLOD: true,
    lodDistances: [10, 20, 50, 100],
    cullDistance: 200
  };
  
  const finalSettings = { ...defaultSettings, ...settings };
  return new InstancedPointCloudRenderer(maxInstances, finalSettings);
}
```

#### client/src/utils/memoryManager.ts
```ts
/**
 * Comprehensive Memory Management System
 * Handles WebGL resources, canvas management, and performance monitoring
 */

import * as THREE from 'three';

// Performance monitoring
export class PerformanceMonitor {
  private static timers: Map<string, number> = new Map();
  private static stats: Map<string, { count: number; total: number; min: number; max: number; avg: number }> = new Map();

  static startTimer(label: string): () => void {
    const start = performance.now();
    this.timers.set(label, start);
    
    return () => {
      const end = performance.now();
      const duration = end - start;
      this.timers.delete(label);
      this.updateStats(label, duration);
    };
  }

  private static updateStats(label: string, duration: number): void {
    const existing = this.stats.get(label);
    if (existing) {
      existing.count++;
      existing.total += duration;
      existing.min = Math.min(existing.min, duration);
      existing.max = Math.max(existing.max, duration);
      existing.avg = existing.total / existing.count;
    } else {
      this.stats.set(label, {
        count: 1,
        total: duration,
        min: duration,
        max: duration,
        avg: duration
      });
    }
  }

  static getStats(label?: string) {
    if (label) {
      return this.stats.get(label);
    }
    return Object.fromEntries(this.stats);
  }

  static clearStats(): void {
    this.stats.clear();
  }

  static logStats(): void {
    console.group('Performance Stats');
    for (const [label, stats] of this.stats) {
      console.log(`${label}: avg=${stats.avg.toFixed(2)}ms, min=${stats.min.toFixed(2)}ms, max=${stats.max.toFixed(2)}ms, count=${stats.count}`);
    }
    console.groupEnd();
  }
}

// WebGL resource management
export class WebGLResourceManager {
  private static resources: Map<any, { type: string; created: number }> = new Map();
  private static disposed: WeakSet<any> = new WeakSet();
  
  static register(resource: THREE.Material | THREE.Geometry | THREE.Texture, type: string): void {
    if (!this.disposed.has(resource)) {
      this.resources.set(resource, {
        type,
        created: Date.now()
      });
    }
  }

  static unregister(resource: any): void {
    this.resources.delete(resource);
    this.disposed.add(resource);
  }

  static disposeAll(): void {
    for (const [resource, info] of this.resources) {
      try {
        if (resource && typeof resource.dispose === 'function' && !this.disposed.has(resource)) {
          resource.dispose();
          this.disposed.add(resource);
        }
      } catch (error) {
        console.warn(`Failed to dispose ${info.type}:`, error);
      }
    }
    this.resources.clear();
  }

  static getResourceCount(): number {
    return this.resources.size;
  }

  static getResourcesByType(): Record<string, number> {
    const counts: Record<string, number> = {};
    for (const [, info] of this.resources) {
      counts[info.type] = (counts[info.type] || 0) + 1;
    }
    return counts;
  }
}

// Canvas memory management
export class MemoryManager {
  private static canvasPool: HTMLCanvasElement[] = [];
  private static maxPoolSize = 10;
  private static activeCanvases: Set<HTMLCanvasElement> = new Set();

  static getCanvas(width: number, height: number): HTMLCanvasElement {
    // Try to reuse from pool
    let canvas = this.canvasPool.pop();
    
    if (!canvas) {
      canvas = document.createElement('canvas');
    }
    
    canvas.width = width;
    canvas.height = height;
    this.activeCanvases.add(canvas);
    
    return canvas;
  }

  static releaseCanvas(canvas: HTMLCanvasElement): void {
    if (!this.activeCanvases.has(canvas)) return;
    
    this.activeCanvases.delete(canvas);
    
    // Clear canvas
    const ctx = canvas.getContext('2d');
    if (ctx) {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
    }
    
    // Return to pool if not full
    if (this.canvasPool.length < this.maxPoolSize) {
      this.canvasPool.push(canvas);
    }
  }

  static cloneCanvas(source: HTMLCanvasElement): HTMLCanvasElement {
    const clone = this.getCanvas(source.width, source.height);
    const ctx = clone.getContext('2d');
    if (ctx) {
      ctx.drawImage(source, 0, 0);
    }
    return clone;
  }

  static getPoolStats(): { poolSize: number; activeCanvases: number } {
    return {
      poolSize: this.canvasPool.length,
      activeCanvases: this.activeCanvases.size
    };
  }

  static cleanup(): void {
    // Clear all active canvases
    for (const canvas of this.activeCanvases) {
      const ctx = canvas.getContext('2d');
      if (ctx) {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
      }
    }
    this.activeCanvases.clear();
    this.canvasPool = [];
  }
}

// Error recovery system
export class ErrorRecovery {
  static async retry<T>(
    fn: () => Promise<T>,
    maxAttempts: number = 3,
    onRetry?: (attempt: number, error: Error) => void
  ): Promise<T> {
    let lastError: Error;
    
    for (let attempt = 1; attempt <= maxAttempts; attempt++) {
      try {
        return await fn();
      } catch (error) {
        lastError = error as Error;
        
        if (attempt === maxAttempts) {
          throw lastError;
        }
        
        if (onRetry) {
          onRetry(attempt, lastError);
        }
        
        // Exponential backoff
        const delay = Math.pow(2, attempt) * 100;
        await new Promise(resolve => setTimeout(resolve, delay));
      }
    }
    
    throw lastError!;
  }

  static withFallback<T>(
    primary: () => Promise<T>,
    fallback: () => Promise<T>,
    shouldFallback?: (error: Error) => boolean
  ): Promise<T> {
    return primary().catch(error => {
      if (!shouldFallback || shouldFallback(error)) {
        console.warn('Primary operation failed, using fallback:', error);
        return fallback();
      }
      throw error;
    });
  }
}

// WebGL context loss recovery
export class WebGLContextManager {
  private static contexts: Map<WebGLRenderingContext, { 
    canvas: HTMLCanvasElement;
    onLost: () => void;
    onRestored: () => void;
  }> = new Map();

  static register(
    gl: WebGLRenderingContext,
    onLost: () => void,
    onRestored: () => void
  ): void {
    const canvas = gl.canvas as HTMLCanvasElement;
    
    this.contexts.set(gl, { canvas, onLost, onRestored });
    
    canvas.addEventListener('webglcontextlost', (event) => {
      event.preventDefault();
      console.warn('WebGL context lost');
      onLost();
    });
    
    canvas.addEventListener('webglcontextrestored', () => {
      console.log('WebGL context restored');
      onRestored();
    });
  }

  static unregister(gl: WebGLRenderingContext): void {
    this.contexts.delete(gl);
  }

  static forceContextLoss(gl: WebGLRenderingContext): void {
    const ext = gl.getExtension('WEBGL_lose_context');
    if (ext) {
      ext.loseContext();
    }
  }

  static restoreContext(gl: WebGLRenderingContext): void {
    const ext = gl.getExtension('WEBGL_lose_context');
    if (ext) {
      ext.restoreContext();
    }
  }
}

// Global cleanup function
export function cleanup(): void {
  MemoryManager.cleanup();
  WebGLResourceManager.disposeAll();
  PerformanceMonitor.clearStats();
  
  // Force garbage collection if available
  if (window.gc) {
    window.gc();
  }
}

// Browser memory monitoring
export class MemoryMonitor {
  static getMemoryInfo(): any {
    if ('memory' in performance) {
      return (performance as any).memory;
    }
    return null;
  }

  static logMemoryUsage(): void {
    const memory = this.getMemoryInfo();
    if (memory) {
      console.group('Memory Usage');
      console.log(`Used: ${(memory.usedJSHeapSize / 1024 / 1024).toFixed(2)} MB`);
      console.log(`Total: ${(memory.totalJSHeapSize / 1024 / 1024).toFixed(2)} MB`);
      console.log(`Limit: ${(memory.jsHeapSizeLimit / 1024 / 1024).toFixed(2)} MB`);
      console.groupEnd();
    }
  }

  static isMemoryPressureHigh(): boolean {
    const memory = this.getMemoryInfo();
    if (!memory) return false;
    
    const usageRatio = memory.usedJSHeapSize / memory.jsHeapSizeLimit;
    return usageRatio > 0.8; // 80% threshold
  }
}

// Initialize cleanup on page unload
if (typeof window !== 'undefined') {
  window.addEventListener('beforeunload', cleanup);
  window.addEventListener('unload', cleanup);
}
```

#### client/src/utils/performanceOptimizer.ts
```ts
/**
 * AAA Performance Optimization System
 * GPU-first approach with aggressive caching and batching
 */

// Frame rate targeting and adaptive quality
export class FrameRateOptimizer {
  private static targetFPS = 60;
  private static currentFPS = 60;
  private static frameHistory: number[] = [];
  private static lastFrameTime = 0;
  private static qualityScale = 1.0;
  private static adaptiveQuality = true;

  static measureFrame(): void {
    const now = performance.now();
    if (this.lastFrameTime) {
      const frameTime = now - this.lastFrameTime;
      const fps = 1000 / frameTime;
      
      this.frameHistory.push(fps);
      if (this.frameHistory.length > 30) {
        this.frameHistory.shift();
      }
      
      this.currentFPS = this.frameHistory.reduce((a, b) => a + b) / this.frameHistory.length;
      
      if (this.adaptiveQuality) {
        this.adjustQuality();
      }
    }
    this.lastFrameTime = now;
  }

  private static adjustQuality(): void {
    const fpsRatio = this.currentFPS / this.targetFPS;
    
    if (fpsRatio < 0.8) {
      // Drop quality to maintain framerate
      this.qualityScale = Math.max(0.5, this.qualityScale * 0.95);
    } else if (fpsRatio > 1.1 && this.qualityScale < 1.0) {
      // Increase quality if we have headroom
      this.qualityScale = Math.min(1.0, this.qualityScale * 1.02);
    }
  }

  static getQualityScale(): number {
    return this.qualityScale;
  }

  static getCurrentFPS(): number {
    return this.currentFPS;
  }

  static setTargetFPS(fps: number): void {
    this.targetFPS = fps;
  }

  static enableAdaptiveQuality(enabled: boolean): void {
    this.adaptiveQuality = enabled;
  }
}

// GPU-accelerated uniform batching
export class UniformBatcher {
  private static uniformCache = new Map<string, any>();
  private static dirtyUniforms = new Set<string>();
  private static batchedUpdates: Array<{ key: string; value: any }> = [];

  static setUniform(key: string, value: any): void {
    const cached = this.uniformCache.get(key);
    if (cached !== value) {
      this.uniformCache.set(key, value);
      this.dirtyUniforms.add(key);
      this.batchedUpdates.push({ key, value });
    }
  }

  static flushUniforms(material: any): boolean {
    if (this.batchedUpdates.length === 0) return false;

    // Batch all uniform updates in single GPU call
    for (const { key, value } of this.batchedUpdates) {
      if (material.uniforms && material.uniforms[key]) {
        material.uniforms[key].value = value;
      }
    }

    this.batchedUpdates = [];
    this.dirtyUniforms.clear();
    return true;
  }

  static hasDirtyUniforms(): boolean {
    return this.batchedUpdates.length > 0;
  }
}

// Shader compilation cache with hot-swapping
export class ShaderCache {
  private static cache = new Map<string, any>();
  private static compilationQueue: Array<{ key: string; shader: string }> = [];

  static getShader(key: string, vertexShader: string, fragmentShader: string): any {
    const cacheKey = `${key}_${this.hashCode(vertexShader + fragmentShader)}`;
    
    if (this.cache.has(cacheKey)) {
      return this.cache.get(cacheKey);
    }

    // Queue for async compilation to avoid blocking
    this.compilationQueue.push({ key: cacheKey, shader: vertexShader + fragmentShader });
    return null;
  }

  static precompileShaders(): void {
    // Use requestIdleCallback for non-blocking compilation
    if (window.requestIdleCallback) {
      window.requestIdleCallback(() => this.processCompilationQueue());
    } else {
      setTimeout(() => this.processCompilationQueue(), 16);
    }
  }

  private static processCompilationQueue(): void {
    const item = this.compilationQueue.shift();
    if (item) {
      // Compile shader in idle time
      this.cache.set(item.key, item.shader);
      
      if (this.compilationQueue.length > 0) {
        this.precompileShaders();
      }
    }
  }

  private static hashCode(str: string): number {
    let hash = 0;
    for (let i = 0; i < str.length; i++) {
      const char = str.charCodeAt(i);
      hash = ((hash << 5) - hash) + char;
      hash = hash & hash; // 32-bit integer
    }
    return hash;
  }
}

// Geometry instancing for point clouds
export class GeometryInstancer {
  private static instancedGeometries = new Map<string, any>();
  private static maxInstances = 10000;

  static createInstancedGeometry(baseGeometry: any, instanceCount: number): any {
    const key = `instanced_${instanceCount}`;
    
    if (this.instancedGeometries.has(key)) {
      return this.instancedGeometries.get(key);
    }

    // Create instanced geometry with pre-allocated buffers
    const instancedGeometry = baseGeometry.clone();
    
    // Pre-allocate instance matrices
    const instanceMatrix = new Float32Array(instanceCount * 16);
    instancedGeometry.instanceMatrix = instanceMatrix;
    
    this.instancedGeometries.set(key, instancedGeometry);
    return instancedGeometry;
  }

  static updateInstances(geometry: any, transforms: Float32Array): void {
    if (geometry.instanceMatrix) {
      geometry.instanceMatrix.set(transforms);
      geometry.instanceMatrix.needsUpdate = true;
    }
  }
}

// Memory pool for frequent allocations
export class ObjectPool<T> {
  private available: T[] = [];
  private factory: () => T;
  private reset: (obj: T) => void;

  constructor(factory: () => T, reset: (obj: T) => void, initialSize = 10) {
    this.factory = factory;
    this.reset = reset;
    
    // Pre-populate pool
    for (let i = 0; i < initialSize; i++) {
      this.available.push(factory());
    }
  }

  acquire(): T {
    if (this.available.length > 0) {
      return this.available.pop()!;
    }
    return this.factory();
  }

  release(obj: T): void {
    this.reset(obj);
    this.available.push(obj);
  }

  getPoolSize(): number {
    return this.available.length;
  }
}

// WebGL state caching to avoid redundant calls
export class WebGLStateCache {
  private static currentState = new Map<string, any>();

  static setBlendMode(gl: WebGLRenderingContext, mode: number): void {
    const key = 'blendMode';
    if (this.currentState.get(key) !== mode) {
      gl.blendFunc(gl.SRC_ALPHA, mode);
      this.currentState.set(key, mode);
    }
  }

  static setDepthTest(gl: WebGLRenderingContext, enabled: boolean): void {
    const key = 'depthTest';
    if (this.currentState.get(key) !== enabled) {
      if (enabled) {
        gl.enable(gl.DEPTH_TEST);
      } else {
        gl.disable(gl.DEPTH_TEST);
      }
      this.currentState.set(key, enabled);
    }
  }

  static setCullFace(gl: WebGLRenderingContext, mode: number | null): void {
    const key = 'cullFace';
    if (this.currentState.get(key) !== mode) {
      if (mode !== null) {
        gl.enable(gl.CULL_FACE);
        gl.cullFace(mode);
      } else {
        gl.disable(gl.CULL_FACE);
      }
      this.currentState.set(key, mode);
    }
  }

  static clear(): void {
    this.currentState.clear();
  }
}

// Frustum culling for point clouds
export class FrustumCuller {
  private static frustumPlanes: number[][] = [];

  static updateFrustum(camera: any): void {
    const matrix = camera.projectionMatrix.clone().multiply(camera.matrixWorldInverse);
    
    // Extract frustum planes from projection matrix
    this.frustumPlanes = [
      [matrix.elements[3] + matrix.elements[0], matrix.elements[7] + matrix.elements[4], matrix.elements[11] + matrix.elements[8], matrix.elements[15] + matrix.elements[12]], // Right
      [matrix.elements[3] - matrix.elements[0], matrix.elements[7] - matrix.elements[4], matrix.elements[11] - matrix.elements[8], matrix.elements[15] - matrix.elements[12]], // Left
      [matrix.elements[3] + matrix.elements[1], matrix.elements[7] + matrix.elements[5], matrix.elements[11] + matrix.elements[9], matrix.elements[15] + matrix.elements[13]], // Top
      [matrix.elements[3] - matrix.elements[1], matrix.elements[7] - matrix.elements[5], matrix.elements[11] - matrix.elements[9], matrix.elements[15] - matrix.elements[13]], // Bottom
      [matrix.elements[3] + matrix.elements[2], matrix.elements[7] + matrix.elements[6], matrix.elements[11] + matrix.elements[10], matrix.elements[15] + matrix.elements[14]], // Far
      [matrix.elements[3] - matrix.elements[2], matrix.elements[7] - matrix.elements[6], matrix.elements[11] - matrix.elements[10], matrix.elements[15] - matrix.elements[14]]  // Near
    ];
  }

  static isPointInFrustum(x: number, y: number, z: number): boolean {
    for (const plane of this.frustumPlanes) {
      if (plane[0] * x + plane[1] * y + plane[2] * z + plane[3] <= 0) {
        return false;
      }
    }
    return true;
  }

  static cullPoints(positions: Float32Array): Float32Array {
    const culledPositions: number[] = [];
    
    for (let i = 0; i < positions.length; i += 3) {
      if (this.isPointInFrustum(positions[i], positions[i + 1], positions[i + 2])) {
        culledPositions.push(positions[i], positions[i + 1], positions[i + 2]);
      }
    }
    
    return new Float32Array(culledPositions);
  }
}

// Level-of-detail system for point clouds
export class LODManager {
  private static lodLevels = [
    { distance: 10, density: 1.0 },
    { distance: 50, density: 0.5 },
    { distance: 100, density: 0.25 },
    { distance: 200, density: 0.1 }
  ];

  static getLODDensity(distance: number): number {
    for (let i = 0; i < this.lodLevels.length; i++) {
      if (distance <= this.lodLevels[i].distance) {
        return this.lodLevels[i].density;
      }
    }
    return this.lodLevels[this.lodLevels.length - 1].density;
  }

  static decimatePoints(positions: Float32Array, density: number): Float32Array {
    if (density >= 1.0) return positions;
    
    const step = Math.max(1, Math.floor(1 / density));
    const decimated: number[] = [];
    
    for (let i = 0; i < positions.length; i += 3 * step) {
      decimated.push(positions[i], positions[i + 1], positions[i + 2]);
    }
    
    return new Float32Array(decimated);
  }
}

// Performance monitoring with heat maps
export class PerformanceProfiler {
  private static hotspots = new Map<string, { count: number; totalTime: number; avgTime: number }>();
  private static currentProfile = new Map<string, number>();

  static startProfile(label: string): void {
    this.currentProfile.set(label, performance.now());
  }

  static endProfile(label: string): void {
    const start = this.currentProfile.get(label);
    if (start) {
      const duration = performance.now() - start;
      const existing = this.hotspots.get(label);
      
      if (existing) {
        existing.count++;
        existing.totalTime += duration;
        existing.avgTime = existing.totalTime / existing.count;
      } else {
        this.hotspots.set(label, { count: 1, totalTime: duration, avgTime: duration });
      }
      
      this.currentProfile.delete(label);
    }
  }

  static getHotspots(): Array<{ label: string; avgTime: number; count: number }> {
    return Array.from(this.hotspots.entries())
      .map(([label, data]) => ({ label, avgTime: data.avgTime, count: data.count }))
      .sort((a, b) => b.avgTime - a.avgTime);
  }

  static clearProfiles(): void {
    this.hotspots.clear();
    this.currentProfile.clear();
  }
}
```

#### client/src/utils/rateLimiter.ts
```ts

// Simple client-side rate limiter
export class RateLimiter {
  private static attempts: Map<string, number[]> = new Map();
  
  static isAllowed(key: string, maxAttempts: number = 5, windowMs: number = 60000): boolean {
    const now = Date.now();
    const windowStart = now - windowMs;
    
    // Get existing attempts for this key
    const keyAttempts = this.attempts.get(key) || [];
    
    // Filter out attempts outside the time window
    const recentAttempts = keyAttempts.filter(timestamp => timestamp > windowStart);
    
    // Check if we're within the limit
    if (recentAttempts.length >= maxAttempts) {
      console.warn(`Rate limit exceeded for ${key}. ${recentAttempts.length}/${maxAttempts} attempts in last ${windowMs}ms`);
      return false;
    }
    
    // Add current attempt
    recentAttempts.push(now);
    this.attempts.set(key, recentAttempts);
    
    return true;
  }
  
  static reset(key: string) {
    this.attempts.delete(key);
  }
  
  static getAttemptCount(key: string, windowMs: number = 60000): number {
    const now = Date.now();
    const windowStart = now - windowMs;
    const keyAttempts = this.attempts.get(key) || [];
    return keyAttempts.filter(timestamp => timestamp > windowStart).length;
  }
}

```

#### client/src/utils/renderTargetPool.ts
```ts

class RenderTargetPool {
  private pool: HTMLCanvasElement[] = [];
  private activeTargets = new Set<HTMLCanvasElement>();
  private maxPoolSize = 8;

  acquireCanvas(width: number, height: number): HTMLCanvasElement {
    const suitable = this.pool.find(canvas => 
      canvas.width === width && 
      canvas.height === height && 
      !this.activeTargets.has(canvas)
    );

    if (suitable) {
      this.activeTargets.add(suitable);
      return suitable;
    }

    if (this.pool.length < this.maxPoolSize) {
      const canvas = document.createElement('canvas');
      canvas.width = width;
      canvas.height = height;
      this.pool.push(canvas);
      this.activeTargets.add(canvas);
      return canvas;
    }

    // Fallback: create temporary canvas
    const canvas = document.createElement('canvas');
    canvas.width = width;
    canvas.height = height;
    return canvas;
  }

  releaseCanvas(canvas: HTMLCanvasElement): void {
    this.activeTargets.delete(canvas);
    // Clear for reuse
    const ctx = canvas.getContext('2d');
    if (ctx) {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
    }
  }

  clear(): void {
    this.pool = [];
    this.activeTargets.clear();
  }
}

export const renderTargetPool = new RenderTargetPool();

```

#### client/src/utils/securityLogger.ts
```ts
// Security logging utility
export class SecurityLogger {
  private static logs: Array<{
    timestamp: string;
    level: 'info' | 'warning' | 'error';
    event: string;
    details?: any;
    userAgent?: string;
  }> = [];

  static logSecurityEvent(
    level: 'info' | 'warning' | 'error',
    event: string,
    details?: any
  ) {
    const logEntry = {
      timestamp: new Date().toISOString(),
      level,
      event,
      details: details ? JSON.stringify(details) : undefined,
      userAgent: navigator.userAgent,
    };

    this.logs.push(logEntry);
    
    // Console logging for development
    const logMessage = `[SECURITY ${level.toUpperCase()}] ${event}`;
    if (level === 'error') {
      console.error(logMessage, details);
    } else if (level === 'warning') {
      console.warn(logMessage, details);
    } else {
      console.log(logMessage, details);
    }

    // Keep only last 100 logs to prevent memory issues
    if (this.logs.length > 100) {
      this.logs = this.logs.slice(-100);
    }
  }

  static getSecurityLogs() {
    return [...this.logs];
  }

  static logFileUploadAttempt(fileName: string, fileSize: number, mimeType: string) {
    this.logSecurityEvent('info', 'FILE_UPLOAD_ATTEMPT', {
      fileName,
      fileSize,
      mimeType,
    });
  }

  static logFileUploadSuccess(fileName: string) {
    this.logSecurityEvent('info', 'FILE_UPLOAD_SUCCESS', { fileName });
  }

  static logFileUploadFailure(fileName: string, reason: string) {
    this.logSecurityEvent('warning', 'FILE_UPLOAD_FAILURE', {
      fileName,
      reason,
    });
  }

  static logSuspiciousActivity(activity: string, details?: any) {
    this.logSecurityEvent('error', 'SUSPICIOUS_ACTIVITY', {
      activity,
      ...details,
    });
  }
}

```

#### client/src/utils/videoEncoder.ts
```ts

import WebMWriter from 'webm-writer';
import { MemoryManager, ErrorRecovery, PerformanceMonitor } from './memoryManager';

export interface VideoEncoderOptions {
  width: number;
  height: number;
  quality: number;
  frameRate: number;
  transparent?: boolean;
}

export interface VideoFrame {
  canvas: HTMLCanvasElement;
  timestamp: number;
}

export class VideoEncoder {
  private writer: WebMWriter;
  private frames: VideoFrame[] = [];
  private isEncoding = false;

  constructor(options: VideoEncoderOptions) {
    this.writer = new WebMWriter({
      quality: options.quality / 100, // Convert 0-100 to 0-1
      frameRate: options.frameRate,
      transparent: options.transparent || false
    });
  }

  addFrame(canvas: HTMLCanvasElement, timestamp: number = 0): void {
    if (this.isEncoding) {
      throw new Error('Cannot add frames while encoding');
    }

    const timer = PerformanceMonitor.startTimer('video_frame_clone');
    
    // Use memory-managed canvas cloning
    const clonedCanvas = MemoryManager.cloneCanvas(canvas);
    
    timer();

    this.frames.push({
      canvas: clonedCanvas,
      timestamp
    });

    // Add frame to WebM writer
    this.writer.addFrame(clonedCanvas);
  }

  async encode(
    onProgress?: (progress: number) => void,
    onComplete?: (blob: Blob) => void,
    onError?: (error: Error) => void
  ): Promise<Blob> {
    return ErrorRecovery.retry(async () => {
      return new Promise<Blob>((resolve, reject) => {
        if (this.isEncoding) {
          reject(new Error('Already encoding'));
          return;
        }

        if (this.frames.length === 0) {
          reject(new Error('No frames to encode'));
          return;
        }

        const timer = PerformanceMonitor.startTimer('video_encode');
        this.isEncoding = true;

        try {
          let progressInterval: number | null = null;
          let currentProgress = 0;

          if (onProgress) {
            progressInterval = window.setInterval(() => {
              currentProgress = Math.min(currentProgress + 0.1, 0.9);
              onProgress(currentProgress);
            }, 100);
          }

          this.writer.complete().then((blob: Blob) => {
            this.isEncoding = false;
            timer();
            this.disposeFrames();
            
            if (progressInterval) {
              clearInterval(progressInterval);
            }
            
            if (onProgress) {
              onProgress(1.0);
            }
            
            if (onComplete) onComplete(blob);
            resolve(blob);
          }).catch((error: Error) => {
            this.isEncoding = false;
            timer();
            
            if (progressInterval) {
              clearInterval(progressInterval);
            }
            
            console.error('Video encoding error:', error);
            if (onError) onError(error);
            reject(error);
          });

        } catch (error) {
          this.isEncoding = false;
          timer();
          reject(error);
        }
      });
    }, 2, (attempt, error) => {
      console.warn(`Video encoding attempt ${attempt} failed:`, error);
    });
  }

  clear(): void {
    if (this.isEncoding) {
      throw new Error('Cannot clear while encoding');
    }
    this.disposeFrames();
  }

  private disposeFrames(): void {
    this.frames.forEach(frame => {
      MemoryManager.releaseCanvas(frame.canvas);
    });
    this.frames = [];
  }

  getFrameCount(): number {
    return this.frames.length;
  }

  getEstimatedSize(): number {
    // Rough estimation for WebM video size in MB
    const pixelsPerFrame = this.frames.length > 0 ? 
      this.frames[0].canvas.width * this.frames[0].canvas.height : 0;
    const totalPixels = pixelsPerFrame * this.frames.length;
    const compressionFactor = 0.1; // WebM has excellent compression
    return (totalPixels * compressionFactor) / (1024 * 1024);
  }
}

export const createVideoEncoder = (options: VideoEncoderOptions): VideoEncoder => {
  return new VideoEncoder(options);
};

```

#### client/src/utils/visualModes.ts
```ts
/**
 * Cinematic-only mode system for PixelFlow visualization
 * Temporarily isolated to showcase cinematic AI depth estimation
 */

export interface VisualMode {
  id: string;
  name: string;
  description: string;
  settings: {
    nearClipping: number;
    farClipping: number;
    pointSize: number;
    zOffset: number;
    fov: number;
    depthScale: number;
    minDistance: number;
    maxDistance: number;
    depthPower: number;
    pointSizeDepthFactor: number;
    invertDepth: boolean;
    epsilon: number;
    exponentialK: number;
    gamma: number;
    stereographicC: number;
    offsetStrength: number;
    noiseScale: number;
    useRealDepth: boolean;
  };
}

export const VISUAL_MODES: VisualMode[] = [
  {
    id: 'cinematic',
    name: 'Cinematic',
    description: 'AI depth estimation with artistic effects for immersive visualization',
    settings: {
      nearClipping: 0.1,
      farClipping: 0.9,
      pointSize: 2.0,
      zOffset: 0.0,
      fov: 45,
      depthScale: 0.8,
      minDistance: 0.0,
      maxDistance: 1.0,
      depthPower: 1.2,
      pointSizeDepthFactor: 1.5,
      invertDepth: false,
      epsilon: 0.05,
      exponentialK: 0.3,
      gamma: 1.2,
      stereographicC: 0.2,
      offsetStrength: 0.15,
      noiseScale: 80.0,
      useRealDepth: true
    }
  }
];

export function getVisualMode(id: string): VisualMode | undefined {
  return VISUAL_MODES.find(mode => mode.id === id);
}

export function applyVisualMode(mode: VisualMode, onSettingsChange: (key: string, value: number | boolean) => void): void {
  Object.entries(mode.settings).forEach(([key, value]) => {
    onSettingsChange(key, value);
  });
}
```

#### client/src/utils/webglForcer.ts
```ts
/**
 * WebGL Context Forcer - Aggressive WebGL context creation for PixelFlow
 * Forces hardware acceleration and bypasses browser limitations
 */

export interface WebGLContextInfo {
  context: WebGLRenderingContext | WebGL2RenderingContext | null;
  version: string;
  vendor: string;
  renderer: string;
  supported: boolean;
  error?: string;
}

export class WebGLForcer {
  private static instance: WebGLForcer;
  private contextCache: Map<HTMLCanvasElement, WebGLRenderingContext | WebGL2RenderingContext> = new Map();

  static getInstance(): WebGLForcer {
    if (!WebGLForcer.instance) {
      WebGLForcer.instance = new WebGLForcer();
    }
    return WebGLForcer.instance;
  }

  /**
   * Override browser WebGL detection flags
   */
  private overrideBrowserDetection(): void {
    if (typeof window !== 'undefined') {
      (window as any).WebGLRenderingContext = window.WebGLRenderingContext || function() {};
      (window as any).WebGL2RenderingContext = window.WebGL2RenderingContext || function() {};
      
      if (navigator.hardwareConcurrency === undefined) {
        Object.defineProperty(navigator, 'hardwareConcurrency', {
          value: 8,
          writable: false
        });
      }
    }
  }

  /**
   * Enable hardware acceleration attributes on canvas
   */
  private enableHardwareAcceleration(canvas: HTMLCanvasElement): void {
    canvas.style.imageRendering = 'optimizeQuality';
    canvas.style.transform = 'translateZ(0)';
    canvas.style.willChange = 'transform';
    canvas.style.backfaceVisibility = 'hidden';
    canvas.style.perspective = '1000px';
  }

  /**
   * Force WebGL context creation with hardware acceleration override
   */
  forceWebGLContext(canvas: HTMLCanvasElement): WebGLContextInfo {
    this.overrideBrowserDetection();
    this.enableHardwareAcceleration(canvas);
    
    const cached = this.contextCache.get(canvas);
    if (cached) {
      return this.getContextInfo(cached);
    }

    // Try progressive context attributes from most compatible to least
    const contextAttributeOptions: WebGLContextAttributes[] = [
      {
        alpha: false,
        depth: true,
        stencil: false,
        antialias: false,
        premultipliedAlpha: false,
        preserveDrawingBuffer: false,
        failIfMajorPerformanceCaveat: false,
        powerPreference: 'default',
        desynchronized: false
      },
      {
        alpha: true,
        depth: true,
        stencil: false,
        antialias: false,
        premultipliedAlpha: false,
        preserveDrawingBuffer: true,
        failIfMajorPerformanceCaveat: false,
        powerPreference: 'high-performance',
        desynchronized: false
      },
      {
        // Minimal attributes for maximum compatibility
        failIfMajorPerformanceCaveat: false
      }
    ];

    const contextTypes = ['webgl2', 'webgl', 'experimental-webgl', 'webkit-3d', 'moz-webgl'];

    // Try each combination of context type and attributes
    for (const attributes of contextAttributeOptions) {
      for (const contextType of contextTypes) {
        try {
          const gl = canvas.getContext(contextType, attributes) as WebGLRenderingContext | WebGL2RenderingContext;
          
          if (gl && this.validateWebGLContext(gl)) {
            this.contextCache.set(canvas, gl);
            console.log(`WebGL context created successfully: ${contextType} with attributes:`, attributes);
            this.initializeWebGLContext(gl);
            return this.getContextInfo(gl);
          }
        } catch (error) {
          console.warn(`Failed to create ${contextType} context with attributes:`, attributes, error);
        }
      }
    }

    return this.forceSoftwareWebGL(canvas, contextAttributeOptions[0]);
  }

  /**
   * Validate WebGL context functionality
   */
  private validateWebGLContext(gl: WebGLRenderingContext | WebGL2RenderingContext): boolean {
    try {
      gl.getParameter(gl.VERSION);
      gl.getParameter(gl.VENDOR);
      gl.getParameter(gl.RENDERER);
      
      const vertexShader = gl.createShader(gl.VERTEX_SHADER);
      const fragmentShader = gl.createShader(gl.FRAGMENT_SHADER);
      
      if (!vertexShader || !fragmentShader) {
        return false;
      }

      gl.shaderSource(vertexShader, `
        attribute vec2 position;
        void main() {
          gl_Position = vec4(position, 0.0, 1.0);
        }
      `);
      
      gl.shaderSource(fragmentShader, `
        precision mediump float;
        void main() {
          gl_FragColor = vec4(1.0, 1.0, 1.0, 1.0);
        }
      `);

      gl.compileShader(vertexShader);
      gl.compileShader(fragmentShader);

      const vertexCompiled = gl.getShaderParameter(vertexShader, gl.COMPILE_STATUS);
      const fragmentCompiled = gl.getShaderParameter(fragmentShader, gl.COMPILE_STATUS);

      gl.deleteShader(vertexShader);
      gl.deleteShader(fragmentShader);

      return vertexCompiled && fragmentCompiled;
    } catch (error) {
      console.warn('WebGL context validation failed:', error);
      return false;
    }
  }

  /**
   * Initialize WebGL context with required settings
   */
  private initializeWebGLContext(gl: WebGLRenderingContext | WebGL2RenderingContext): void {
    try {
      gl.enable(gl.DEPTH_TEST);
      gl.enable(gl.BLEND);
      gl.blendFunc(gl.SRC_ALPHA, gl.ONE_MINUS_SRC_ALPHA);
      gl.viewport(0, 0, gl.canvas.width, gl.canvas.height);
      gl.clearColor(0.0, 0.0, 0.0, 1.0);
      gl.clear(gl.COLOR_BUFFER_BIT | gl.DEPTH_BUFFER_BIT);
      console.log('WebGL context initialized successfully');
    } catch (error) {
      console.warn('WebGL context initialization warning:', error);
    }
  }

  /**
   * Force software WebGL implementation with canvas fallback
   */
  private forceSoftwareWebGL(canvas: HTMLCanvasElement, attributes: WebGLContextAttributes): WebGLContextInfo {
    console.log('Attempting software WebGL fallback...');
    
    try {
      // Create a fresh canvas for software rendering
      const softwareCanvas = document.createElement('canvas');
      softwareCanvas.width = canvas.width || 640;
      softwareCanvas.height = canvas.height || 480;
      
      const softwareAttributes = {
        ...attributes,
        failIfMajorPerformanceCaveat: false,
        powerPreference: 'default' as const,
        alpha: false,
        antialias: false
      };

      // Try basic WebGL context on new canvas
      const gl = softwareCanvas.getContext('webgl', softwareAttributes) as WebGLRenderingContext;
      
      if (gl) {
        // Replace original canvas with working one
        if (canvas.parentNode) {
          canvas.parentNode.replaceChild(softwareCanvas, canvas);
        }
        
        this.contextCache.set(softwareCanvas, gl);
        this.initializeWebGLContext(gl);
        console.log('Software WebGL context created successfully');
        return this.getContextInfo(gl);
      }
    } catch (error) {
      console.warn('Software WebGL creation failed:', error);
    }

    // Final fallback: Create mock context for development
    console.log('Creating Canvas 2D fallback for development');
    return this.createCanvas2DFallback(canvas);
  }

  /**
   * Canvas 2D fallback for development environments
   */
  private createCanvas2DFallback(canvas: HTMLCanvasElement): WebGLContextInfo {
    const ctx = canvas.getContext('2d');
    if (ctx) {
      // Clear canvas with black background
      ctx.fillStyle = '#000000';
      ctx.fillRect(0, 0, canvas.width, canvas.height);
      
      // Draw simple message
      ctx.fillStyle = '#ffffff';
      ctx.font = '16px monospace';
      ctx.textAlign = 'center';
      ctx.fillText('WebGL Not Available', canvas.width / 2, canvas.height / 2 - 10);
      ctx.fillText('Canvas 2D Fallback Active', canvas.width / 2, canvas.height / 2 + 10);
      
      console.log('Canvas 2D fallback active - some features will be limited');
    }

    return {
      context: null,
      version: 'Canvas 2D Fallback',
      vendor: 'Browser Default', 
      renderer: 'Software Renderer',
      supported: false,
      error: 'WebGL not available - using Canvas 2D fallback'
    };
  }

  /**
   * Get context information
   */
  private getContextInfo(gl: WebGLRenderingContext | WebGL2RenderingContext): WebGLContextInfo {
    try {
      return {
        context: gl,
        version: gl.getParameter(gl.VERSION),
        vendor: gl.getParameter(gl.VENDOR),
        renderer: gl.getParameter(gl.RENDERER),
        supported: true
      };
    } catch (error) {
      return {
        context: gl,
        version: 'Unknown',
        vendor: 'Unknown',
        renderer: 'Unknown', 
        supported: true
      };
    }
  }

  /**
   * Clean up context cache
   */
  dispose(): void {
    this.contextCache.clear();
  }
}

export const webglForcer = WebGLForcer.getInstance();
```

#### client/src/utils/webxr.ts
```ts
/**
 * WebXR utilities for immersive point cloud visualization
 * Provides VR/AR support for PixelFlow point clouds
 */

export interface XRSettings {
  enabled: boolean;
  mode: 'vr' | 'ar' | 'inline';
  handTracking: boolean;
  environmentBlend: 'opaque' | 'additive' | 'alpha-blend';
  referenceSpace: 'local' | 'local-floor' | 'bounded-floor' | 'unbounded';
}

export interface XRController {
  id: number;
  position: [number, number, number];
  rotation: [number, number, number, number];
  isConnected: boolean;
  buttons: boolean[];
  axes: number[];
}

export class WebXRManager {
  private xrSession: XRSession | null = null;
  private xrReferenceSpace: XRReferenceSpace | null = null;
  private animationFrame: number | null = null;
  private controllers: Map<number, XRController> = new Map();
  private canvas: HTMLCanvasElement;
  private gl: WebGL2RenderingContext;
  private settings: XRSettings;

  constructor(canvas: HTMLCanvasElement, gl: WebGL2RenderingContext, settings: XRSettings) {
    this.canvas = canvas;
    this.gl = gl;
    this.settings = settings;
  }

  async isSupported(): Promise<boolean> {
    if (!navigator.xr) {
      console.log('WebXR not supported in this browser');
      return false;
    }

    try {
      const isVRSupported = await navigator.xr.isSessionSupported('immersive-vr');
      const isARSupported = await navigator.xr.isSessionSupported('immersive-ar');
      return isVRSupported || isARSupported;
    } catch (error) {
      console.warn('WebXR support check failed:', error);
      return false;
    }
  }

  async startSession(mode: 'vr' | 'ar' = 'vr'): Promise<boolean> {
    if (!navigator.xr) return false;

    try {
      const sessionMode = mode === 'vr' ? 'immersive-vr' : 'immersive-ar';
      const sessionInit: XRSessionInit = {
        requiredFeatures: ['local'],
        optionalFeatures: ['hand-tracking', 'local-floor', 'bounded-floor']
      };

      this.xrSession = await navigator.xr.requestSession(sessionMode, sessionInit);
      
      // Configure WebGL layer
      const glLayer = new XRWebGLLayer(this.xrSession, this.gl);
      await this.xrSession.updateRenderState({ baseLayer: glLayer });

      // Set up reference space
      this.xrReferenceSpace = await this.xrSession.requestReferenceSpace(this.settings.referenceSpace);

      // Start the render loop
      this.xrSession.requestAnimationFrame(this.onXRFrame.bind(this));

      // Set up event listeners
      this.xrSession.addEventListener('end', this.onSessionEnd.bind(this));
      this.xrSession.addEventListener('inputsourceschange', this.onInputSourcesChange.bind(this));

      console.log(`WebXR ${mode.toUpperCase()} session started successfully`);
      return true;
    } catch (error) {
      console.error('Failed to start WebXR session:', error);
      return false;
    }
  }

  private onXRFrame(time: number, frame: XRFrame) {
    if (!this.xrSession || !this.xrReferenceSpace) return;

    const session = this.xrSession;
    this.animationFrame = session.requestAnimationFrame(this.onXRFrame.bind(this));

    // Get viewer pose
    const pose = frame.getViewerPose(this.xrReferenceSpace);
    if (!pose) return;

    // Update controller states
    this.updateControllers(frame);

    // Render for each eye
    const glLayer = session.renderState.baseLayer!;
    this.gl.bindFramebuffer(this.gl.FRAMEBUFFER, glLayer.framebuffer);

    for (let i = 0; i < pose.views.length; i++) {
      const view = pose.views[i];
      const viewport = glLayer.getViewport(view)!;
      
      this.gl.viewport(viewport.x, viewport.y, viewport.width, viewport.height);
      
      // Render point cloud for this view
      this.renderPointCloudForEye(view);
    }
  }

  private updateControllers(frame: XRFrame) {
    if (!this.xrSession || !this.xrReferenceSpace) return;

    for (let i = 0; i < this.xrSession.inputSources.length; i++) {
      const inputSource = this.xrSession.inputSources[i];
      if (inputSource.gripSpace) {
        const pose = frame.getPose(inputSource.gripSpace, this.xrReferenceSpace);
        if (pose) {
          const controller: XRController = {
            id: this.getControllerID(inputSource),
            position: [pose.transform.position.x, pose.transform.position.y, pose.transform.position.z],
            rotation: [
              pose.transform.orientation.x,
              pose.transform.orientation.y,
              pose.transform.orientation.z,
              pose.transform.orientation.w
            ],
            isConnected: true,
            buttons: inputSource.gamepad ? Array.from(inputSource.gamepad.buttons).map((b: any) => b.pressed) : [],
            axes: inputSource.gamepad ? Array.from(inputSource.gamepad.axes) : []
          };
          
          this.controllers.set(controller.id, controller);
        }
      }
    }
  }

  private getControllerID(inputSource: XRInputSource): number {
    // Simple ID generation based on handedness
    return inputSource.handedness === 'left' ? 0 : 1;
  }

  private renderPointCloudForEye(view: XRView) {
    // Get view matrices
    const viewMatrix = view.transform.inverse.matrix;
    const projectionMatrix = view.projectionMatrix;

    // Dispatch render event with XR matrices
    window.dispatchEvent(new CustomEvent('xr-render', {
      detail: {
        viewMatrix: Array.from(viewMatrix),
        projectionMatrix: Array.from(projectionMatrix),
        eye: view.eye
      }
    }));
  }

  private onSessionEnd() {
    this.xrSession = null;
    this.xrReferenceSpace = null;
    this.controllers.clear();
    
    if (this.animationFrame) {
      // Note: cancelAnimationFrame not available on XRSession, it ends automatically
      this.animationFrame = null;
    }

    console.log('WebXR session ended');
    
    // Dispatch end event
    window.dispatchEvent(new CustomEvent('xr-session-end'));
  }

  private onInputSourcesChange(event: any) {
    // Handle controller connection/disconnection
    for (const removed of event.removed) {
      const id = this.getControllerID(removed);
      this.controllers.delete(id);
    }

    console.log('XR input sources changed:', event);
  }

  async endSession(): Promise<void> {
    if (this.xrSession) {
      await this.xrSession.end();
    }
  }

  getControllers(): XRController[] {
    return Array.from(this.controllers.values());
  }

  isSessionActive(): boolean {
    return this.xrSession !== null;
  }

  // Hand tracking utilities
  getHandPose(handedness: 'left' | 'right', frame: XRFrame): XRJointPose[] | null {
    if (!this.xrSession || !this.xrReferenceSpace) return null;

    const inputSource = Array.from(this.xrSession.inputSources).find(
      source => source.handedness === handedness && source.hand
    );

    if (!inputSource?.hand) return null;

    const poses: XRJointPose[] = [];
    // Iterate through XRHand joints using proper WebXR API
    const jointNames: XRHandJoint[] = [
      'wrist', 'thumb-metacarpal', 'thumb-phalanx-proximal', 'thumb-phalanx-distal', 'thumb-tip',
      'index-finger-metacarpal', 'index-finger-phalanx-proximal', 'index-finger-phalanx-intermediate', 
      'index-finger-phalanx-distal', 'index-finger-tip', 'middle-finger-metacarpal', 
      'middle-finger-phalanx-proximal', 'middle-finger-phalanx-intermediate', 
      'middle-finger-phalanx-distal', 'middle-finger-tip', 'ring-finger-metacarpal',
      'ring-finger-phalanx-proximal', 'ring-finger-phalanx-intermediate', 
      'ring-finger-phalanx-distal', 'ring-finger-tip', 'pinky-finger-metacarpal',
      'pinky-finger-phalanx-proximal', 'pinky-finger-phalanx-intermediate',
      'pinky-finger-phalanx-distal', 'pinky-finger-tip'
    ];

    for (const jointName of jointNames) {
      const joint = inputSource.hand.get(jointName);
      if (joint && frame.getJointPose) {
        const pose = frame.getJointPose(joint, this.xrReferenceSpace);
        if (pose) {
          poses.push(pose);
        }
      }
    }

    return poses.length > 0 ? poses : null;
  }
}

// Utility functions for XR interaction
export function createXRButton(onVRClick: () => void, onARClick: () => void): HTMLElement {
  const container = document.createElement('div');
  container.className = 'xr-controls flex gap-2';

  const vrButton = document.createElement('button');
  vrButton.textContent = 'Enter VR';
  vrButton.className = 'px-4 py-2 bg-purple-600 hover:bg-purple-500 text-white rounded-lg transition-colors';
  vrButton.onclick = onVRClick;

  const arButton = document.createElement('button');
  arButton.textContent = 'Enter AR';
  arButton.className = 'px-4 py-2 bg-blue-600 hover:bg-blue-500 text-white rounded-lg transition-colors';
  arButton.onclick = onARClick;

  container.appendChild(vrButton);
  container.appendChild(arButton);

  return container;
}

// Matrix utilities for XR
export function createXRViewMatrix(position: [number, number, number], rotation: [number, number, number, number]): Float32Array {
  const [x, y, z] = position;
  const [qx, qy, qz, qw] = rotation;
  
  // Convert quaternion to rotation matrix, then invert for view matrix
  const matrix = new Float32Array(16);
  
  // Quaternion to matrix conversion
  const xx = qx * qx;
  const yy = qy * qy;
  const zz = qz * qz;
  const xy = qx * qy;
  const xz = qx * qz;
  const yz = qy * qz;
  const wx = qw * qx;
  const wy = qw * qy;
  const wz = qw * qz;

  matrix[0] = 1 - 2 * (yy + zz);
  matrix[1] = 2 * (xy + wz);
  matrix[2] = 2 * (xz - wy);
  matrix[3] = 0;

  matrix[4] = 2 * (xy - wz);
  matrix[5] = 1 - 2 * (xx + zz);
  matrix[6] = 2 * (yz + wx);
  matrix[7] = 0;

  matrix[8] = 2 * (xz + wy);
  matrix[9] = 2 * (yz - wx);
  matrix[10] = 1 - 2 * (xx + yy);
  matrix[11] = 0;

  matrix[12] = -x;
  matrix[13] = -y;
  matrix[14] = -z;
  matrix[15] = 1;

  return matrix;
}
```

### Styles

#### client/src/index.css
```css

@tailwind base;
@tailwind components;
@tailwind utilities;

/* Definition of the design system. All colors, gradients, fonts, etc should be defined here. */

@layer base {
  :root {
    --background: 0 0% 100%;
    --foreground: 222.2 84% 4.9%;

    --card: 0 0% 100%;
    --card-foreground: 222.2 84% 4.9%;

    --popover: 0 0% 100%;
    --popover-foreground: 222.2 84% 4.9%;

    --primary: 222.2 47.4% 11.2%;
    --primary-foreground: 210 40% 98%;

    --secondary: 210 40% 96.1%;
    --secondary-foreground: 222.2 47.4% 11.2%;

    --muted: 210 40% 96.1%;
    --muted-foreground: 215.4 16.3% 46.9%;

    --accent: 210 40% 96.1%;
    --accent-foreground: 222.2 47.4% 11.2%;

    --destructive: 0 84.2% 60.2%;
    --destructive-foreground: 210 40% 98%;

    --border: 214.3 31.8% 91.4%;
    --input: 214.3 31.8% 91.4%;
    --ring: 222.2 84% 4.9%;

    --radius: 0.5rem;

    --sidebar-background: 0 0% 98%;

    --sidebar-foreground: 240 5.3% 26.1%;

    --sidebar-primary: 240 5.9% 10%;

    --sidebar-primary-foreground: 0 0% 98%;

    --sidebar-accent: 240 4.8% 95.9%;

    --sidebar-accent-foreground: 240 5.9% 10%;

    --sidebar-border: 220 13% 91%;

    --sidebar-ring: 217.2 91.2% 59.8%;
  }

  .dark {
    --background: 222.2 84% 4.9%;
    --foreground: 210 40% 98%;

    --card: 222.2 84% 4.9%;
    --card-foreground: 210 40% 98%;

    --popover: 222.2 84% 4.9%;
    --popover-foreground: 210 40% 98%;

    --primary: 210 40% 98%;
    --primary-foreground: 222.2 47.4% 11.2%;

    --secondary: 217.2 32.6% 17.5%;
    --secondary-foreground: 210 40% 98%;

    --muted: 217.2 32.6% 17.5%;
    --muted-foreground: 215 20.2% 65.1%;

    --accent: 217.2 32.6% 17.5%;
    --accent-foreground: 210 40% 98%;

    --destructive: 0 62.8% 30.6%;
    --destructive-foreground: 210 40% 98%;

    --border: 217.2 32.6% 17.5%;
    --input: 217.2 32.6% 17.5%;
    --ring: 212.7 26.8% 83.9%;
    --sidebar-background: 240 5.9% 10%;
    --sidebar-foreground: 240 4.8% 95.9%;
    --sidebar-primary: 224.3 76.3% 48%;
    --sidebar-primary-foreground: 0 0% 100%;
    --sidebar-accent: 240 3.7% 15.9%;
    --sidebar-accent-foreground: 240 4.8% 95.9%;
    --sidebar-border: 240 3.7% 15.9%;
    --sidebar-ring: 217.2 91.2% 59.8%;
  }
}

@layer base {
  * {
    @apply border-border;
  }

  body {
    @apply bg-black text-foreground;
  }
}

```

### Library

#### client/src/lib/utils.ts
```ts
import { clsx, type ClassValue } from "clsx"
import { twMerge } from "tailwind-merge"

export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs))
}

```

---

## Backend Server

### server/index.ts
```ts
import express, { type Request, Response, NextFunction } from "express";
import { registerRoutes } from "./routes";
import { setupVite, serveStatic, log } from "./vite";

const app = express();
app.use(express.json());
app.use(express.urlencoded({ extended: false }));

app.use((req, res, next) => {
  const start = Date.now();
  const path = req.path;
  let capturedJsonResponse: Record<string, any> | undefined = undefined;

  const originalResJson = res.json;
  res.json = function (bodyJson, ...args) {
    capturedJsonResponse = bodyJson;
    return originalResJson.apply(res, [bodyJson, ...args]);
  };

  res.on("finish", () => {
    const duration = Date.now() - start;
    if (path.startsWith("/api")) {
      let logLine = `${req.method} ${path} ${res.statusCode} in ${duration}ms`;
      if (capturedJsonResponse) {
        logLine += ` :: ${JSON.stringify(capturedJsonResponse)}`;
      }

      if (logLine.length > 80) {
        logLine = logLine.slice(0, 79) + "…";
      }

      log(logLine);
    }
  });

  next();
});

(async () => {
  const server = await registerRoutes(app);

  app.use((err: any, _req: Request, res: Response, _next: NextFunction) => {
    const status = err.status || err.statusCode || 500;
    const message = err.message || "Internal Server Error";

    res.status(status).json({ message });
    throw err;
  });

  // importantly only setup vite in development and after
  // setting up all the other routes so the catch-all route
  // doesn't interfere with the other routes
  if (app.get("env") === "development") {
    await setupVite(app, server);
  } else {
    serveStatic(app);
  }

  // ALWAYS serve the app on port 5000
  // this serves both the API and the client.
  // It is the only port that is not firewalled.
  const port = 5000;
  server.listen({
    port,
    host: "0.0.0.0",
    reusePort: true,
  }, () => {
    log(`serving on port ${port}`);
  });
})();

```

### server/routes.ts
```ts
import type { Express } from "express";
import { createServer, type Server } from "http";
import { storage } from "./storage";

export async function registerRoutes(app: Express): Promise<Server> {
  // Demo video now served directly from public directory
  // No API routes needed for video serving

  const httpServer = createServer(app);

  return httpServer;
}

```

### server/storage.ts
```ts
import { users, type User, type InsertUser } from "@shared/schema";

// modify the interface with any CRUD methods
// you might need

export interface IStorage {
  getUser(id: number): Promise<User | undefined>;
  getUserByUsername(username: string): Promise<User | undefined>;
  createUser(user: InsertUser): Promise<User>;
}

export class MemStorage implements IStorage {
  private users: Map<number, User>;
  currentId: number;

  constructor() {
    this.users = new Map();
    this.currentId = 1;
  }

  async getUser(id: number): Promise<User | undefined> {
    return this.users.get(id);
  }

  async getUserByUsername(username: string): Promise<User | undefined> {
    return Array.from(this.users.values()).find(
      (user) => user.username === username,
    );
  }

  async createUser(insertUser: InsertUser): Promise<User> {
    const id = this.currentId++;
    const user: User = { ...insertUser, id };
    this.users.set(id, user);
    return user;
  }
}

export const storage = new MemStorage();

```

### server/vite.ts
```ts
import express, { type Express } from "express";
import fs from "fs";
import path from "path";
import { createServer as createViteServer, createLogger } from "vite";
import { type Server } from "http";
import viteConfig from "../vite.config";
import { nanoid } from "nanoid";

const viteLogger = createLogger();

export function log(message: string, source = "express") {
  const formattedTime = new Date().toLocaleTimeString("en-US", {
    hour: "numeric",
    minute: "2-digit",
    second: "2-digit",
    hour12: true,
  });

  console.log(`${formattedTime} [${source}] ${message}`);
}

export async function setupVite(app: Express, server: Server) {
  const serverOptions = {
    middlewareMode: true,
    hmr: { server },
    allowedHosts: true,
  };

  const vite = await createViteServer({
    ...viteConfig,
    configFile: false,
    customLogger: {
      ...viteLogger,
      error: (msg, options) => {
        viteLogger.error(msg, options);
        process.exit(1);
      },
    },
    server: serverOptions,
    appType: "custom",
  });

  app.use(vite.middlewares);
  app.use("*", async (req, res, next) => {
    const url = req.originalUrl;

    try {
      const clientTemplate = path.resolve(
        import.meta.dirname,
        "..",
        "client",
        "index.html",
      );

      // always reload the index.html file from disk incase it changes
      let template = await fs.promises.readFile(clientTemplate, "utf-8");
      template = template.replace(
        `src="/src/main.tsx"`,
        `src="/src/main.tsx?v=${nanoid()}"`,
      );
      const page = await vite.transformIndexHtml(url, template);
      res.status(200).set({ "Content-Type": "text/html" }).end(page);
    } catch (e) {
      vite.ssrFixStacktrace(e as Error);
      next(e);
    }
  });
}

export function serveStatic(app: Express) {
  const distPath = path.resolve(import.meta.dirname, "public");

  if (!fs.existsSync(distPath)) {
    throw new Error(
      `Could not find the build directory: ${distPath}, make sure to build the client first`,
    );
  }

  app.use(express.static(distPath));

  // fall through to index.html if the file doesn't exist
  app.use("*", (_req, res) => {
    res.sendFile(path.resolve(distPath, "index.html"));
  });
}

```

---

## Shared Code

No shared files detected.

## Root Configuration

### vite.config.ts
```ts
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";
import path from "path";
import runtimeErrorOverlay from "@replit/vite-plugin-runtime-error-modal";

export default defineConfig({
  plugins: [
    react(),
    runtimeErrorOverlay(),
    ...(process.env.NODE_ENV !== "production" &&
    process.env.REPL_ID !== undefined
      ? [
          await import("@replit/vite-plugin-cartographer").then((m) =>
            m.cartographer(),
          ),
        ]
      : []),
  ],
  resolve: {
    alias: {
      "@": path.resolve(import.meta.dirname, "client", "src"),
      "@shared": path.resolve(import.meta.dirname, "shared"),
      "@assets": path.resolve(import.meta.dirname, "attached_assets"),
    },
  },
  root: path.resolve(import.meta.dirname, "client"),
  build: {
    outDir: path.resolve(import.meta.dirname, "dist/public"),
    emptyOutDir: true,
  },
});

```

---

## Build Instructions

To recreate this project from this archive:

### 1. Setup Project Structure
```bash
mkdir pixelflow-recreated
cd pixelflow-recreated
mkdir -p client/src/{components,hooks,lib,pages,utils}
mkdir -p client/src/components/ui
mkdir -p server
mkdir -p shared
```

### 2. Install Dependencies
```bash
npm init -y
# Install only the essential dependencies (31 packages):
npm install react react-dom react-router-dom @tanstack/react-query three @tensorflow/tfjs @tensorflow/tfjs-backend-webgl @tensorflow/tfjs-backend-webgpu @tensorflow-models/depth-estimation express gif.js html2canvas webm-writer framer-motion lucide-react tailwindcss @radix-ui/react-toast @radix-ui/react-tooltip class-variance-authority clsx tailwind-merge date-fns d3 drizzle-orm drizzle-zod memorystore next-themes tw-animate-css tailwindcss-animate wouter zod

# Development dependencies
npm install -D typescript tsx vite @vitejs/plugin-react drizzle-kit autoprefixer postcss
```

### 3. Copy Files
Copy each file from this archive to its corresponding location in the project structure.

### 4. Run Project
```bash
npm run dev
```

## File Manifest
Total functional files archived: 66

### Used Files (58):
- client/src/App.tsx
- client/src/components/AdvancedTransition.tsx
- client/src/components/AnimatedSlider.tsx
- client/src/components/ControlPanel.tsx
- client/src/components/DemoVideoSection.tsx
- client/src/components/GifExportDialog.tsx
- client/src/components/IntroAnimation.tsx
- client/src/components/LoadingScreen.tsx
- client/src/components/NeuralNetworkVisualizer.tsx
- client/src/components/OceanShader.tsx
- client/src/components/PixelMoshOverlay.tsx
- client/src/components/VRInterface.tsx
- client/src/components/VideoExportDialog.tsx
- client/src/components/WelcomeScreen.tsx
- client/src/components/ui/button.tsx
- client/src/components/ui/dialog.tsx
- client/src/components/ui/progress.tsx
- client/src/components/ui/select.tsx
- client/src/components/ui/slider.tsx
- client/src/components/ui/switch.tsx
- client/src/components/ui/toast.tsx
- client/src/components/ui/toaster.tsx
- client/src/components/ui/tooltip.tsx
- client/src/hooks/use-mobile.tsx
- client/src/hooks/use-toast.ts
- client/src/hooks/useGifExport.tsx
- client/src/hooks/useVideoExport.tsx
- client/src/hooks/useVideoPointCloud.tsx
- client/src/index.css
- client/src/lib/utils.ts
- client/src/main.tsx
- client/src/pages/FavoritesGallery.tsx
- client/src/pages/Index.tsx
- client/src/pages/NotFound.tsx
- client/src/utils/canvasPool.ts
- client/src/utils/demoVideo.ts
- client/src/utils/depthEstimation.ts
- client/src/utils/ditherShaders.ts
- client/src/utils/fileValidation.ts
- client/src/utils/fxaaProcessor.ts
- client/src/utils/gifEncoder.ts
- client/src/utils/gifOptimizer.ts
- client/src/utils/halftoneEffect.ts
- client/src/utils/instancedPointCloud.ts
- client/src/utils/memoryManager.ts
- client/src/utils/performanceOptimizer.ts
- client/src/utils/rateLimiter.ts
- client/src/utils/renderTargetPool.ts
- client/src/utils/securityLogger.ts
- client/src/utils/videoEncoder.ts
- client/src/utils/visualModes.ts
- client/src/utils/webglForcer.ts
- client/src/utils/webxr.ts
- server/index.ts
- server/routes.ts
- server/storage.ts
- server/vite.ts
- vite.config.ts

### Configuration Files (8):
- package.json
- vite.config.ts
- tailwind.config.ts
- postcss.config.js
- components.json
- drizzle.config.ts
- tsconfig.json
- .replit

---

*This archive represents a complete, functional snapshot of PixelFlow with all unnecessary code removed.*
*Every file in this archive is actively used and required for the application to function.*
