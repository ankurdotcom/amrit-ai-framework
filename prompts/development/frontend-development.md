# 🎨 FRONTEND DEVELOPMENT PROMPTS
*AI Prompts for Modern Frontend Implementation*

## 🚀 **REACT + TYPESCRIPT PROJECT SETUP**

```
ROLE: Senior Frontend Developer & UX Engineer

TASK: Create a complete React + TypeScript frontend application with modern best practices.

REQUIREMENTS: [Insert project requirements]

IMPLEMENTATION STEPS:

1. PROJECT INITIALIZATION:
```bash
npx create-react-app [project-name] --template typescript
cd [project-name]
npm install @reduxjs/toolkit react-redux
npm install @mui/material @emotion/react @emotion/styled
npm install react-router-dom @types/react-router-dom
npm install axios react-query
npm install @testing-library/react @testing-library/jest-dom
npm install eslint-config-prettier prettier
```

2. FOLDER STRUCTURE:
```
src/
├── components/           # Reusable UI components
│   ├── common/          # Generic components
│   ├── forms/           # Form components
│   └── layout/          # Layout components
├── pages/               # Page-level components
├── hooks/               # Custom React hooks
├── services/            # API service layer
├── store/               # Redux store configuration
├── types/               # TypeScript type definitions
├── utils/               # Utility functions
├── styles/              # Global styles and themes
└── __tests__/           # Test files
```

3. COMPONENT IMPLEMENTATION:
Create components following these patterns:

```typescript
// Component Template
import React from 'react';
import { styled } from '@mui/material/styles';

interface ComponentProps {
  // Define prop types
}

const StyledComponent = styled('div')(({ theme }) => ({
  // Styled component definition
}));

export const Component: React.FC<ComponentProps> = ({
  // Props destructuring
}) => {
  // Component logic
  
  return (
    <StyledComponent>
      {/* Component JSX */}
    </StyledComponent>
  );
};
```

4. STATE MANAGEMENT:
Implement Redux Toolkit store:

```typescript
// store/index.ts
import { configureStore } from '@reduxjs/toolkit';
import { authSlice } from './authSlice';
import { uiSlice } from './uiSlice';

export const store = configureStore({
  reducer: {
    auth: authSlice.reducer,
    ui: uiSlice.reducer,
  },
});

export type RootState = ReturnType<typeof store.getState>;
export type AppDispatch = typeof store.dispatch;
```

5. API INTEGRATION:
Create service layer:

```typescript
// services/api.ts
import axios from 'axios';

const api = axios.create({
  baseURL: process.env.REACT_APP_API_URL,
  timeout: 10000,
});

export const authService = {
  login: (credentials: LoginCredentials) => 
    api.post('/auth/login', credentials),
  logout: () => api.post('/auth/logout'),
};
```

6. TESTING STRATEGY:
Implement comprehensive testing:

```typescript
// Component.test.tsx
import { render, screen, fireEvent } from '@testing-library/react';
import { Component } from './Component';

describe('Component', () => {
  it('should render correctly', () => {
    render(<Component />);
    expect(screen.getByRole('button')).toBeInTheDocument();
  });
  
  it('should handle user interaction', () => {
    const handleClick = jest.fn();
    render(<Component onClick={handleClick} />);
    fireEvent.click(screen.getByRole('button'));
    expect(handleClick).toHaveBeenCalledTimes(1);
  });
});
```

QUALITY STANDARDS:
- TypeScript strict mode enabled
- ESLint + Prettier configuration
- 90%+ test coverage
- Accessibility compliance (WCAG 2.1)
- Performance optimization (lazy loading, memoization)
- Responsive design (mobile-first approach)
```

## 🎯 **COMPONENT DESIGN PROMPT**

```
ROLE: UI/UX Developer & Accessibility Expert

TASK: Design and implement reusable UI components with modern design principles.

COMPONENT REQUIREMENTS:
- Accessibility compliant (ARIA labels, keyboard navigation)
- Responsive design (mobile, tablet, desktop)
- Theme support (light/dark mode)
- TypeScript interfaces
- Comprehensive testing
- Storybook documentation

IMPLEMENTATION TEMPLATE:

```typescript
// Button Component Example
import React from 'react';
import { styled } from '@mui/material/styles';
import { Button as MuiButton, ButtonProps as MuiButtonProps } from '@mui/material';

