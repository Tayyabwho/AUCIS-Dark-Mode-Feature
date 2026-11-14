# AUCIS-Dark-Mode-Feature
# 🌓 React & Tailwind Dark/Light Mode Engine

Built as part of the official **AUCIS Website** (Air University Kamra)[cite: 1]. This feature provides a seamless theme-switching toggle across the application.

---

## 🚀 What I Built & Solved
* **Dynamic DOM Class Toggling**: Engineered a React state handler that updates the HTML document root to apply the `.dark` class.
* **Tailwind CSS Layer Configuration**: Customized `@layer base` inside `index.css` to manage global background colors, smooth transition timings, and theme states.
* **Contrast & Accessibility Fixes**: Resolved light-mode contrast issues so text automatically adapts between light and dark backgrounds.

---

## 📂 The Core Code

### 1. Global Theme Styles (`index.css`)
```css
@layer base {
  :root {
    color-scheme: light;
  }

  .dark {
    color-scheme: dark;
  }

  html {
    scroll-behavior: smooth;
  }

  body {
    @apply bg-white text-zinc-900 transition-colors duration-300;
  }

  .dark body {
    @apply bg-ink text-cream;
    background-image:
      radial-gradient(1200px 620px at 82% -8%, rgba(65, 90, 119, 0.38), transparent 62%),
      radial-gradient(900px 520px at 6% 4%, rgba(119, 141, 122, 0.16), transparent 60%),
      radial-gradient(900px 700px at 50% 110%, rgba(212, 196, 168, 0.09), transparent 65%);
    background-attachment: fixed;
  }
}
