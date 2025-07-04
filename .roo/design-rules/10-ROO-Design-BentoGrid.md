# Bento Grid Design System

## Core Design Philosophy

The Bento Grid system creates elegant, data-rich layouts inspired by Japanese bento boxes and Apple's product pages. It emphasizes visual hierarchy through varied card sizes, strategic use of gradients, and clear typography to present complex information in digestible, scannable formats. Perfect for dashboards, product showcases, and content-heavy interfaces.

## 1. Design Principles

### 1.1 Structured Flexibility
- Asymmetric grid system with intentional variety in card sizes
- Consistent 20px border radius (`rounded-[20px]`) for visual cohesion
- Strategic use of whitespace with 4-6px base spacing (`gap-4` to `gap-6`)
- Clear content hierarchy through size and positioning
- Modular approach allowing for easy rearrangement

### 1.2 Visual Rhythm
- Balanced composition with varied card dimensions
- Consistent spacing between all grid elements
- Purposeful use of gradient accents for emphasis
- Clean, minimal aesthetic with focus on content
- Subtle depth through shadows and elevation

### 1.3 Data-Driven Design
- Typography optimized for scanning and comprehension
- Color-coded information for quick identification
- Progressive disclosure of detailed information
- Visual weight assigned based on content importance
- Clear information architecture

## 2. Color System

