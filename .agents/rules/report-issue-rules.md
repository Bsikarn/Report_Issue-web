---
trigger: always_on
---

---
trigger: always_on
---

# 🛠️ Workspace Rules: Issue Tracker

## 🎨 1. Design System & Aesthetics
- **Color Palette:** - Background & Surface: `#EFF1F8` (Off-white/Light blue base).
  - Primary Action: `#0D6EFD` (Cobalt Blue) for buttons and active states.
  - Text: `#0B2240` (Navy) for headings, `#8A97B0` (Muted Blue-Gray) for secondary text.
  - Shadows: `#FFFFFF` (Light source) and `#C5C8D4` (Dark shadow) for depth.
- **Visual Style:** - **Neumorphism:** Strictly use soft depth shadows, elevated component cards, and sunken input fields (inset shadows).
  - **Shape:** Rounded corners everywhere (`12px` to `32px` for cards, `50px` for pill tags).
- **Typography:** Use 'Poppins' for Headings/Labels and 'DM Sans' for Body text.
- **Icons:** Use minimal inline SVGs. Avoid heavy icon libraries.

## 🛠️ 2. Tech Stack & Frameworks
- **Frontend:** Pure HTML5, Vanilla CSS3, and Vanilla JavaScript (ES6+).
- **Backend:** Django (Python).
- **Prohibited:** STRICTLY NO external CSS frameworks (No Tailwind, No Bootstrap) and NO JavaScript frameworks (No React, No Vue). Stick to Vanilla.

## 🗄️ 3. Architecture & Django Standards
- **Static Files:** All CSS and JS files must be stored in the `static/` directory and loaded using `{% load static %}` in templates.
- **Templates:** Use Django Template Language (DTL) for rendering dynamic content in HTML files located in the `templates/` directory.
- **Separation of Concerns:** Keep logic in `script.js`, styling in `style.css`, and structure in `index.html`. Do not use inline styles unless absolutely necessary for dynamic JS calculations.

## 📸 4. Specific Feature Rules
- **Dynamic Filtering:** The issue feed must dynamically filter based on three location variables (Building, Floor, Room) using Vanilla JavaScript arrays and DOM manipulation.
- **Validation:** Empty form submissions must trigger a red inset shadow (`box-shadow: inset... rgba(239,68,68,.2)`) on the respective fields instead of default browser alerts.
- **Feedback:** Use custom bottom-center Toast notifications for success/error messages with smooth CSS transitions.

## 🤖 5. AI Agent Workflow (Integrated with Global Rules)
- **Code Generation:** When generating frontend code, utilize the established CSS variables (`var(--bg)`, `var(--blue)`, `var(--neu-lg)`, etc.) to maintain the Neumorphic theme.
- **Context Awareness:** Understand that this is a Django monolith. Do not suggest API endpoints (like Next.js/Express) unless explicitly asked to build Django REST Framework views.
- **Language:** While this file and code variables are in English, all AI chat responses and explanations must be in **Thai (ภาษาไทย)**.