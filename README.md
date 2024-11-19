# React Project Folder Structure Guide

## 📋 Overview
A comprehensive and scalable folder structure for React applications. This structure focuses on maintainability, scalability, and clear separation of concerns.

## 📁 Root Structure
```bash
src/
├── assets/              # Static assets (images, fonts, styles)
├── components/          # Shared components
├── features/           # Feature-based modules
├── hooks/              # Custom React hooks
├── services/           # API and services
├── store/              # State management
├── utils/              # Utility functions
├── pages/              # Application pages
├── routes/             # Routing configuration
├── config/             # App configuration
├── types/              # TypeScript definitions
├── App.tsx             # Root component
└── index.tsx           # Entry point
```

## 📂 Directory Details

### `assets/`
```bash
assets/
├── images/
│   ├── logos/          # Logo variations
│   ├── icons/          # Icon assets
│   └── backgrounds/    # Background images
├── fonts/
│   ├── roboto/         # Font family files
│   └── poppins/
└── styles/
    ├── global.css      # Global styles
    ├── variables.css   # CSS variables
    ├── animations.css  # Global animations
    └── themes/
        ├── light.css   # Light theme
        └── dark.css    # Dark theme
```

### `components/`
```bash
components/
├── common/             # Shared components
│   ├── Button/
│   │   ├── index.ts
│   │   ├── Button.tsx
│   │   ├── Button.test.tsx
│   │   ├── Button.stories.tsx
│   │   ├── Button.module.css
│   │   └── types.ts
│   ├── Input/
│   ├── Modal/
│   ├── Card/
│   ├── Table/
│   └── Form/
│       ├── TextField/
│       ├── Select/
│       ├── Checkbox/
│       └── RadioGroup/
└── layout/
    ├── Header/
    │   ├── index.ts
    │   ├── Header.tsx
    │   ├── components/
    │   │   ├── Navigation/
    │   │   └── UserMenu/
    │   └── styles.module.css
    ├── Footer/
    ├── Sidebar/
    └── PageWrapper/
```

### `features/`
```bash
features/
├── auth/              # Authentication feature
│   ├── components/
│   │   ├── LoginForm/
│   │   ├── RegisterForm/
│   │   └── ForgotPassword/
│   ├── services/
│   │   ├── authService.ts
│   │   └── authApi.ts
│   ├── hooks/
│   │   ├── useAuth.ts
│   │   └── useAuthForm.ts
│   ├── store/
│   │   ├── authSlice.ts
│   │   └── authSelectors.ts
│   └── types/
│       └── auth.types.ts
└── dashboard/         # Dashboard feature
    ├── components/
    │   ├── DashboardStats/
    │   ├── RecentActivity/
    │   └── Charts/
    ├── services/
    ├── hooks/
    └── types/
```

### `hooks/`
```bash
hooks/
├── useApi/
│   ├── index.ts
│   ├── useApi.ts
│   └── types.ts
├── useLocalStorage/
├── useDebounce/
└── useMediaQuery/
```

### `services/`
```bash
services/
├── api/
│   ├── client/
│   │   ├── index.ts
│   │   ├── axios.ts
│   │   └── interceptors.ts
│   ├── endpoints.ts
│   └── types/
│       └── api.types.ts
└── storage/
    ├── localStorage.ts
    └── sessionStorage.ts
```

### `store/`
```bash
store/
├── slices/
│   ├── user/
│   │   ├── userSlice.ts
│   │   └── userSelectors.ts
│   └── app/
│       ├── appSlice.ts
│       └── appSelectors.ts
├── middleware/
│   └── logger.ts
└── store.ts
```

### `utils/`
```bash
utils/
├── helpers/
│   ├── date.ts
│   ├── string.ts
│   ├── number.ts
│   └── validation.ts
├── constants/
│   ├── routes.ts
│   ├── config.ts
│   └── api.ts
└── types/
    ├── common.types.ts
    └── api.types.ts
```

### `pages/`
```bash
pages/
├── Home/
│   ├── index.tsx
│   ├── components/
│   └── styles.module.css
├── Dashboard/
│   ├── index.tsx
│   ├── components/
│   └── SubPages/
│       ├── Analytics/
│       └── Settings/
└── Profile/
```

### `routes/`
```bash
routes/
├── PrivateRoute.tsx      # Protected route wrapper
├── PublicRoute.tsx       # Public route wrapper
├── AppRoutes.tsx         # Main routing config
└── routeConfig.ts        # Route definitions
```

### `config/`
```bash
config/
├── env.ts               # Environment variables
├── theme.ts             # Theme configuration
├── i18n.ts             # Internationalization
└── constants.ts         # Global constants
```

### `types/`
```bash
types/
├── global.d.ts          # Global declarations
├── env.d.ts            # Environment types
└── styled.d.ts         # Style system types
```

## 📝 Key Principles

1. **Component Organization**
   - Common components are reusable across features
   - Layout components handle structural elements
   - Each component has its own directory with related files

2. **Feature-First Architecture**
   - Features contain all related code
   - Each feature is self-contained
   - Features can have their own components, services, and types

3. **Clear Separation of Concerns**
   - Services handle external communication
   - Hooks manage reusable logic
   - Utils contain helper functions
   - Types ensure consistency

4. **Page Organization**
   - Pages represent routes
   - Sub-pages handle nested routes
   - Page-specific components stay with their pages

5. **Asset Management**
   - Images are categorized by type
   - Styles are separated by scope
   - Themes are clearly defined

6. **Type Safety**
   - Global types in `/types`
   - Feature-specific types within features
   - Component types alongside components

This structure provides a scalable foundation for React applications of any size while maintaining clarity and organization.
