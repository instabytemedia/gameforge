# GameForge

> Craft Games, Unite Community

GameForge is a premium platform where board game enthusiasts can design, play, and share their own games, leveraging AI-powered tools for game balancing and mechanics suggestions. It offers a vast library of user-generated games, fostering a community that collaborates and competes. By focusing on user-generated content and community engagement, GameForge creates a unique and constantly evolving experience.

## Features

- AI-assisted game design
- Community forums
- Game sharing and rating system

## Tech Stack

- **Framework:** Next.js 14 (App Router)
- **Database:** Supabase (PostgreSQL)
- **Auth:** Supabase Auth
- **Styling:** Tailwind CSS
- **Language:** TypeScript

## Getting Started

1. Clone this repository
2. Copy `.env.example` to `.env.local` and fill in your credentials
3. Run `npm install`
4. Run `npm run dev`

## Project Structure

```
├── app/                  # Next.js App Router pages
├── components/           # React components
├── lib/                  # Utilities and helpers
├── supabase/            # Database schema
└── INSTRUCTIONS.md      # Detailed build guide for AI assistants
```

## Database

This project uses 2 main entities:
- **Game**: A user-created board game
- **User**: A registered user

## Build Instructions

For detailed step-by-step build instructions, see [`INSTRUCTIONS.md`](./INSTRUCTIONS.md).

This file contains comprehensive guidance for building this project with AI coding assistants like Claude Code, Cursor, or Windsurf.

---

*Generated with [Claudery](https://claudery.io) - AI-powered blueprint generator*
