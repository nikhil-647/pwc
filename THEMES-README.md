# PWC Website - Multi-Theme System

## Overview
This website features a complete multi-theme system where each theme shares the same HTML structure and functionality, but uses different color palettes. This allows you to easily provide different color options to your client.

## Available Themes

### 1. **Base Gold Theme** (Default)
- **File:** `index.html`
- **Theme CSS:** `theme-base.css`
- **Colors:** Gold (#EAB308), Yellow (#FEF08A), Dark (#0F172A)
- **Description:** Professional gold palette symbolizing prosperity and trust

### 2. **Ocean Blue Theme**
- **File:** `index-ocean-blue.html`
- **Theme CSS:** `theme-ocean-blue.css`
- **Colors:** Sky Blue (#0EA5E9), Light Blue (#7DD3FC), Navy (#0C4A6E)
- **Description:** Professional blue inspired by ocean and sky

### 3. **Emerald Green Theme**
- **File:** `index-emerald-green.html`
- **Theme CSS:** `theme-emerald-green.css`
- **Colors:** Emerald (#10B981), Mint (#6EE7B7), Forest (#064E3B)
- **Description:** Fresh green symbolizing growth and prosperity

### 4. **Royal Purple Theme**
- **File:** `index-royal-purple.html`
- **Theme CSS:** `theme-royal-purple.css`
- **Colors:** Purple (#A855F7), Lavender (#D8B4FE), Deep Purple (#581C87)
- **Description:** Luxurious purple representing premium services

### 5. **Crimson Red Theme**
- **File:** `index-crimson-red.html`
- **Theme CSS:** `theme-crimson-red.css`
- **Colors:** Red (#EF4444), Pink (#FCA5A5), Maroon (#7F1D1D)
- **Description:** Bold red representing strength and confidence

### 6. **Midnight Navy Theme**
- **File:** `index-midnight-navy.html`
- **Theme CSS:** `theme-midnight-navy.css`
- **Colors:** Navy (#1E293B), Blue (#60A5FA), Light Blue (#BFDBFE)
- **Description:** Sophisticated navy with silver accents

## File Structure

```
pwc/
├── theme-selector.html          # Theme selection landing page
├── index.html                   # Base Gold Theme (default)
├── index-ocean-blue.html        # Ocean Blue Theme
├── index-emerald-green.html     # Emerald Green Theme
├── index-royal-purple.html      # Royal Purple Theme
├── index-crimson-red.html       # Crimson Red Theme
├── index-midnight-navy.html     # Midnight Navy Theme
├── theme-base.css               # Base CSS variables
├── theme-ocean-blue.css         # Ocean Blue colors
├── theme-emerald-green.css      # Emerald Green colors
├── theme-royal-purple.css       # Royal Purple colors
├── theme-crimson-red.css        # Crimson Red colors
├── theme-midnight-navy.css      # Midnight Navy colors
└── styles.css                   # Main styling (uses variables)
```

## How It Works

### CSS Variable System

The theme system uses CSS custom properties (variables) to control all colors throughout the website:

1. **theme-base.css** - Defines all color variables with default values
2. **theme-{name}.css** - Overrides variables with theme-specific colors
3. **styles.css** - Uses variables throughout all styling

### Color Variables

Each theme file overrides these variables:

```css
:root {
    /* Primary Colors */
    --primary-dark
    --primary-light
    --accent-primary
    --accent-secondary
    
    /* Text Colors */
    --text-primary
    --text-secondary
    --text-light
    --text-on-dark
    
    /* Background Colors */
    --bg-primary
    --bg-secondary
    --bg-dark
    --bg-card
    
    /* Gradient Colors */
    --gradient-start
    --gradient-mid
    --gradient-end
    
    /* And many more... */
}
```

## Usage Instructions

### For Viewing Themes:
1. Open `theme-selector.html` to see all available themes
2. Click on any theme to view the full website in that color palette
3. Each theme is a complete, functional website

### For Development:

#### To Add a New Theme:
1. Create a new theme CSS file: `theme-{name}.css`
2. Copy the structure from `theme-base.css`
3. Customize all color variables
4. Copy `index.html` to `index-{name}.html`
5. Update the `<link>` tag to reference your new theme CSS
6. Add your theme to `theme-selector.html`

#### To Modify Existing Theme:
1. Open the theme's CSS file (e.g., `theme-ocean-blue.css`)
2. Modify the color values in the `:root` section
3. Save and refresh - changes apply instantly

#### To Update Content:
1. Content is the same across all themes
2. Edit the HTML files or edit one and copy to others
3. Only the `<link>` tag should differ between theme HTML files

## Advantages of This System

✅ **Separation of Concerns** - Colors separated from structure
✅ **Easy Maintenance** - Update colors without touching HTML
✅ **Client Flexibility** - Present multiple options easily
✅ **Consistent Experience** - Same functionality across themes
✅ **Scalable** - Easy to add new themes
✅ **Performance** - No JavaScript needed for theming
✅ **SEO Friendly** - Each theme can be on separate route

## Deployment Options

### Option 1: Separate Routes
Deploy each theme on different routes:
- `yoursite.com/gold` → index.html
- `yoursite.com/ocean-blue` → index-ocean-blue.html
- `yoursite.com/emerald-green` → index-emerald-green.html
- etc.

### Option 2: Subdomains
Use subdomains for each theme:
- `gold.yoursite.com`
- `blue.yoursite.com`
- `green.yoursite.com`

### Option 3: Single Site with Theme Selector
Have theme-selector.html as landing page, let users choose

### Option 4: Client-Specific Deployment
Deploy one specific theme based on client preference

## Browser Support

✅ All modern browsers (Chrome, Firefox, Safari, Edge)
✅ CSS Variables supported in all major browsers
✅ Fully responsive on all devices
✅ No JavaScript required for themes (only for interactions)

## Customization Tips

### To Change a Specific Color:
1. Find the variable in the theme CSS file
2. Update the color value
3. Use hex (#), rgb(), rgba(), or color names

### To Add New Color Variables:
1. Add to `theme-base.css` first
2. Override in each theme CSS file
3. Use in `styles.css` with `var(--variable-name)`

### To Adjust Opacity:
Use rgba() values in theme files:
```css
--hover-overlay: rgba(14, 165, 233, 0.1);
```

## Color Psychology Guide

🟡 **Gold/Yellow** - Prosperity, optimism, warmth
🔵 **Blue** - Trust, professionalism, stability
🟢 **Green** - Growth, prosperity, reliability  
🟣 **Purple** - Luxury, sophistication, creativity
🔴 **Red** - Strength, passion, confidence
⚫ **Navy** - Authority, elegance, corporate

## Technical Notes

- All color values use CSS custom properties
- Themes load in correct cascade order
- No theme conflicts or specificity issues
- Compatible with build tools and preprocessors
- Can be extended with dark mode variants

## Support

For questions or customization help, contact the developer.

## License

© 2026 Patil Wafekar Consultancy LLP
Designed & Developed by Nikhil Patil

---

**Last Updated:** January 14, 2026
