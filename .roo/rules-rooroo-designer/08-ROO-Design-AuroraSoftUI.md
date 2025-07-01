# 08-Design-AuroraSoftUI: "Aurora Soft UI" Design System

## 1. Design Philosophy

**Aurora Soft UI** is a modern, clean, and approachable design language. Its core is to create a clear, comfortable, and engaging digital environment for users through soft visual elements and intuitive interactions.

### Core Principles:
- **Clarity & Simplicity:** Use distraction-free layouts and generous whitespace to make core content and functions immediately clear.
- **Soft & Approachable:** Employ large border radii, smooth gradients, and soft shadows to create a friendly, stress-free visual experience.
- **Depth & Hierarchy:** Use shadows and scaling to subtly build visual hierarchy among interface elements, guiding user attention.
- **Vibrant Functionalism:** Utilize a set of bright, vibrant functional colors to clearly communicate states, feedback, and actionable items.
- **Playful Details:** Appropriately incorporate emojis or micro-interactions to enhance emotional engagement and bring the interface to life.

## 2. Design Tokens

Design tokens are the foundation for building the interface, ensuring global visual consistency.

### 2.1. Color System

- **Background:**
  - `bg-gradient-to-br from-slate-100 to-purple-100`

- **Primary Palette:**
  - `white`: `#ffffff` (for cards and core content backgrounds)
  - `gray-900`: `#111827` (for main titles and high-contrast text)
  - `gray-600`: `#4b5563` (for subtitles and descriptive text)

- **Functional Palette:**
  - **Accent/Selected:**
    - `red-400`: `#f87171` (border)
    - `red-50`: `#fef2f2` (background)
    - `red-500`: `#ef4444` (text/icon)
  - **Warning:**
    - `yellow-400`: `#fbbf24` (border)
    - `yellow-50`: `#fffbeb` (background)
    - `yellow-700`: `#b45309` (text)
  - **Success/Result:**
    - `teal-400`: `#2dd4bf` (border)
    - `teal-50`: `#f0fdfa` (background)

- **Button Palette:**
  - `Primary`: `bg-gray-900`, hover `bg-gray-800`
  - `Retry`: `bg-red-500`, hover `bg-red-600`
  - `Save`: `bg-teal-500`, hover `bg-teal-600`
  - `Share`: `bg-purple-500`, hover `bg-purple-600`

### 2.2. Typography System

- **Scale:**
  - `text-4xl` (36px): Main title
  - `text-3xl` (30px): Result title
  - `text-lg` (18px): Subtitle, section title
  - `text-base` (16px): Body text
  - `text-sm` (14px): Descriptive text
- **Weight:**
  - `font-bold` (700): Main title
  - `font-semibold` (600): Section title
  - `font-medium` (500): Button text
  - `font-normal` (400): Body text

### 2.3. Spacing System

- **Base unit:** `4px`
- **Component spacing:** `mb-8` (32px), `gap-4` (16px)
- **Content padding:** `p-8` (32px), `p-4` (16px), `p-12` (48px)
- **Button padding:** `px-6 py-3` (24px, 12px)

### 2.4. Radius System

- `rounded-3xl` (24px): Main container
- `rounded-2xl` (16px): Result card
- `rounded-xl` (12px): Buttons, selector cards
- `rounded-lg` (8px): Input fields

### 2.5. Shadow System

- `shadow-xl`: `0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1)` (for main cards, creates floating effect)
- `shadow-lg`: `0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1)` (for hover states)

## 3. Component Blueprints

### 3.1. Main Card
- **Style:** `bg-white rounded-3xl shadow-xl`
- **Description:** Floating card for core content, serves as the focal point of the interface.

### 3.2. Buttons
- **General style:** `rounded-xl font-medium transition-colors`
- **Primary button:** Dark background, white text, used for final or main actions.
- **Functional buttons:** Colored background, white text, used for specific contextual actions (e.g., retry, save).

### 3.3. Selectors
- **Style:** `border-2 rounded-xl p-4 cursor-pointer`
- **Selected state:** Uses accent color (red) for border and background, with a clear icon (✓).
- **Unselected state:** Uses neutral gray border, border color deepens on hover.

### 3.4. Alerts
- **Style:** `bg-yellow-50 border-l-4 border-yellow-400 p-4`
- **Description:** Prominent color bar on the left and warning icon, used to convey important information.

### 3.5. Upload Area
- **Style:** `border-2 border-dashed border-gray-300 rounded-xl p-12 text-center`
- **Description:** Dashed border and generous whitespace clearly indicate an interactive drag-and-drop area.

## 4. Iconography & Animation

- **Icon system:** Prefer semantic, cross-platform **Emoji** as icons to enhance approachability.
  - `😊`, `⚠️`, `📤`, `📁`, `🔄`, `💾`, `🔗`, `👍`, `👎`
- **Animation:**
  - **Transition effects:** `transition-colors duration-200` for all interactive elements, providing smooth visual feedback.
  - **Loading state:** Use `animate-spin` for a simple loading animation.

## 5. Accessibility

- **Color contrast:** Ensure all text and background colors meet WCAG 2.1 AA standards.
- **Keyboard navigation:** All interactive elements must be accessible via keyboard.
- **Focus state:** Use clear `focus:ring` styles to indicate the current focus position.
- **ARIA:** Add necessary `role` and `aria-*` attributes to non-semantic HTML elements.

## 6. Usage Guidelines

### 6.1. Color Usage Principles
- **Primary palette:** Used for the foundational framework of the interface, such as backgrounds and main text.
- **Functional colors:** Strictly used to convey specific states (e.g., selected, warning, success), maintaining clear semantics.
- **Button colors:** Guide users to perform key actions; color should match the importance of the action.

### 6.2. Spacing Usage Principles
- **Consistency:** Strictly follow defined spacing units; avoid arbitrary magic numbers to ensure harmonious and rhythmic layouts.
- **Breathing space:** Use larger spacing (e.g., `mb-8`) between components and content blocks to provide visual breathing room.

### 6.3. Radius Usage Principles
- **Hierarchy:** The size of the border radius should relate to the importance or size of the element. The largest radius (`rounded-3xl`) is for the outermost container, decreasing for inner components.
- **Consistency:** Similar components (e.g., all buttons) should use the same radius value.