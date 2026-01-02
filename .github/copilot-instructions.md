# AI Coding Guidelines for component_react

## Project Overview
This is a React single-page application built with Vite, using React 19. The project focuses on component development with a minimal setup for fast development and hot module replacement (HMR).

## Architecture
- **Entry Point**: `src/main.jsx` renders the app into `#root` using `createRoot` and `StrictMode`.
- **Root Component**: `src/App.jsx` serves as the main component, demonstrating basic React patterns.
- **Structure**: Components and styles are colocated in `src/`. Assets go in `src/assets/`.
- **Build Tool**: Vite handles bundling, dev server, and production builds with React plugin for HMR.

## Key Patterns
- Use functional components with React hooks (e.g., `useState` in `src/App.jsx`).
- Import styles directly in components (e.g., `import './App.css'`).
- Assets: Import SVGs as React components or use public paths for static files.
- No TypeScript: Write plain JavaScript with JSX.

## Developer Workflows
- **Development**: Run `npm run dev` to start Vite dev server with HMR.
- **Build**: Use `npm run build` to create production bundle in `dist/`.
- **Linting**: Execute `npm run lint` to check code with ESLint (config in `eslint.config.js`).
- **Preview**: After build, `npm run preview` serves the production build locally.

## Conventions
- Component naming: PascalCase (e.g., `App`).
- File extensions: `.jsx` for components, `.js` for utilities.
- CSS: Scoped styles per component, global styles in `src/index.css`.
- Dependencies: Minimal - only React and Vite essentials. Add new packages via `npm install`.

## Integration Points
- No external APIs or services currently integrated.
- For future additions: Use `fetch` or libraries like Axios for HTTP requests.
- State management: Start with local state; consider Context API or Redux for complex apps.

## Examples
- Basic component with state: See `src/App.jsx` for `useState` usage.
- Styling: Inline classes and imported CSS as in `src/App.css`.
- Asset handling: SVG imports like `import reactLogo from './assets/react.svg'`.

Follow React best practices: Keep components small, use hooks for logic, handle side effects properly.