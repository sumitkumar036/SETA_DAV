# 🌟 Emotion Tracker (SETA_DAV)

> A beautiful, safe, and simple feelings portal designed for **D.A.V Public School** students to share their daily moods, coupled with a real-time analytics workspace for teachers and administration.

[Live Demo Deployed on GitHub Pages](https://sumitkumar.online/SETA_DAV/) 
<img width="1904" height="949" alt="image" src="https://github.com/user-attachments/assets/c7a32ac2-7347-4203-9c87-b3054c8f083d" />


---

## 🎨 System Preview & UI Design Philosophy

The application is built using a custom **Full-Bleed Responsive Layout Engine** via Tailwind CSS. 

* **Mobile First Context:** On small screens, cards seamlessly break out into a native **2px viewport gap** with sharp, continuous screen-edge alignments—perfectly optimized for smooth, distraction-free tapping on mobile devices and classroom tablets.
* **Desktop Centering Matrix:** On larger viewports, layout widths automatically scale up, safely centering into structured Glassmorphism bento grids (`max-w-xl`, `max-w-6xl`) with flowing animated morphing ambient background gradients.
* **Fluid Theme Engine:** Complete support for a high-vibrancy Dark Mode configured via hardware-accelerated CSS screen filters.

---

## ✨ Features

### 🧒 Student Check-In Workspace
* **5-Step Gamified Workflow:** Designed with oversized, kid-friendly actionable option cards.
  * **Step 1:** Roster Class Grade Selection.
  * **Step 2:** Student Identity Name Picker.
  * **Step 3:** Password/ID Masked Pin Verification.
  * **Step 4:** Vibrant Emoji Mood Spectrum Picker (`Very Happy` to `Angry/Anxious`).
  * **Step 5:** Contextual Reason Preset Cards (e.g., *Friends*, *Learning*, *Family*) + custom type-in input boxes.
* **Daily Star Rewards:** Celebratory end-sequence animation yielding virtual "+10 Daily Stars" to encourage daily mental wellness monitoring.

### 📊 Educator & Administrator Dashboard
* **Live Analysis Board:** Automatically tallies active connected user ratios matching current filtering timelines (`Today`, `1 Week`, `1 Month`).
* **Interactive Tooltip Mood Board:** Displays real-time aggregated bar chart trends of student states. Hovering over any mood color bar dynamically renders custom tooltips tracking exact student lists.
* **Granular Directory Filters:** Multi-variable dropdown matrix filters to isolate specific class roster records or specific flagged emotional trend updates.

---

## 🛠️ Tech Stack & Architecture

* **Frontend Framework:** React 18 (TypeScript / JSX)
* **Routing System:** React Router DOM v6 *(configured with dynamic repository base URL sub-directories for strict asset resolution on GitHub Pages)*
* **Styling Suite:** Tailwind CSS v3 + Tailwind Preflight Normalization + Lucide Icons (`react-icons/lu`)
* **State Management:** Zustand (Global State management tracking active sessions, credentials, and light/dark appearance modes)
* **Data Fetching:** TanStack React Query v5 *(utilizing query cache invalidation pipelines to pull down instant hot-reloads upon student submission updates)*

---

## 📁 Directory Structure Overview

```text
src/
├── api/             # Axiom/Fetch request interfaces (StudentService)
├── components/      # Global atomic reusable components
│   ├── Button.tsx
│   ├── Container.tsx
│   ├── FullBleedSection.tsx  👈 Core custom mobile responsive layout engine
│   └── InputField.tsx
├── hooks/           # TanStack data tracking hooks (useAppData, useAuth)
├── pages/           # High-level workspace view layout states
│   ├── AdminDashboard.tsx
│   ├── ForgotPasswordPage.tsx
│   ├── Home.tsx
│   ├── LoginPage.tsx
│   └── StudentCheckIn.tsx
├── store/           # Zustand global state wrappers (globalStore)
├── utils/           # Time calculation logic and static application constants
├── App.tsx          # Dynamic application shell and router layout
└── main.tsx         # Virtual DOM entry engine node
