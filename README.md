# bleattree

claude slopped linktree clone

## Quick Start

### Local Development

1. Clone or download this repository
2. Edit `config.json` with your information
3. Serve the files with any local web server:

```bash
# Using Python 3
python3 -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (install http-server first: npm install -g http-server)
http-server -p 8000

# Using PHP
php -S localhost:8000
```

4. Open `http://localhost:8000` in your browser

### Production Deployment

Deploy the files to any static hosting service:

- **GitHub Pages**: Push to a GitHub repo and enable Pages
- **Netlify**: Drag and drop the folder or connect your Git repo
- **Vercel**: Import your project from Git
- **Cloudflare Pages**: Connect your repository
- **Any web hosting**: Upload via FTP/SFTP to your server

## Customization

### Edit Your Profile

Open `config.json` and modify the profile section:

```json
{
  "profile": {
    "name": "Your Name",
    "bio": "Your bio or tagline here",
    "avatar": "https://your-image-url.com/avatar.jpg"
  }
}
```

### Add Your Links

Add or modify links in the `sections` array:

```json
{
  "sections": [
    {
      "title": "My Links",
      "note": "Optional description for this section",
      "links": [
        {
          "title": "My Website",
          "url": "https://example.com"
        },
        {
          "title": "GitHub",
          "url": "https://github.com/username"
        }
      ]
    }
  ]
}
```

**Link Icons:**
- By default, favicons are automatically fetched from each URL
- Add `"image": "images/myicon.png"` to use a custom local image
- Add `"icon": "🌐"` to use an emoji instead
- Priority: local image > emoji > favicon

### Use Custom Images

Place your custom icons in the `images/` folder and reference them:

```json
{
  "title": "My Cool Link",
  "url": "https://example.com",
  "image": "images/my-cool-icon.png"
}
```

**Image Guidelines:**
- Supported formats: PNG, JPG, GIF, SVG, WebP
- Recommended size: 64x64px or larger
- Images will be scaled to 24x24px for display
- If the image fails to load, it will fallback to the URL's favicon

### Customize Colors

Change the theme in `config.json`:

```json
{
  "theme": {
    "backgroundColor": "#0f172a",
    "cardColor": "#1e293b",
    "textColor": "#f1f5f9",
    "accentColor": "#6366f1",
    "linkHoverColor": "#818cf8"
  }
}
```

### Add Social Links

Add social media icons at the bottom:

```json
{
  "social": [
    {
      "platform": "github",
      "url": "https://github.com/username"
    },
    {
      "platform": "twitter",
      "url": "https://twitter.com/username"
    }
  ]
}
```

Supported platforms: `github`, `twitter`, `linkedin`, `instagram`, `youtube`, `facebook`, `twitch`, `discord`, `spotify`, `tiktok`

## File Structure

```
bleattree/
├── index.html       # Main HTML file
├── styles.css       # All styling
├── app.js          # JavaScript for loading config
├── config.json     # Your customization settings
├── oneko.js        # Animated cat cursor follower
├── oneko.gif       # Cat sprite sheet
├── images/         # Place custom link icons here
│   └── README.md   # Usage instructions
└── README.md       # This file
```

## Advanced Customization

### Custom Favicon

Add a favicon by placing this in the `<head>` section of `index.html`:

```html
<link rel="icon" type="image/png" href="favicon.png">
```

### Analytics

Add analytics by including your tracking code before the closing `</body>` tag in `index.html`.

### Custom Fonts

Add custom fonts in `styles.css`:

```css
@import url('https://fonts.googleapis.com/css2?family=Your+Font&display=swap');

body {
    font-family: 'Your Font', sans-serif;
}
```

## Browser Support

Works on all modern browsers:
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Opera 76+

## License

Free to use for personal and commercial projects. No attribution required.


