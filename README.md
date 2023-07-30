
# TAILWIND-DARK-MODE

**Easy way to implement dark mode for an existing TailwindCSS project**

Easy way to implement dark mode for an existing TailwindCSS project.

### Setup

```js
// file = tailwind.config.js
import addUtilitesWithDarkMode from 'dark-mode-tailwind'

export default {
   content: {
      files: ["./index.html","./src/**/*.{js,ts,jsx,tsx}",], //your usual path for tailwind
   },
   /* Your rest tailwind config */
   darkMode: 'class',
   plugins: [
      /* Your rest tailwind plugins */
      plugin(addUtilitesWithDarkMode(({ addUtility }) => {
         addUtility('bg', 'background-color', {
            black: ['#222222', '#eee']
         })
      }))
   ],
}
```
