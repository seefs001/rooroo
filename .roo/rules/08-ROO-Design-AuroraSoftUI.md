# 08-Design-AuroraSoftUI: "Aurora Soft UI" 官方设计系统

## 1. 设计哲学

**Aurora Soft UI** 是一套现代、简洁且富有亲和力的设计语言。其核心在于通过柔和的视觉元素和直观的交互，为用户创造一个清晰、舒适且引人入胜的数字环境。

### 核心原则:
- **清晰与简洁 (Clarity & Simplicity):** 采用无干扰的布局和充足的留白，让核心内容和功能一目了然。
- **柔和美学 (Soft & Approachable):** 广泛使用大圆角、平滑渐变和柔和阴影，营造出友好、无压力的视觉感受。
- **深度与层次 (Depth & Hierarchy):** 通过阴影和缩放，巧妙地构建界面元素的视觉层次，引导用户注意力。
- **多彩功能主义 (Vibrant Functionalism):** 使用一组明亮、充满活力的功能色，清晰地传达状态、反馈和可操作项。
- **趣味性细节 (Playful Details):** 适度融入 Emoji 或微交互等趣味元素，提升用户的情感体验，让界面充满生机。

## 2. 设计令牌 (Design Tokens)

设计令牌是构建界面的基础，确保了全局的视觉一致性。

### 2.1. 颜色系统 (Color System)

- **背景 (Background):**
  - `bg-gradient-to-br from-slate-100 to-purple-100`

- **主色调 (Primary Palette):**
  - `white`: `#ffffff` (用于卡片和核心内容背景)
  - `gray-900`: `#111827` (用于主标题和高对比度文本)
  - `gray-600`: `#4b5563` (用于副标题和描述性文本)

- **功能色 (Functional Palette):**
  - **Accent/Selected (强调/选中):**
    - `red-400`: `#f87171` (边框)
    - `red-50`: `#fef2f2` (背景)
    - `red-500`: `#ef4444` (文本/图标)
  - **Warning (警告):**
    - `yellow-400`: `#fbbf24` (边框)
    - `yellow-50`: `#fffbeb` (背景)
    - `yellow-700`: `#b45309` (文本)
  - **Success/Result (成功/结果):**
    - `teal-400`: `#2dd4bf` (边框)
    - `teal-50`: `#f0fdfa` (背景)

- **按钮色 (Button Palette):**
  - `Primary`: `bg-gray-900`, hover `bg-gray-800`
  - `Retry`: `bg-red-500`, hover `bg-red-600`
  - `Save`: `bg-teal-500`, hover `bg-teal-600`
  - `Share`: `bg-purple-500`, hover `bg-purple-600`

### 2.2. 字体系统 (Typography System)

- **字阶 (Scale):**
  - `text-4xl` (36px): 主标题
  - `text-3xl` (30px): 结果标题
  - `text-lg` (18px): 副标题, 区域标题
  - `text-base` (16px): 正文
  - `text-sm` (14px): 描述性文字
- **字重 (Weight):**
  - `font-bold` (700): 主标题
  - `font-semibold` (600): 区域标题
  - `font-medium` (500): 按钮文字
  - `font-normal` (400): 正文

### 2.3. 间距系统 (Spacing System)

- **基础单位:** `4px`
- **组件间距:** `mb-8` (32px), `gap-4` (16px)
- **内容内边距:** `p-8` (32px), `p-4` (16px), `p-12` (48px)
- **按钮内边距:** `px-6 py-3` (24px, 12px)

### 2.4. 圆角系统 (Radius System)

- `rounded-3xl` (24px): 主容器
- `rounded-2xl` (16px): 结果卡片
- `rounded-xl` (12px): 按钮, 选择卡片
- `rounded-lg` (8px): 输入框

### 2.5. 阴影系统 (Shadow System)

- `shadow-xl`: `0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1)` (用于主卡片，营造悬浮感)
- `shadow-lg`: `0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1)` (用于悬停状态)

## 3. 组件蓝图 (Component Blueprints)

### 3.1. 主卡片 (Main Card)
- **样式:** `bg-white rounded-3xl shadow-xl`
- **描述:** 承载核心内容的悬浮卡片，是界面的焦点。

### 3.2. 按钮 (Buttons)
- **通用样式:** `rounded-xl font-medium transition-colors`
- **主按钮:** 深色背景，白色文字，用于最终或主要操作。
- **功能按钮:** 彩色背景，白色文字，用于特定上下文操作 (如重试、保存)。

### 3.3. 选择器 (Selectors)
- **样式:** `border-2 rounded-xl p-4 cursor-pointer`
- **选中状态:** 使用强调色（红色）的边框和背景，并附有明确的图标（✓）。
- **未选中状态:** 使用中性灰色边框，悬停时边框颜色加深。

### 3.4. 提示/警告框 (Alerts)
- **样式:** `bg-yellow-50 border-l-4 border-yellow-400 p-4`
- **描述:** 左侧有明显的颜色条，并配有警告图标，用于传达重要提示信息。

### 3.5. 上传区域 (Upload Area)
- **样式:** `border-2 border-dashed border-gray-300 rounded-xl p-12 text-center`
- **描述:** 使用虚线边框和大面积留白，清晰地标示出可交互的拖放区域。

## 4. 图标与动画 (Iconography & Animation)

- **图标系统:** 优先使用语义化、跨平台一致的 **Emoji** 作为图标，以增强亲和力。
  - `😊`, `⚠️`, `📤`, `📁`, `🔄`, `💾`, `🔗`, `👍`, `👎`
- **动画:**
  - **过渡效果:** `transition-colors duration-200` 用于所有可交互元素，提供平滑的视觉反馈。
  - **加载状态:** 使用 `animate-spin` 实现简洁的加载动画。

## 5. 可访问性 (Accessibility)

- **颜色对比度:** 确保所有文本和背景色符合 WCAG 2.1 AA 标准。
- **键盘导航:** 所有交互元素必须可通过键盘访问。
- **焦点状态:** 使用清晰的 `focus:ring` 样式，明确指示当前焦点位置。
- **ARIA:** 为非语义化HTML元素添加必要的 `role` 和 `aria-*` 属性。

## 6. 使用指南 (Usage Guidelines)

### 6.1. 颜色使用原则
- **主色调**: 用于构建界面的基础框架，如背景和主要文本。
- **功能色**: 严格用于传达特定状态（如选中、警告、成功），保持其语义的明确性。
- **按钮色**: 用于引导用户执行关键操作，颜色应与操作的重要性相匹配。

### 6.2. 间距使用原则
- **一致性**: 严格遵循定义的间距单位，避免随意使用魔术数字，以保证布局的和谐与韵律。
- **呼吸感**: 在组件和内容块之间使用较大的间距（如 `mb-8`），为用户提供视觉上的喘息空间。

### 6.3. 圆角使用原则
- **层级关系**: 圆角大小应与元素的重要性或尺寸相关联。最大的圆角（`rounded-3xl`）用于最外层的容器，向内层组件递减。
- **一致性**: 同类组件（如所有按钮）应使用相同的圆角值。