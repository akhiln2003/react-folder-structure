# React Project Folder Structure Guide

## 📋 Overview
A comprehensive and scalable folder structure for React applications. This structure focuses on maintainability, scalability, and clear separation of concerns.

## 📁 Root Structure
```bash
src/
├── assets/
│   ├── images/
│   │   ├── logos/
│   │   ├── icons/
│   │   └── backgrounds/
│   ├── fonts/
│   │   ├── roboto/
│   │   └── poppins/
│   └── styles/
│       ├── global.css          # Global styles
│       ├── variables.css       # CSS variables
│       ├── animations.css      # Global animations
│       └── themes/
│           ├── light.css
│           └── dark.css
│
├── components/
│   ├── common/                 # Shared components
│   │   ├── Button/
│   │   │   ├── index.ts       # Export file
│   │   │   ├── Button.tsx     # Main component
│   │   │   ├── Button.test.tsx
│   │   │   ├── Button.stories.tsx  # Storybook stories
│   │   │   ├── Button.module.css
│   │   │   └── types.ts       # Component types
│   │   ├── Input/
│   │   ├── Modal/
│   │   ├── Card/
│   │   ├── Table/
│   │   └── Form/
│   │       ├── TextField/
│   │       ├── Select/
│   │       ├── Checkbox/
│   │       └── RadioGroup/
│   │
│   └── layout/
│       ├── Header/
│       │   ├── index.ts
│       │   ├── Header.tsx
│       │   ├── components/    # Header-specific components
│       │   │   ├── Navigation/
│       │   │   └── UserMenu/
│       │   └── styles.module.css
│       ├── Footer/
│       ├── Sidebar/
│       └── PageWrapper/
│
├── features/                   # Feature-based modules
│   ├── auth/
│   │   ├── components/
│   │   │   ├── LoginForm/
│   │   │   ├── RegisterForm/
│   │   │   └── ForgotPassword/
│   │   ├── services/
│   │   │   ├── authService.ts
│   │   │   └── authApi.ts
│   │   ├── hooks/
│   │   │   ├── useAuth.ts
│   │   │   └── useAuthForm.ts
│   │   ├── store/
│   │   │   ├── authSlice.ts
│   │   │   └── authSelectors.ts
│   │   └── types/
│   │       └── auth.types.ts
│   │
│   └── dashboard/
│       ├── components/
│       │   ├── DashboardStats/
│       │   ├── RecentActivity/
│       │   └── Charts/
│       ├── services/
│       ├── hooks/
│       └── types/
│
├── hooks/                      # Global custom hooks
│   ├── useApi/
│   │   ├── index.ts
│   │   ├── useApi.ts
│   │   └── types.ts
│   ├── useLocalStorage/
│   ├── useDebounce/
│   └── useMediaQuery/
│
├── services/
│   ├── api/
│   │   ├── client/
│   │   │   ├── index.ts
│   │   │   ├── axios.ts       # Axios instance setup
│   │   │   └── interceptors.ts
│   │   ├── endpoints.ts
│   │   └── types/
│   │       └── api.types.ts
│   └── storage/
│       ├── localStorage.ts
│       └── sessionStorage.ts
│
├── store/                      # State management
│   ├── slices/
│   │   ├── user/
│   │   │   ├── userSlice.ts
│   │   │   └── userSelectors.ts
│   │   └── app/
│   │       ├── appSlice.ts
│   │       └── appSelectors.ts
│   ├── middleware/
│   │   └── logger.ts
│   └── store.ts
│
├── utils/
│   ├── helpers/
│   │   ├── date.ts
│   │   ├── string.ts
│   │   ├── number.ts
│   │   └── validation.ts
│   ├── constants/
│   │   ├── routes.ts
│   │   ├── config.ts
│   │   └── api.ts
│   └── types/
│       ├── common.types.ts
│       └── api.types.ts
│
├── pages/
│   ├── Home/
│   │   ├── index.tsx
│   │   ├── components/        # Page-specific components
│   │   └── styles.module.css
│   ├── Dashboard/
│   │   ├── index.tsx
│   │   ├── components/
│   │   └── SubPages/
│   │       ├── Analytics/
│   │       └── Settings/
│   └── Profile/
│
├── routes/
│   ├── PrivateRoute.tsx
│   ├── PublicRoute.tsx
│   ├── AppRoutes.tsx          # Main routing configuration
│   └── routeConfig.ts         # Route definitions
│
├── config/
│   ├── env.ts                 # Environment variables
│   ├── theme.ts               # Theme configuration
│   ├── i18n.ts               # Internationalization config
│   └── constants.ts           # Global constants
│
├── types/
│   ├── global.d.ts            # Global type declarations
│   ├── env.d.ts              # Environment variables types
│   └── styled.d.ts           # Styled-components types
│
├── App.tsx
├── index.tsx
└── vite-env.d.ts             # If using Vite
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