### 2.1 Base Palette
- **Primary Background**: `white` (#ffffff)
- **Secondary Background**: `slate-50` (#f8fafc)
- **Tertiary Background**: `gray-50` (#f9fafb)
- **Page Background**: `gray-100` (#f3f4f6)

### 2.2 Accent Gradient System
- **Primary Gradient**: `from-[#C084FC] to-[#7E22CE]` (purple spectrum)
- **Secondary Gradient**: `from-[#60A5FA] to-[#3B82F6]` (blue spectrum)
- **Tertiary Gradient**: `from-[#34D399] to-[#10B981]` (green spectrum)
- **Warm Gradient**: `from-[#F59E0B] to-[#D97706]` (amber spectrum)

### 2.3 Typography Colors
- **Primary Text**: `gray-900` (#111827)
- **Secondary Text**: `gray-600` (#4b5563)
- **Muted Text**: `gray-400` (#9ca3af)
- **Accent Text**: Uses gradient colors for emphasis
- **Inverse Text**: `white` (#ffffff) on dark backgrounds

### 2.4 Functional Colors
- **Success**: `emerald-600` (#059669)
- **Warning**: `amber-600` (#d97706)
- **Error**: `red-600` (#dc2626)
- **Info**: `blue-600` (#2563eb)
- **Neutral**: `gray-600` (#4b5563)

## 3. Typography System

### 3.1 Font Stack
- **Primary**: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif
- **Fallback**: system-ui, sans-serif

### 3.2 Type Scale & Hierarchy
- **Hero/Key Data**: `text-4xl lg:text-5xl font-bold` (36px/48px)
- **Display**: `text-3xl lg:text-4xl font-bold` (30px/36px)
- **Title**: `text-2xl font-bold` (24px)
- **Card Title**: `text-xl font-semibold` (20px)
- **Subtitle**: `text-lg font-medium` (18px)
- **Body**: `text-base font-normal` (16px)
- **Small Body**: `text-sm font-normal` (14px)
- **Caption**: `text-xs font-medium` (12px)

### 3.3 Gradient Typography
- **Hero Text**: `bg-gradient-to-r from-[#C084FC] to-[#7E22CE] bg-clip-text text-transparent`
- **Accent Numbers**: `bg-gradient-to-r from-[#60A5FA] to-[#3B82F6] bg-clip-text text-transparent`
- **Key Metrics**: `bg-gradient-to-r from-[#34D399] to-[#10B981] bg-clip-text text-transparent`

### 3.4 Line Heights
- **Display Text**: `leading-tight` (1.25)
- **UI Text**: `leading-normal` (1.5)
- **Body Text**: `leading-relaxed` (1.625)
- **Compact Text**: `leading-none` (1)

## 4. Layout System

### 4.1 Grid Structure
- **Base Grid**: CSS Grid with `grid-template-columns: repeat(auto-fit, minmax(300px, 1fr))`
- **Large Screens**: `grid-template-columns: repeat(4, 1fr)`
- **Medium Screens**: `grid-template-columns: repeat(2, 1fr)`
- **Small Screens**: `grid-template-columns: 1fr`
- **Gap**: `gap-4` (16px) standard, `gap-6` (24px) for spacious layouts

### 4.2 Card Sizing Patterns
- **Single Unit**: `grid-column: span 1 / span 1`
- **Double Width**: `grid-column: span 2 / span 2`
- **Triple Width**: `grid-column: span 3 / span 3`
- **Full Width**: `grid-column: span 4 / span 4`
- **Tall Cards**: `grid-row: span 2 / span 2`
- **Feature Cards**: `grid-column: span 2; grid-row: span 2`

### 4.3 Container System
- **Page Container**: `max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`
- **Section Container**: `max-w-6xl mx-auto px-4`
- **Narrow Container**: `max-w-4xl mx-auto px-4`
- **Grid Container**: `w-full max-w-none`

### 4.4 Breakpoints
- **Mobile**: < 640px (single column)
- **Tablet**: 640px - 1023px (2 columns)
- **Desktop**: 1024px - 1279px (3-4 columns)
- **Large**: ≥ 1280px (4+ columns)

## 5. Component Library

### 5.1 Card Foundation
- **Base Card**: `bg-white rounded-[20px] shadow-md overflow-hidden`
- **Interactive Card**: `hover:-translate-y-1 hover:shadow-lg transition-all duration-200 cursor-pointer`
- **Feature Card**: `bg-white rounded-[20px] shadow-lg p-6 relative overflow-hidden`
- **Compact Card**: `bg-white rounded-[20px] shadow-sm p-4`

### 5.2 Card Variants
- **Data Card**: Focus on large numbers and metrics
- **Feature Card**: Hero content with imagery
- **List Card**: Structured information in lists
- **Chart Card**: Data visualization container
- **CTA Card**: Action-oriented with buttons
- **Media Card**: Image/video focused

### 5.3 Card Content Structure
- **Header**: `flex items-center justify-between mb-4`
- **Title**: `text-xl font-semibold text-gray-900 mb-2`
- **Subtitle**: `text-sm text-gray-600 mb-4`
- **Body**: `text-base text-gray-700 leading-relaxed`
- **Footer**: `flex items-center justify-between mt-4 pt-4 border-t border-gray-100`

### 5.4 Navigation Elements
- **Breadcrumbs**: `text-sm text-gray-500 mb-6`
- **Tabs**: `border-b border-gray-200 mb-6`
- **Pagination**: `flex justify-center mt-8`
- **Filters**: `flex flex-wrap gap-2 mb-6`

### 5.5 Data Display
- **Metric Cards**: Large numbers with context
- **Progress Bars**: `bg-gray-200 rounded-full overflow-hidden`
- **Status Indicators**: Colored dots or badges
- **Charts**: Integrated data visualization
- **Tables**: Responsive table layouts within cards

### 5.6 Interactive Elements
- **Buttons**: `rounded-lg px-4 py-2 font-medium transition-colors`
- **Links**: `text-blue-600 hover:text-blue-800 font-medium`
- **Tags**: `rounded-full bg-purple-100 text-purple-800 px-2 py-0.5 text-xs font-medium`
- **Badges**: `rounded-full bg-gray-100 text-gray-600 px-2 py-1 text-xs`

## 6. Content Patterns

### 6.1 Hero Section
- **Layout**: Full-width card with gradient background
- **Content**: Large headline with supporting text
- **Position**: Top of grid, spans full width
- **Style**: `bg-gradient-to-r from-[#C084FC] to-[#7E22CE] text-white`

### 6.2 Metric Dashboard
- **Layout**: Grid of metric cards with varying sizes
- **Content**: Key numbers, trends, and comparisons
- **Hierarchy**: Most important metrics get larger cards
- **Style**: Clean numbers with contextual information

### 6.3 Feature Showcase
- **Layout**: Mixed-size cards highlighting key features
- **Content**: Feature descriptions with supporting visuals
- **Variation**: Some cards span multiple columns/rows
- **Style**: Balanced composition with visual variety

### 6.4 Product Specifications
- **Layout**: Organized grid of specification cards
- **Content**: Technical details, features, and comparisons
- **Grouping**: Related specs grouped together
- **Style**: Clean, scannable information design

### 6.5 Content Library
- **Layout**: Uniform cards in flexible grid
- **Content**: Articles, resources, tools, or media
- **Filtering**: Category-based organization
- **Style**: Consistent card design with clear hierarchy

## 7. Responsive Behavior

### 7.1 Mobile Strategy
- **Layout**: Single column stack
- **Card Sizes**: All cards full width
- **Spacing**: Reduced gaps (`gap-4` to `gap-3`)
- **Typography**: Smaller text sizes
- **Touch**: Minimum 44px touch targets

### 7.2 Tablet Optimization
- **Layout**: 2-column grid
- **Card Sizes**: Some cards span both columns
- **Spacing**: Standard gaps (`gap-4` to `gap-6`)
- **Typography**: Medium text sizes
- **Interaction**: Hover effects enabled

### 7.3 Desktop Experience
- **Layout**: Full grid system (3-4 columns)
- **Card Sizes**: Full variety of card sizes
- **Spacing**: Generous gaps (`gap-6` to `gap-8`)
- **Typography**: Full text scale
- **Interaction**: All hover and micro-interactions

### 7.4 Large Screen Optimization
- **Layout**: Extended grid (4+ columns)
- **Card Sizes**: More complex arrangements
- **Spacing**: Maximum whitespace
- **Typography**: Largest text sizes
- **Content**: Additional details and features

## 8. Interaction States

### 8.1 Hover Effects
- **Cards**: `hover:-translate-y-1 hover:shadow-lg transition-all duration-200`
- **Buttons**: `hover:bg-opacity-90 transition-colors duration-150`
- **Links**: `hover:text-blue-800 transition-colors duration-150`
- **Interactive Elements**: Scale and shadow changes

### 8.2 Focus States
- **Cards**: `focus:ring-2 focus:ring-blue-500 focus:ring-offset-2`
- **Buttons**: `focus:ring-2 focus:ring-offset-2 focus:ring-current`
- **Links**: `focus:ring-2 focus:ring-blue-500 focus:ring-offset-1`

### 8.3 Active States
- **Cards**: `active:scale-98 transition-transform duration-100`
- **Buttons**: `active:scale-95 transition-transform duration-100`
- **Interactive Elements**: Subtle press effect

### 8.4 Loading States
- **Cards**: Skeleton loading with pulse animation
- **Content**: `animate-pulse bg-gray-200 rounded`
- **Images**: Placeholder with loading indicator

## 9. Visual Hierarchy

### 9.1 Size Hierarchy
- **Primary**: Large cards (2x2 or 2x1) for key content
- **Secondary**: Medium cards (1x2 or 2x1) for important content
- **Tertiary**: Standard cards (1x1) for regular content
- **Supporting**: Small cards for supplementary information

### 9.2 Color Hierarchy
- **Primary**: Gradient backgrounds for key content
- **Secondary**: Colored accents for important elements
- **Tertiary**: Neutral backgrounds with colored details
- **Supporting**: Minimal color for background content

### 9.3 Typography Hierarchy
- **Level 1**: Hero text with gradients
- **Level 2**: Large bold text for key metrics
- **Level 3**: Medium semibold for card titles
- **Level 4**: Regular text for body content
- **Level 5**: Small text for supporting details

## 10. Accessibility Standards

### 10.1 Color & Contrast
- **Minimum Contrast**: 4.5:1 for normal text
- **Large Text**: 3:1 for text 18px+ or 14px+ bold
- **Gradient Text**: Ensure sufficient contrast across gradient
- **Color Coding**: Never rely solely on color for meaning

### 10.2 Navigation
- **Keyboard**: All interactive elements keyboard accessible
- **Tab Order**: Logical reading order through grid
- **Skip Links**: Ability to skip to main content
- **Focus Management**: Clear focus indicators

### 10.3 Screen Reader Support
- **Semantic HTML**: Proper heading hierarchy
- **ARIA Labels**: Descriptive labels for cards
- **Alt Text**: Meaningful descriptions for images
- **Landmarks**: Clear page structure

### 10.4 Responsive Accessibility
- **Mobile**: Easy thumb navigation
- **Touch Targets**: Minimum 44px interactive areas
- **Zoom**: Content readable at 200% zoom
- **Orientation**: Support both portrait and landscape

This Bento Grid system creates sophisticated, information-rich layouts that scale beautifully across devices while maintaining excellent usability and accessibility standards.