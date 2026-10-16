# Responsive Web Design Masterclass Project

This project is a complete, industrial-standard reference implementation demonstrating all core **Responsive Web Design** concepts:

1. **Viewport Meta Tag**: Setting initial scale and device width.
2. **Mobile-First CSS**: Writing baseline styles for mobile screens first, then expanding with `min-width` media queries.
3. **Breakpoints**: 
   - Mobile: Default / `< 480px`
   - Mobile Landscape / Large Phones: `@media (min-width: 480px)`
   - Tablets: `@media (min-width: 768px)`
   - Desktops: `@media (min-width: 1024px)`
4. **Responsive Typography (`clamp()`)**: Fluid scaling headings without media query clutter (`clamp(MIN, VAL, MAX)`).
5. **Responsive Images**:
   - `<picture>` element for **Art Direction** (loading different images per breakpoint).
   - `srcset` & `sizes` attributes for **Resolution Switching** (loading optimized image sizes based on viewport).

## 📂 Project Structure

```text
responsive-web-design/
├── index.html              # Main HTML markup showcasing all responsive features
├── README.md               # Documentation & testing guide
├── css/
│   └── styles.css          # Mobile-first CSS stylesheet with clamp & media queries
└── assets/
    ├── hero-mobile.svg     # Art direction image for Mobile
    ├── hero-tablet.svg     # Art direction image for Tablet
    ├── hero-desktop.svg    # Art direction image for Desktop
    ├── card-sm.svg         # Resolution switching image (Small - 400w)
    ├── card-md.svg         # Resolution switching image (Medium - 800w)
    └── card-lg.svg         # Resolution switching image (Large - 1200w)
```

## 🚀 How to Run & Test in VS Code

1. Open this folder in VS Code (`File > Open Folder...`).
2. Install the **Live Server** extension (or right click `index.html` and open with default browser).
3. Open **Chrome / Edge Developer Tools** (`F12` or `Ctrl + Shift + I` / `Cmd + Option + I`).
4. Toggle the **Device Toolbar** (`Ctrl + Shift + M` / `Cmd + Shift + M`).
5. Resize the screen width to observe:
   - **Breakpoint Badge** updating at top-right (`Mobile < 480px`, `Large Phone ≥ 480px`, `Tablet ≥ 768px`, `Desktop ≥ 1024px`).
   - **Hero Image** swapping art styles via `<picture>`.
   - **Product Image** selecting optimum `srcset` resolution.
   - **Typography** smoothly scaling with `clamp()`.
   - **Card Grid** flowing from 1 column -> 2 columns -> 3 columns -> 4 columns.
