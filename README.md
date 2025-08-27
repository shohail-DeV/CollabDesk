# CollabDesk — Full‑Stack Jira‑Style Issue Tracker

> CollabDesk is an academic project built to simulate real‑world issue tracking scenarios used in customer support and software development teams. It mirrors workflows found in tools like JIRA, enabling practice in **ticket resolution**, **documentation**, and **SLA adherence**.

## Overview

* **What**: An issue‑tracking platform with ticketing, SLAs, comments, assignees, labels, and dashboards.
* **Why**: To provide students and early professionals a hands‑on environment for practicing collaborative workflows without enterprise license costs.
* **How**: Powered by **Next.js 14 App Router**, **React**, **Tailwind CSS**, **Prisma ORM**, **Neon Postgres**, **Clerk Authentication**, and **shadcn/ui**.

## Features

* Workspace & project onboarding
* Authentication via Clerk (sign‑in, sign‑up, onboarding)
* Ticket creation, updates, and resolution workflows
* Kanban board with drag‑and‑drop (Backlog, In‑Progress, Blocked, Done)
* Labels, priorities, assignees, due dates, attachments
* Comments and activity logs
* SLA timers and badges
* Filters, search, and analytics dashboard
* Role‑based access: owner, member, viewer
* Responsive UI built with shadcn/ui

## Tech Stack

* **Frontend**: Next.js 14, React 18, Tailwind CSS, shadcn/ui
* **Backend**: Server actions in Next.js
* **Database**: Neon Postgres with Prisma ORM
* **Auth**: Clerk (with Organizations enabled)
* **Deployment**: Vercel
* **Language/Tools**: TypeScript, ESLint, Prettier

## Getting Started

### Prerequisites

* Node.js ≥ 18.17
* pnpm (or npm/yarn)
* Neon Postgres account
* Clerk application

### Installation

```bash
git clone <your-repo-url> collabdesk
cd collabdesk
pnpm install
```

### Environment Variables

Create a `.env` file with:

```bash
DATABASE_URL="postgresql://<user>:<password>@<neon-host>/<db>?sslmode=require"

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="pk_..."
CLERK_SECRET_KEY="sk_..."

NEXT_PUBLIC_CLERK_SIGN_IN_URL="/sign-in"
NEXT_PUBLIC_CLERK_SIGN_UP_URL="/sign-up"
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL="/onboarding"
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL="/onboarding"
```

### Database Setup

```bash
pnpm prisma generate
pnpm prisma migrate dev --name init
pnpm prisma db seed # optional
```

### Run Locally

```bash
pnpm dev
# App runs at http://localhost:3000
```

## Deployment (Vercel Recommended)

1. Push repo to GitHub.
2. Import project in Vercel.
3. Add `.env` variables to Vercel Project Settings.
4. Run `prisma migrate deploy` during build.

## Roadmap

* Sprints & velocity tracking
* Slack/GitHub integrations
* Bulk edit & CSV import/export
* Custom SLAs per project
* Webhooks for automation

## License

MIT License — free to use and modify.

---

### Academic Context

This project was built as part of coursework to provide a real‑world simulation of issue‑tracking platforms. CollabDesk demonstrates workflows used by modern teams in **customer support** and **software development**, fostering practical exposure to collaboration and SLA‑driven processes.
