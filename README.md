# Erik — Capstone Research Website

## File Structure

```
eriksite/
├── index.html              ← Home page (open this in browser)
├── css/
│   └── style.css           ← All styles (fonts, colors, layout, animation)
├── assets/                 ← Put your images here
│   └── hero-bg.jpg         ← (replace with your actual hero background image)
└── pages/
    ├── essay.html          ← Full research paper
    ├── findings.html       ← Key findings + implementation steps
    ├── resources.html      ← Books, tools, worksheets
    └── about.html          ← About the author
```

## How to Open

1. Copy the entire `eriksite/` folder to your computer.
2. Open `index.html` in any web browser (Chrome, Firefox, Safari).
3. All links between pages work automatically — no server needed.

## Adding Your Hero Background Image

1. Place your image in the `assets/` folder (e.g., `assets/hero-bg.jpg`).
2. Open `css/style.css`.
3. Find the `.hero-bg` selector (around line 100).
4. Uncomment the image lines:

```css
.hero-bg {
  background-image: url('../assets/hero-bg.jpg');
  background-size: cover;
  background-position: center;
}
```

## Scroll Animations

- Elements with the class `scroll-fade` animate in as you scroll using CSS `animation-timeline: view()`.
- **Supported in:** Chrome 115+, Edge 115+
- **Firefox/Safari fallback:** Elements are shown statically (no animation, but content is fully visible).

## Customizing Colors

All colors are defined as CSS variables at the top of `style.css`:

```css
:root {
  --cream:      #f7f4ef;
  --clay:       #c5856a;   ← accent/highlight color
  --sage:       #8fa89a;
  --dusty-blue: #7a9cb8;
  --ink:        #1a1714;   ← text color
}
```

Change these values to retheme the entire site instantly.
