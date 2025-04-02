# CLAUDE.md - Guidelines for the FordAmp Tickets Application

## Development Commands
- Start local server: `python -m http.server` or `npx serve`
- View site: Open browser to http://localhost:8000 (or port shown in terminal)
- Debug: Open browser console (F12) to check for JS errors and API responses
- Validate HTML: Use browser dev tools or https://validator.w3.org/
- Test API: Run `fetch('https://sheets.googleapis.com/v4/spreadsheets/your-spreadsheet-id/values/A1:Z1000?key=your-api-key').then(r=>r.json()).then(console.log)`
- Lint HTML: Use `npx html-validate index.html`
- Quick reload: Install `browser-sync` and run `npx browser-sync start --server --files "*.html, *.js, *.css"`

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
- Spacing: 2-space indentation, space after keywords/before blocks
- Error handling: Wrap API calls in try/catch with user-friendly messages
- Fetch: Set timeouts, show loading states, handle network failures
- Data: Parse dates with Intl.DateTimeFormat, format currency with Intl.NumberFormat
- DOM: Prefer querySelector/All over getElementById/getElementsByClassName
- Modularity: Group related functions, use comments to separate sections

### HTML/CSS
- HTML: Use semantic elements (header, nav, section, article, footer)
- Classes: lowercase with hyphens (e.g., event-card)
- Mobile-first design: Use media queries to enhance for larger screens
- Variables: Use CSS custom properties for colors, spacing, fonts
- Performance: Lazy-load images, preload critical assets
- Animation: Use CSS transitions/animations over JavaScript when possible