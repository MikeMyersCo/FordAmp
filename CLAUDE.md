# CLAUDE.md - Guidelines for the Tickets Application

## Development Commands
- View site: Open `index.html` in browser or use a simple HTTP server (`python -m http.server` or `npx serve`)
- Check JS errors: Open browser console (F12) while viewing the page
- Validate HTML: Use browser developer tools or https://validator.w3.org/
- Deploy: Upload files to web hosting service

## Code Style Guidelines

### JavaScript
- Use ES6+ features (arrow functions, async/await, template literals)
- Variable naming: camelCase for variables and functions, PascalCase for classes
- Store sensitive data (API keys) in `process-env.js` and `local-env.js`, never hardcode
- Use try/catch blocks for API calls with appropriate error handling
- Apply fetch() for API requests with proper error handling and loading states
- Prefer const over let where possible; minimize use of var
- Document complex functions with comments explaining purpose and parameters

### HTML/CSS
- Use semantic HTML elements (header, nav, main, section, footer)
- Class naming: descriptive, lowercase with hyphens for multi-word
- Mobile-first responsive design with appropriate breakpoints
- Maintain 2-space indentation
- Group related CSS properties together and order consistently

When making changes, follow existing patterns in the codebase and ensure the site remains functional on all target devices (desktop, tablet, mobile).