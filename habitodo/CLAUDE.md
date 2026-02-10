# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Habitodo is a habit tracker that doubles as a to-do list. It is a Next.js 16 app using the App Router, React 19, TypeScript, and Tailwind CSS v4.

## Commands

- `npm run dev` — start dev server (http://localhost:3000)
- `npm run build` — production build
- `npm run start` — serve production build
- `npm run lint` — run ESLint (uses `eslint-config-next` with core-web-vitals and TypeScript rules)

## Architecture

- **App Router**: all routes live under `app/`. `layout.tsx` is the root layout; `page.tsx` is the home page.
- **Styling**: Tailwind CSS v4 via PostCSS (`@tailwindcss/postcss`). Theme tokens defined in `app/globals.css` using `@theme inline`. Supports light/dark mode via `prefers-color-scheme`.
- **Fonts**: Geist Sans and Geist Mono loaded via `next/font/google`, exposed as CSS variables `--font-geist-sans` and `--font-geist-mono`.
- **Path alias**: `@/*` maps to the project root (configured in `tsconfig.json`).
- **Package manager**: npm (lock file is `package-lock.json`).
