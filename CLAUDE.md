# CLAUDE.md - Guidelines for the FordAmp Tickets Application

## Development Commands
- Start local server: `python -m http.server` or `npx serve`
- View site: Open browser to http://localhost:8000 (or port shown in terminal)
- Debug: Open browser console (F12) to check for JS errors and API responses
- Validate HTML: Use browser dev tools or https://validator.w3.org/
- Test API: Verify Google Sheets connection in console network tab
- Deploy: Upload all files to web hosting service

## Environment Setup
- Create `local-env.js` with your development credentials:
```js
window.ENV = {
    GOOGLE_API_KEY: 'your-google-api-key',
    SPREADSHEET_ID: 'your-spreadsheet-id'
};
```

## Code Style Guidelines

### JavaScript
- Use ES6+ features (arrow functions, async/await, template literals)
- Naming: camelCase for variables/functions, PascalCase for classes
- Store API keys in environment files, never hardcode
- Wrap API calls in try/catch with user-friendly error messages
- Use modern fetch() API with appropriate loading states
- Prefer const over let; avoid var completely

### HTML/CSS
- Use semantic HTML5 elements
- Classes: lowercase with hyphens (e.g., event-card)
- 2-space indentation throughout
- Mobile-first responsive design
- Group related CSS properties logically