interface CustomButtonProps extends MuiButtonProps {
  variant?: 'primary' | 'secondary' | 'danger';
  size?: 'small' | 'medium' | 'large';
  loading?: boolean;
  icon?: React.ReactNode;
}

const StyledButton = styled(MuiButton)<CustomButtonProps>(({ theme, variant }) => ({
  borderRadius: theme.spacing(1),
  textTransform: 'none',
  fontWeight: 500,
  ...(variant === 'primary' && {
    backgroundColor: theme.palette.primary.main,
    color: theme.palette.primary.contrastText,
    '&:hover': {
      backgroundColor: theme.palette.primary.dark,
    },
  }),
  ...(variant === 'danger' && {
    backgroundColor: theme.palette.error.main,
    color: theme.palette.error.contrastText,
    '&:hover': {
      backgroundColor: theme.palette.error.dark,
    },
  }),
}));

export const Button: React.FC<CustomButtonProps> = ({
  children,
  loading = false,
  icon,
  disabled,
  ...props
}) => {
  return (
    <StyledButton
      disabled={disabled || loading}
      startIcon={loading ? <CircularProgress size={16} /> : icon}
      {...props}
    >
      {children}
    </StyledButton>
  );
};

// Component tests
describe('Button', () => {
  it('should render with correct variant styles', () => {
    render(<Button variant="primary">Click me</Button>);
    const button = screen.getByRole('button');
    expect(button).toHaveClass('primary');
  });
  
  it('should show loading state', () => {
    render(<Button loading>Loading</Button>);
    expect(screen.getByRole('progressbar')).toBeInTheDocument();
  });
  
  it('should be accessible', () => {
    render(<Button aria-label="Submit form">Submit</Button>);
    expect(screen.getByLabelText('Submit form')).toBeInTheDocument();
  });
});
```

DESIGN SYSTEM INTEGRATION:
1. Create consistent spacing scale
2. Implement color palette with semantic naming
3. Define typography hierarchy
4. Establish component naming conventions
5. Document component usage patterns
```

## 🎨 **STYLING & THEMING PROMPT**

```
ROLE: UI Designer & Frontend Architect

TASK: Implement comprehensive theming system with modern CSS-in-JS patterns.

THEME IMPLEMENTATION:

```typescript
// theme/index.ts
import { createTheme, ThemeProvider } from '@mui/material/styles';

const baseTheme = {
  spacing: 8,
  typography: {
    fontFamily: '"Inter", "Roboto", "Helvetica", "Arial", sans-serif',
    h1: {
      fontSize: '2.5rem',
      fontWeight: 700,
      lineHeight: 1.2,
    },
    body1: {
      fontSize: '1rem',
      lineHeight: 1.5,
    },
  },
  breakpoints: {
    values: {
      xs: 0,
      sm: 600,
      md: 900,
      lg: 1200,
      xl: 1536,
    },
  },
};

export const lightTheme = createTheme({
  ...baseTheme,
  palette: {
    mode: 'light',
    primary: {
      main: '#1976d2',
      light: '#42a5f5',
      dark: '#1565c0',
      contrastText: '#ffffff',
    },
    secondary: {
      main: '#dc004e',
      light: '#ff5983',
      dark: '#9a0036',
      contrastText: '#ffffff',
    },
    background: {
      default: '#f5f5f5',
      paper: '#ffffff',
    },
    text: {
      primary: '#212121',
      secondary: '#757575',
    },
  },
});

export const darkTheme = createTheme({
  ...baseTheme,
  palette: {
    mode: 'dark',
    primary: {
      main: '#90caf9',
      light: '#e3f2fd',
      dark: '#42a5f5',
      contrastText: '#000000',
    },
    background: {
      default: '#121212',
      paper: '#1e1e1e',
    },
    text: {
      primary: '#ffffff',
      secondary: '#b0b0b0',
    },
  },
});

