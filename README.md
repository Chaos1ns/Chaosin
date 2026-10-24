# JustRemember Health

A lightweight health tracking, medication reminder, and medical history management web application for patients, caregivers, and families.

A user logs medications, appointments, vital signs, and daily health notes in seconds. Caregivers get a unified dashboard to monitor loved ones, track schedules, and receive missed-dose alerts.

No heavy apps to install. Everything runs in the browser, on a phone or on a laptop.

---

## Table of contents

- [Why it exists](#why-it-exists)
- [Features](#features)
- [Interface](#interface)
- [Tech stack](#tech-stack)
- [Project structure](#project-structure)
- [Getting started](#getting-started)
- [Roles](#roles)
- [How the data is protected](#how-the-data-is-protected)
- [Deployment](#deployment)
- [Pricing](#pricing)
- [Credits](#credits)

---

## Why it exists

Patients and elderly individuals often miss medications or struggle to keep track of complex medical schedules across multiple doctors. Traditional paper notebooks get lost, complex medical apps are hard to navigate for seniors, and family caregivers lack a centralized way to stay updated remotely.

JustRemember Health replaces these challenges with an intuitive browser-based interface, automated reminders, and a shared family timeline.

## Features

### For the Patient / User

| Area | What it does |
|---|---|
| Medication Schedule | Clear daily visual checklist of pills, dosages, and times to take them |
| Quick Log | One-tap confirmation when a medication is taken or skipped |
| Reminders | Browser and push notifications for upcoming medication doses |

### For the Caregiver / Family

| Area | What it does |
|---|---|
| Unified Dashboard | Overview of loved ones' daily compliance and health status |
| Alerts | Instant notification if a scheduled medication is missed |
| Appointment Calendar | Shared doctor visits, check-ups, and medication refill schedules |
| Notes & History | Secure log of symptoms, doctor feedback, and dietary notes |

### For the Administrator

- Platform-wide statistics: active users, total logs, system health
- User account management and support tools

## Interface

**Four appearance themes.** Clean designs with high-contrast color palettes designed for readability across all age groups.

| Theme | Look |
|---|---|
| Clinical | Clean medical white, crisp blue accents, high legibility |
| Calm | Soft pastel green and warm earth tones for reduced eye strain |
| Night | Dark mode optimized for evening use in low light |
| High Contrast | Maximum contrast ratios for accessibility and visual clarity |

**Languages.** Multi-language support switchable at any time.

## Tech stack

- **React** with **TypeScript**
- **Supabase** — PostgreSQL database, authentication, and Row Level Security
- **lucide-react** for icons
Project structure
src/
App.tsx — entry point: routing, roles, and layout
index.tsx — React root
config.ts — Supabase configuration and public URL
supabaseClient.ts — Supabase connection
types.ts — shared data types and interfaces
utils.ts — formatting and helper utilities
styles.css — custom styling and theme variables
components/ — shared UI elements and modals
screens/
Auth.tsx — sign-in, sign-up, password recovery
Dashboard.tsx — patient and caregiver home views
Medications.tsx — medication tracker and schedule
Vitals.tsx — health metrics and charts
Settings.tsx — profile, themes, and notifications
Getting started
1. Database
1. Create a project at supabase.com.
2. Run the database schema initialization script to set up tables, triggers, and security policies.
2. Configuration
Fill in your configuration keys in src/config.ts:
 Supabase Project URL
 Supabase Anon Key
3. Run it
Execute the following commands in your terminal:
npm install
npm start
The app opens at http://localhost:3000.
Roles
 Patient: Assigned automatically when signing up as a standard user on the platform.
 Caregiver: Assigned when linked via an invitation or shared family code.
 Administrator: Assigned via system administrator privileges.
How the data is protected
 Row Level Security (RLS) is enabled on all tables to ensure medical data is strictly private and accessible only to authorized individuals.
 Encrypted transport and secure token-based authentication via Supabase.
Deployment
Deploys seamlessly to platforms like Netlify or Vercel.
 Build command: npm run build
 Publish directory: build or dist
Pricing
 Free ($0 / forever): Includes basic medication reminders and personal health log.
 Family ($9.99 / month): Includes multi-caregiver support, unlimited reminders, and vitals history.
 Clinical (Custom): Includes multi-patient management for small care practices.
Credits
Bolt AI
