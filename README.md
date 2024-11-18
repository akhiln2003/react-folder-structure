# Advanced React Project Structure

## 🎯 Overview
A modern, scalable, and maintainable folder structure for enterprise-level React applications. This structure follows feature-first architecture and supports TypeScript, testing, and component isolation.

## 📁 Folder Structure

```bash
src/
├── assets/                     # Static assets
│   ├── images/                # Image files
│   ├── icons/                 # Icon files
│   ├── fonts/                 # Font files
│   └── locales/              # i18n translation files
│
├── components/
│   ├── common/               # Shared/reusable components
│   │   ├── Button/
│   │   │   ├── Button.tsx
│   │   │   ├── Button.test.tsx
│   │   │   ├── Button.styles.ts
│   │   │   └── index.ts
│   │   └── Modal/
│   ├── features/            # Feature-specific components
│   │   ├── Auth/
│   │   └── Dashboard/
│   └── layouts/            # Layout templates
│       ├── MainLayout/
│       └── AuthLayout/
│
├── config/                 # Configuration files
│   ├── environment.ts      # Environment variables
│   ├── constants.ts        # App constants
│   └── api.config.ts       # API configuration
│
├── hooks/                  # Custom React hooks
│   ├── common/            # Shared hooks
│   │   ├── useLocalStorage.ts
│   │   └── useFetch.ts
│   └── features/          # Feature-specific hooks
│       ├── useAuth.ts
│       └── useProfile.ts
│
├── pages/                 # Application pages
│   ├── public/           # Public access pages
│   │   ├── Home/
│   │   └── About/
│   └── protected/        # Authentication required pages
│       └── Dashboard/
│           ├── components/
│           ├── hooks/
│           ├── utils/
│           ├── types/
│           └── index.tsx
│
├── services/             # API and external services
│   ├── api/
│   │   ├── client.ts
│   │   ├── endpoints.ts
│   │   └── interceptors.ts
│   └── features/
│       ├── auth.service.ts
│       └── user.service.ts
│
├── store/               # State management
│   ├── features/       # Feature-based store modules
│   │   ├── auth/
│   │   └── user/
│   ├── hooks.ts
│   └── store.ts
│
├── styles/             # Styling and theming
│   ├── theme/         # Theme configurations
│   ├── foundations/   # Design system foundations
│   └── global.css     # Global styles
│
├── types/             # TypeScript type definitions
│   ├── common/       # Shared types
│   └── features/     # Feature-specific types
│
├── utils/            # Utility functions
│   ├── common/      # Shared utilities
│   └── features/    # Feature-specific utilities
│
├── routes/          # Routing configuration
├── contexts/        # React Context providers
└── lib/            # Third-party library configs
```

## 📚 Directory Details

### `assets/`
- `images/`: Application images and photos
- `icons/`: SVG and other icon files
- `fonts/`: Custom font files
- `locales/`: Internationalization translation files

### `components/`
- `common/`: Reusable components used across features
  - Each component has its own folder with:
    - Component file (`.tsx`)
    - Test file (`.test.tsx`)
    - Styles file (`.styles.ts`)
    - Index file for clean exports
- `features/`: Feature-specific components
- `layouts/`: Page layout templates

### `config/`
- Environment configurations
- API settings
- Constants and app-wide configurations

### `hooks/`
- `common/`: Shared custom hooks
- `features/`: Feature-specific custom hooks

### `pages/`
- `public/`: Publicly accessible pages
- `protected/`: Authentication-required pages
  - Each page can have its own:
    - Components
    - Hooks
    - Utils
    - Types

### `services/`
- API client configuration
- Service implementations
- API interceptors
- Feature-specific services

### `store/`
- Redux/state management setup
- Feature-based store organization
- Custom store hooks
- Selectors and actions

### `styles/`
- Theme configuration
- Design tokens
- Global styles
- CSS foundations

### `types/`
- TypeScript interfaces
- Type definitions
- Shared types
- Feature-specific types

### `utils/`
- Helper functions
- Formatters
- Validators
- Feature-specific utilities

### `routes/`
- Route configurations
- Route guards
- Navigation logic

### `contexts/`
- React Context providers
- Global state management

### `lib/`
- Third-party library configurations
- Service initializations

## 🚀 Best Practices

1. **Component Structure**
```typescript
// index.ts
export { default } from './ComponentName';

// ComponentName.tsx
import { FC } from 'react';
import * as S from './ComponentName.styles';

interface Props {
  // props interface
}

const ComponentName: FC<Props> = ({ }) => {
  return (
    // component JSX
  );
};

export default ComponentName;

// ComponentName.styles.ts
import styled from 'styled-components';

export const Container = styled.div`
  // styles
`;
```

2. **Feature Organization**
- Keep related code together
- Each feature should be independent
- Share common code through common/ directories

3. **Type Safety**
- Use TypeScript for all files
- Create comprehensive interfaces
- Leverage type inference

4. **Testing**
- Co-locate tests with components
- Use meaningful test descriptions
- Follow AAA pattern (Arrange, Act, Assert)

