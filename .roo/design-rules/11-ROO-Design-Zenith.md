# Zenith Design System

## Core Design Principles

### 1. Clean & Minimal
- Generous whitespace with 4px base spacing system (`gap-4`, `gap-6`, `gap-8`)
- Soft rounded corners: `rounded-xl` (12px) for cards, `rounded-lg` (8px) for buttons
- Subtle shadows: `shadow-sm` default, `shadow-md` on hover, `shadow-lg` for modals
- Content-first approach with clear visual hierarchy
- Centered layouts with `max-width` constraints for optimal readability

### 2. Color System
- **Primary**: Amber scale (amber-50 to amber-900) with amber-500 as main CTA
- **Neutral**: Complete gray scale (gray-50 to gray-900) for text and backgrounds
- **Semantic**: 
  - Success: green-50 bg, green-600 text
  - Warning: yellow-50 bg, yellow-600 text  
  - Error: red-50 bg, red-600 text
  - Info: blue-50 bg, blue-600 text
- **Categorical Tags**: Soft pastel backgrounds with medium-weight text
  - Video: red-50/red-600
  - Audio: green-50/green-600
  - Tools: blue-50/blue-600
  - SEO: purple-50/purple-600

### 3. Typography
- **Font Stack**: Inter, system-ui, -apple-system, sans-serif
- **Scale**: 
  - Hero: text-4xl to text-6xl, font-bold
  - Headings: text-xl to text-3xl, font-semibold
  - Body: text-base, font-medium
  - Small: text-sm, font-normal
  - Micro: text-xs, font-medium
- **Line Height**: leading-tight for display, leading-normal for UI, leading-relaxed for body

### 4. Layout System
- **Container**: `max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`
- **Grid Patterns**:
  - 1-col mobile: `grid-cols-1`
  - 2-col tablet: `md:grid-cols-2`
  - 3-col desktop: `lg:grid-cols-3`
  - 4-col wide: `xl:grid-cols-4`
- **Spacing**: `gap-4` (16px) to `gap-8` (32px)
- **Breakpoints**: sm(640px), md(768px), lg(1024px), xl(1280px)

### 5. Component Library

#### Navigation
- **Header**: `bg-white border-b border-gray-200 sticky top-0`
- **Logo**: `text-xl font-bold text-gray-900`
- **Nav Links**: `text-gray-600 hover:text-gray-900 font-medium`
- **CTA Button**: Primary amber button style

#### Cards
- **Base**: `bg-white rounded-xl border border-gray-200 overflow-hidden`
- **Hover**: `hover:shadow-md hover:border-gray-300 transition-all duration-200`
- **Content**: `p-4` to `p-6` internal padding
- **Image**: `aspect-video` or `aspect-square` containers

#### Buttons
- **Primary**: `bg-amber-500 text-white rounded-lg px-5 py-2.5 font-semibold hover:bg-amber-600`
- **Secondary**: `bg-white border border-gray-300 text-gray-700 rounded-lg px-5 py-2.5 hover:bg-gray-50`
- **Ghost**: `text-gray-700 hover:text-gray-900 font-semibold`
- **Size Variants**: `px-3 py-1.5` (sm), `px-5 py-2.5` (md), `px-6 py-3` (lg)

#### Forms
- **Input**: `border border-gray-300 rounded-lg p-3 focus:border-amber-500 focus:ring-1 focus:ring-amber-500`
- **Label**: `text-sm font-medium text-gray-700 mb-1 block`
- **Error**: `border-red-500 focus:border-red-500 focus:ring-red-500`
- **Search**: Large with right-aligned search icon button

#### Tags & Badges
- **Default**: `bg-gray-50 text-gray-600 px-3 py-1.5 rounded-lg text-sm font-medium`
- **Active**: `bg-amber-50 text-amber-600 border border-amber-200`
- **Colored**: Use categorical color system
- **Count**: `bg-gray-100 text-gray-600 px-2 py-1 rounded text-xs`

#### Modals
- **Backdrop**: `fixed inset-0 bg-black bg-opacity-50 z-40`
- **Panel**: `bg-white rounded-xl shadow-lg p-6 max-w-md w-full z-50`
- **Close**: `absolute top-4 right-4 text-gray-400 hover:text-gray-600`

### 6. Interaction States
- **Hover**: 
  - Cards: `hover:shadow-md hover:border-gray-300`
  - Buttons: Color shift with `transition-colors duration-200`
  - Links: `hover:text-gray-900`
- **Focus**: 
  - Interactive elements: `focus:ring-2 focus:ring-amber-400 focus:ring-offset-2`
  - Inputs: `focus:border-amber-500 focus:ring-1 focus:ring-amber-500`
- **Active**: 
  - Buttons: `active:scale-95 transition-transform`
  - Cards: `active:scale-98`
- **Disabled**: `disabled:opacity-50 disabled:cursor-not-allowed`

### 7. Content Patterns
- **Hero Section**: Large centered text with search functionality
- **Feature Grid**: 3-column responsive grid with icon + text
- **Pricing Cards**: Highlighted popular option with feature lists
- **Tool Directory**: Grid layout with category filtering
- **Newsletter**: Prominent email capture with inline form
- **Footer**: Multi-column navigation with brand section

### 8. Responsive Behavior
- **Mobile-First**: Start with single column, expand upward
- **Breakpoint Strategy**: 
  - Mobile: Stack vertically, full-width elements
  - Tablet: 2-column grids, compact navigation
  - Desktop: 3-4 column grids, horizontal navigation
- **Touch Targets**: Minimum 44px for interactive elements
- **Typography**: Responsive text scaling with `sm:text-lg md:text-xl`

### 9. Accessibility Standards
- **Contrast**: 4.5:1 for normal text, 3:1 for large text
- **Focus Management**: Visible focus indicators, logical tab order
- **Keyboard Navigation**: Full functionality without mouse
- **Screen Readers**: Proper heading hierarchy, alt text, ARIA labels
- **Color Independence**: Don't rely solely on color for meaning

This system creates modern, clean interfaces with excellent usability across all device types and use cases.