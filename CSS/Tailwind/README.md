# Tailwind CSS

## Standalone executable

Works even with HTML and CSS files only

```input.css```

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

```tailwind.config.js```

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./*.html"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

```bash
./tailwindcss -i input.css -o output.css --minify
```