// Theme Provider Component
export const ThemeProvider: React.FC<{ children: React.ReactNode }> = ({ children }) => {
  const [darkMode, setDarkMode] = useState(false);
  
  const theme = darkMode ? darkTheme : lightTheme;
  
  return (
    <MuiThemeProvider theme={theme}>
      <CssBaseline />
      <ThemeContext.Provider value={{ darkMode, setDarkMode }}>
        {children}
      </ThemeContext.Provider>
    </MuiThemeProvider>
  );
};
```

RESPONSIVE DESIGN PATTERNS:

```typescript
// Responsive utilities
const useBreakpoint = () => {
  const theme = useTheme();
  const isMobile = useMediaQuery(theme.breakpoints.down('sm'));
  const isTablet = useMediaQuery(theme.breakpoints.between('sm', 'lg'));
  const isDesktop = useMediaQuery(theme.breakpoints.up('lg'));
  
  return { isMobile, isTablet, isDesktop };
};

// Responsive component styling
const ResponsiveContainer = styled('div')(({ theme }) => ({
  padding: theme.spacing(2),
  [theme.breakpoints.up('sm')]: {
    padding: theme.spacing(3),
  },
  [theme.breakpoints.up('lg')]: {
    padding: theme.spacing(4),
  },
}));
```
```

## 🔧 **PERFORMANCE OPTIMIZATION PROMPT**

```
ROLE: Performance Engineer & Frontend Optimizer

TASK: Implement performance optimizations for optimal user experience.

OPTIMIZATION STRATEGIES:

1. CODE SPLITTING:
```typescript
// Lazy loading with React.lazy
const LazyPage = React.lazy(() => import('./pages/LazyPage'));

// Route-based code splitting
const App = () => (
  <BrowserRouter>
    <Routes>
      <Route 
        path="/lazy" 
        element={
          <Suspense fallback={<div>Loading...</div>}>
            <LazyPage />
          </Suspense>
        } 
      />
    </Routes>
  </BrowserRouter>
);
```

2. MEMOIZATION:
```typescript
// React.memo for component optimization
export const ExpensiveComponent = React.memo(({ data }) => {
  return <div>{/* Expensive rendering */}</div>;
});

// useMemo for expensive calculations
const ExpensiveCalculation = ({ items }) => {
  const expensiveValue = useMemo(() => {
    return items.reduce((acc, item) => acc + item.value, 0);
  }, [items]);
  
  return <div>{expensiveValue}</div>;
};

// useCallback for stable function references
const ParentComponent = () => {
  const handleClick = useCallback((id) => {
    // Handle click logic
  }, []);
  
  return <ChildComponent onClick={handleClick} />;
};
```

3. IMAGE OPTIMIZATION:
```typescript
// Progressive image loading
const OptimizedImage = ({ src, alt, ...props }) => {
  const [loaded, setLoaded] = useState(false);
  const [error, setError] = useState(false);
  
  return (
    <div className="image-container">
      {!loaded && !error && <Skeleton variant="rectangular" />}
      <img
        src={src}
        alt={alt}
        onLoad={() => setLoaded(true)}
        onError={() => setError(true)}
        loading="lazy"
        style={{ display: loaded ? 'block' : 'none' }}
        {...props}
      />
      {error && <div>Failed to load image</div>}
    </div>
  );
};
```

4. BUNDLE OPTIMIZATION:
```javascript
// webpack.config.js optimizations
module.exports = {
  optimization: {
    splitChunks: {
      chunks: 'all',
      cacheGroups: {
        vendor: {
          test: /[\\/]node_modules[\\/]/,
          name: 'vendors',
          chunks: 'all',
        },
      },
    },
  },
  resolve: {
    alias: {
      '@': path.resolve(__dirname, 'src'),
    },
  },
};
```

PERFORMANCE METRICS:
- First Contentful Paint: <1.5s
- Largest Contentful Paint: <2.5s
- Time to Interactive: <3.5s
- Cumulative Layout Shift: <0.1
- Bundle size: <250KB (gzipped)
```

---

**�� FRONTEND STATUS**: Modern React development with best practices
**⚡ PERFORMANCE**: Optimized for speed and user experience  
**🔧 MAINTAINABILITY**: Clean architecture with comprehensive testing
**�� RESPONSIVE**: Mobile-first design with accessibility compliance
