# Academic Website - Project Structure

## 📁 Directory Organization

```
Academic_Website/
├── index.html              # Main HTML file
├── index - first version.html  # Backup
│
├── css/
│   └── styles.css         # All styling and color schemes
│
├── js/
│   └── theme.js          # Dark mode/theme toggle functionality
│
├── images/               # Place for profile images, logos, etc.
│   └── README.md        # Image asset guidelines
│
└── files/               # Place for downloadable files (CV, papers, etc.)
    └── README.md        # File asset guidelines
```

## 🎨 CSS Structure (css/styles.css)

The CSS file is organized into logical sections:

- **Typography & Global Styles** - Font families, scroll behavior
- **Light Mode (Default)** - Default color scheme
- **Dark Mode** - Dark theme colors and overrides
- **Navigation** - Logo, nav links, search, theme toggle
- **Profile & Social Icons** - Profile image, social buttons
- **Typography & Sections** - Headings, bio text
- **Lists & Items** - Checkmark icons, list styling
- **Education Section** - Education grid and item styling
- **Publication Cards** - Card styling and hover effects

### Easy Color Editing

All color values are at the top of each section for easy modification:

```css
/* Example - Light Mode */
body {
    background-color: #ffffff;
    color: #1a1a1a;
}

/* Example - Dark Mode */
html.dark-mode body {
    background-color: #0f1419;
    color: #ffffff;
}
```

## 🚀 JavaScript (js/theme.js)

Handles:
- Dark/Light mode toggle
- Theme persistence using localStorage
- Icon switching (sun/moon icons)
- DOMContentLoaded setup for reliability

## 📝 Adding New Content

### New Images
1. Place images in the `images/` folder
2. Reference in HTML: `<img src="images/filename.jpg" alt="description">`

### New Files (CV, Papers, etc.)
1. Place files in the `files/` folder
2. Reference in HTML: `<a href="files/filename.pdf">Download</a>`

### New Styling
1. Edit `css/styles.css` directly
2. Keep the organization structure for maintainability
3. Add comments for new sections

### New JavaScript
1. Create new files in `js/` folder
2. Link them in `index.html`: `<script src="js/filename.js"></script>`

## 🔧 Common Tasks

### Change Color Scheme
Edit `css/styles.css` sections:
- Update hex codes in "Light Mode" section (lines ~20-60)
- Update hex codes in "Dark Mode" section (lines ~65-120)

### Modify Typography
Find classes like `.section-heading`, `.bio-section` in `styles.css`
Update font-size, font-weight, line-height as needed

### Update Theme Toggle
Edit `js/theme.js` - the `applyTheme()` function manages which class to add

## 📱 Responsive Design

CSS uses Tailwind classes for the main layout. Custom CSS handles:
- `.interests-grid` - Changes to 1 column on screens < 768px
- All other responsive behavior through Tailwind classes in HTML

## ✅ Best Practices

1. **Keep CSS organized** - Use the existing section structure
2. **Add comments** - Document why, not just what
3. **Test dark mode** - Check all changes in both themes
4. **Validate links** - Ensure all file/image paths are correct
5. **Version control** - Keep `index - first version.html` as backup

---

**Quick Reference:**
- HTML: `index.html`
- Styling: `css/styles.css`
- Functionality: `js/theme.js`
- Assets: `images/` and `files/` folders
