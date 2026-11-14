# OmniRecall 🤖

> **Your Things. Your Memory. Always Within Reach.**

OmniRecall is an AI-powered personal and household intelligence platform designed to eliminate the mental clutter of everyday life. From mislaid car keys and seasonal gear to expiring warranties, vehicle service histories, family medical dates, and encrypted passwords, OmniRecall organizes everything your household owns and needs to remember—making it retrievable in seconds via natural conversation or instant voice search.

---

## 🎯 The Pain Points We Solve

Most families juggle crucial everyday information across fragmented notes, photo galleries, spreadsheets, and mental memory. This creates friction, lost time, and recurring frustration:

1. **"Where did I put that?" syndrome:**
   Misplaced tools, seasonal clothing, spare keys, cables, and sentimental items cost households hours of searching each year.
2. **Scattered household documentation:**
   Vehicle registration renewals, insurance policies, property deeds, appliance warranties, and serial numbers are buried across physical drawers and buried email attachments.
3. **Critical family dates & milestones:**
   Forgotten birthdays, anniversaries, passport expiration dates, and vaccination schedules.
4. **Credential & sensitive information sprawl:**
   Insecure password sharing over chat apps or sticky notes instead of zero-knowledge, encrypted storage.
5. **Slow, manual searching:**
   Typing specific keywords into traditional search bars fails when you only remember context (e.g., *"Where did I put the blue folder after we came back from the hospital?"*).

---

## ✨ Core Features

### 🎙️ OmniBot AI Companion & Voice Search
- **Context-Aware Assistant:** An animated mascot bot embedded throughout the application that answers natural language questions about your belongings, household history, and upcoming dates.
- **Voice Transcription:** One-tap voice search powered by server-side speech recognition—simply speak what you're looking for.
- **Private RLS-Gated Context:** The AI only knows and answers from records explicitly owned by the authenticated user.

### 🔍 Find My Things
- **Multi-Level Hierarchy:** Organize physical belongings by Place (e.g., *Garage*), Room, Container (e.g., *Top Left Shelf*), and Item.
- **Photo Attachments:** Visual memory cues with secure, private image storage.
- **Fuzzy & Semantic Retrieval:** Find items by title, category, tags, or description.

### 🏠 Personal & Household Modules
Ten dedicated record modules covering every aspect of household administration:
- 📄 **Documents:** Passports, IDs, contracts, policies, and file attachments.
- 🚗 **Vehicles:** Mileage logs, insurance renewals, service intervals, VIN records.
- 💎 **Assets:** High-value electronics, furniture, jewelry, and serial numbers for insurance claims.
- 🩺 **Health:** Prescriptions, medical contacts, blood types, and allergies (excluded from general search for maximum privacy).
- 💳 **Bills & Expenses:** Recurring bills, due dates, payment methods, and automated reminders.
- 🎫 **Memberships:** Gym passes, loyalty clubs, subscriptions, and expiration dates.
- ✈️ **Travel:** Itineraries, frequent flyer numbers, booking confirmations, packing checklists.
- 🛠️ **Tasks & Maintenance:** Filter changes, seasonal upkeep, contractor contacts.
- 🎓 **Education:** Student IDs, school schedules, tuition due dates, transcripts.
- 🚨 **Emergency Contacts:** Direct family lines, doctors, utility emergency hotlines.

### 🔐 Secure Password Vault
- **Client-Side Encryption:** Passwords and secrets are encrypted directly in the browser using Web Crypto before being stored, ensuring zero-knowledge security.

### 🎂 Important Dates & Occasions
- Dedicated calendar tracker for birthdays, anniversaries, and annual milestones with proactive alerts.

### 👥 Family & Household Profiles
- Create distinct profiles for household members with avatars, birthdates, contact info, and assigned belongings.

### 🎨 Apple-Inspired Liquid Glass UI
- Frosted translucent cards, subtle depth blurs, and calm atmospheric palette (`#f7f7f5` / `#1c1c1c` / `#5b7fa3`).
- Interactive 3D flip card landing authentication supporting Apple, Google, and Email sign-in.
- Light and dark themes tuned for reduced glare and clean readability.

---

## 🏗️ Architecture & Technology Stack

| Layer | Technology |
| :--- | :--- |
| **Framework** | [TanStack Start v1](https://tanstack.com/start) (Full-stack React 19, SSR, Edge runtime) |
| **Routing** | TanStack Router (file-based, type-safe routes) |
| **Styling** | [Tailwind CSS v4](https://tailwindcss.com/) & shadcn/ui primitives |
| **Backend & Database** | Lovable Cloud (PostgreSQL with Row Level Security, Supabase Auth & Storage) |
| **AI & Voice** | Lovable AI Gateway (LLM inference & Whisper speech-to-text) |
| **Payments** | [Paddle](https://www.paddle.com/) (Merchant of Record, 7-day trials, Pro tiers, webhook idempotency) |
| **Email Infrastructure** | Custom transactional domain (`notify.omnirecall.app`) for trial reminders |

---

## 🔒 Security & Privacy Model

- **Row Level Security (RLS):** Every database query is strictly scoped to the authenticated user's ID at the database engine level.
- **Client-Side Vault Encryption:** Sensitive credentials never leave the device in plain text; the server stores only encrypted payloads.
- **Fail-Closed Entitlements:** Server-enforced plan boundaries prevent unauthorized record creation and enforce combined saved-item limits across all household modules.

- 📄 License & Attribution
Proprietary — All rights reserved © OmniRecall.
Proudly created by Umair Bin Hassan (aka Umair Khan Wattoo) in Pakistan.
