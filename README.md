# Classy Bear Cabin Website

A clean, modern, fast-loading static website for Classy Bear Cabin - a luxury vacation rental in Gatlinburg, TN.

## Features

- **Mobile-responsive** design that works on all devices
- **Fast-loading** with lazy-loaded images and minimal dependencies
- **Rustic luxury** aesthetic with warm earth tones
- **Smooth scrolling** navigation with fixed header
- **Animated elements** on scroll for visual interest
- **SEO-friendly** with proper meta tags

## Sections

1. **Hero** - Full-screen banner with key property highlights
2. **About** - Property overview with key stats
3. **Amenities** - 6 featured amenities with icons
4. **Gallery** - Masonry-style photo grid
5. **Location** - Nearby attractions with embedded map
6. **CTA** - Call-to-action with parallax background
7. **Contact** - Contact info and feature list
8. **Footer** - Navigation links and branding

## Files

```
website/
├── index.html    # Main HTML file
├── style.css     # All styles (no external CSS frameworks)
└── README.md     # This file
```

## Local Preview

Simply open `index.html` in a web browser, or use a local server:

```bash
# Using Python
python3 -m http.server 8000

# Using Node.js (if http-server is installed)
npx http-server

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000`

## Deploying to GitHub Pages

### Option 1: Deploy from main branch

1. Create a new GitHub repository (e.g., `classy-bear-cabin`)

2. Initialize and push the website files:
   ```bash
   cd website
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/classy-bear-cabin.git
   git push -u origin main
   ```

3. Go to repository **Settings** → **Pages**

4. Under "Source", select:
   - Branch: `main`
   - Folder: `/ (root)`

5. Click **Save**

6. Your site will be live at: `https://YOUR_USERNAME.github.io/classy-bear-cabin/`

### Option 2: Custom domain

1. After deploying to GitHub Pages, go to **Settings** → **Pages**

2. Under "Custom domain", enter your domain (e.g., `www.classybearcabin.com`)

3. Add these DNS records with your domain registrar:

   **For apex domain (classybearcabin.com):**
   ```
   Type: A
   Host: @
   Value: 185.199.108.153
   Value: 185.199.109.153
   Value: 185.199.110.153
   Value: 185.199.111.153
   ```

   **For www subdomain:**
   ```
   Type: CNAME
   Host: www
   Value: YOUR_USERNAME.github.io
   ```

4. Check "Enforce HTTPS" once DNS propagates

## Customization

### Images

Currently using images from the Airbnb CDN. To use your own images:

1. Add images to an `images/` folder
2. Update the `src` attributes in `index.html`
3. Recommended: Optimize images for web (max 1920px wide, compressed)

### Colors

Edit the CSS variables in `style.css`:

```css
:root {
    --color-primary: #8B5A2B;      /* Main brown */
    --color-primary-dark: #5D3A1A;  /* Darker brown */
    --color-accent: #D4A574;        /* Golden tan */
    /* ... etc */
}
```

### Booking Link

Update the booking URL in all `href` attributes containing the booking link:

```html
href="https://classybearcabin.com/search?period=daily&duration=1&adults=1"
```

### Contact Info

Update the email in the contact section:

```html
<a href="mailto:info@classybearcabin.com">info@classybearcabin.com</a>
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome for Android)

## Performance Tips

- Images are lazy-loaded (`loading="lazy"`)
- No external JavaScript libraries
- Minimal CSS with no frameworks
- Google Fonts loaded with `display=swap`

## License

© 2025 Classy Bear Cabin. All rights reserved.
