# Portfolio Website

A modern, responsive portfolio website built with HTML, CSS, and JavaScript.

## Features

- 🎨 Modern and clean design
- 📱 Fully responsive layout
- ⚡ Smooth animations and transitions
- 🚀 Fast loading and optimized performance
- 📧 Working contact form
- 🌙 Dark mode support (optional)
- 📊 Interactive skill showcase
- 💼 Project gallery with hover effects

## Sections

1. **Hero Section** - Introduction with call-to-action buttons
2. **About** - Personal information and statistics
3. **Skills** - Technical skills organized by categories
4. **Projects** - Featured work with live demos and source code links
5. **Contact** - Contact form and social media links

## Technologies Used

- HTML5
- CSS3 (Flexbox, Grid, Animations)
- Vanilla JavaScript
- Font Awesome Icons
- Google Fonts

## Setup Instructions

1. Clone or download the repository
2. Open `index.html` in your browser
3. Customize the content with your information
4. Replace placeholder images with your own
5. Update social media links and contact information

## Customization

### Colors
Edit the CSS variables in `styles.css`:
```css
:root {
    --primary-color: #667eea;
    --secondary-color: #764ba2;
    --accent-color: #f093fb;
}
```

### Content
- Update personal information in `index.html`
- Replace project details and images
- Modify skill categories and items
- Update contact information

### Images
Replace these placeholder images:
- Profile picture: Update the `src` in the hero section
- Project images: Replace placeholder URLs with your project screenshots

## Deployment

### GitHub Pages
1. Push code to GitHub repository
2. Go to repository Settings
3. Enable GitHub Pages from main branch
4. Your site will be available at `https://username.github.io/repository-name`

### Netlify
1. Drag and drop the project folder to Netlify
2. Your site will be deployed automatically

### Vercel
1. Import project from GitHub
2. Deploy with default settings

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact

Feel free to reach out if you have any questions or suggestions!
```

## إضافة ملف package.json للمشروع:

```json:package.json
{
  "name": "portfolio-website",
  "version": "1.0.0",
  "description": "A modern responsive portfolio website",
  "main": "index.html",
  "scripts": {
    "start": "live-server --port=3000",
    "build": "npm run minify-css && npm run minify-js",
    "minify-css": "cleancss -o dist/styles.min.css styles.css",
    "minify-js": "uglifyjs script.js -o dist/script.min.js",
    "deploy": "gh-pages -d .",
    "lint": "eslint script.js",
    "format": "prettier --write *.html *.css *.js"
  },
  "keywords": [
    "portfolio",
    "website",
    "responsive",
    "html",
    "css",
    "javascript"
  ],
  "author": "Your Name",
  "license": "MIT",
  "devDependencies": {
    "clean-css-cli": "^5.6.2",
    "eslint": "^8.0.0",
    "gh-pages": "^4.0.0",
    "live-server": "^1.2.2",
    "prettier": "^2.8.0",
    "uglify-js": "^3.17.4"
  },
  "repository": {
    "type": "git",
    "url": "https://github.com/yourusername/portfolio-website.git"
  },
  "homepage": "https://yourusername.github.io/portfolio-website"
}
```

## إضافة ملف .gitignore:

```gitignore:.gitignore
# Dependencies
node_modules/
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Build outputs
dist/
build/

# Environment variables
.env
.env.local
.env.development.local
.env.test.local
.env.production.local

# IDE files
.vscode/
.idea/
*.swp
*.swo

# OS generated files
.DS_Store
.DS_Store?
._*
.Spotlight-V100
.Trashes
ehthumbs.db
Thumbs.db

# Logs
logs
*.log

# Temporary files
*.tmp
*.temp
```

## إضافة ملف CSS إضافي للطباعة:

```css:print.css
/* Print Styles */
@media print {
    * {
        background: transparent !important;
        color: black !important;
        box-shadow: none !important;
        text-shadow: none !important;
    }

    body {
        font-size: 12pt;
        line-height: 1.4;
    }

    .navbar,
    .hamburger,
    .back-to-top,
    .theme-toggle,
    .hero-buttons,
    .project-overlay,
    .social-links {
        display: none !important;
    }

    .hero {
        background: none !important;
        color: black !important;
        padding: 20px 0;
        min-height: auto;
    }

    .hero-content {
        grid-template-columns: 1fr;
        gap: 1rem;
    }

    .profile-pic {
        width: 150px;
        height: 150px;
        margin: 0 auto;
    }

    .section-title {
        font-size: 18pt;
        margin-bottom: 1rem;
        border-bottom: 2px solid black;
        padding-bottom: 5px;
    }

    .project-card,
    .skill-category,
    .stat {
        break-inside: avoid;
        margin-bottom: 1rem;
        border: 1px solid #ccc;
        padding: 1rem;
    }

    .contact-form {
        display: none;
    }

    a[href]:after {
        content: " (" attr(href) ")";
        font-size: 10pt;
    }

    .nav-link[href]:after,
    .social-link[href]:after,
    .project-link[href]:after {
        content: "";
    }
}
```

## إضافة ملف robots.txt لمحركات البحث:

```txt:robots.txt
User-agent: *
Allow: /

Sitemap: https://yourdomain.com/sitemap.xml
```

## إضافة ملف sitemap.xml:

```xml:sitemap.xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    <url>
        <loc>https://yourdomain.com/</loc>
        <lastmod>2024-01-01</lastmod>
        <changefreq>monthly</changefreq>
        <priority>1.0</priority>
    </url>
</urlset>
```

## إضافة ملف manifest.json للـ PWA:

```json:manifest.json
{
    "name": "Your Name - Portfolio",
    "short_name": "Portfolio",
    "description": "Personal portfolio website showcasing my work and skills",
    "start_url": "/",
    "display": "standalone",
    "background_color": "#667eea",
    "theme_color": "#667eea",
    "orientation": "portrait-primary",
    "icons": [
        {
            "src": "icons/icon-72x72.png",
            "sizes": "72x72",
            "type": "image/png"
        },
        {
            "src": "icons/icon-96x96.png",
            "sizes": "96x96",
            "type": "image/png"
        },
        {
            "src": "icons/icon-128x128.png",
            "sizes": "128x128",
            "type": "image/png"
        },
        {
            "src": "icons/icon-144x144.png",
            "sizes": "144x144",
            "type": "image/png"
        },
        {
            "src": "icons/icon-152x152.png",
            "sizes": "152x152",
            "type": "image/png"
        },
        {
            "src": "icons/icon-192x192.png",
            "sizes": "192x192",
            "type": "image/png"
        },
        {
            "src": "icons/icon-384x384.png",
            "sizes": "384x384",
            "type": "image/png"
        },
        {
            "src": "icons/icon-512x512.png",
            "sizes": "512x512",
            "type": "image/png"
        }
    ]
}
```

## إضافة Service Worker للـ PWA:

```javascript:sw.js
const CACHE_NAME = 'portfolio-v1';
const urlsToCache = [
    '/',
    '/index.html',
    '/styles.css',
    '/script.js',
    '/print.css',
    'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css'
];

// Install event
self.addEventListener('install', event => {
    event.waitUntil(
        caches.open(CACHE_NAME)
            .then(cache => {
                return cache.addAll(urlsToCache);
            })
    );
});

// Fetch event
self.addEventListener('fetch', event => {
    event.respondWith(
        caches.match(event.request)
            .then(response => {
                // Return cached version or fetch from network
                return response || fetch(event.request);
            })
    );
});

// Activate event
self.addEventListener('activate', event => {
    event.waitUntil(
        caches.keys().then(cacheNames => {
            return Promise.all(
                cacheNames.map(cacheName => {
                    if (cacheName !== CACHE_NAME) {
                        return caches.delete(cacheName);
                    }
                })
            );
        })
    );
});
```

## تحديث index.html لإضافة PWA والتحسينات:

```html:index-updated.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Your Name - Full Stack Developer & UI/UX Designer. View my portfolio and get in touch for web development projects.">
    <meta name="keywords" content="web developer, full stack, UI/UX designer, portfolio, javascript, react, node.js">
    <meta name="author" content="Your Name">
    
    <!-- Open Graph Meta Tags -->
    <meta property="og:title" content="Your Name - Portfolio">
    <meta property="og:description" content="Full Stack Developer & UI/UX Designer">
    <meta property="og:image" content="https://yourdomain.com/og-image.jpg">
    <meta property="og:url" content="https://yourdomain.com">
    <meta property="og:type" content="website">
    
    <!-- Twitter Card Meta Tags -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Your Name - Portfolio">
    <meta name="twitter:description" content="Full Stack Developer & UI/UX Designer">
    <meta name="twitter:image" content="https://yourdomain.com/twitter-image.jpg">
    
    <title>Your Name - Portfolio</title>
    
    <!-- Favicon -->
    <link rel="icon" type="image/x-icon" href="/favicon.ico">
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
    <link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
    
    <!-- PWA Manifest -->
    <link rel="manifest" href="/manifest.json">
    <meta name="theme-color" content="#667eea">
    
    <!-- Stylesheets -->
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="print.css" media="print">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    
    <!-- Preconnect to external domains -->
    <link rel="preconnect" href="https://cdnjs.cloudflare.com">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Schema.org structured data -->
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "Person",
        "name": "Your Name",
        "jobTitle": "Full Stack Developer",
        "description": "Full Stack Developer & UI/UX Designer",
        "url": "https://yourdomain.com",
        "sameAs": [
            "https://github.com/yourusername",
            "https://linkedin.com/in/yourusername",
            "https://twitter.com/yourusername"
        ]
    }
    </script>
</head>
<body>
    <!-- Rest of your HTML content remains the same -->
    <!-- ... -->
    
    <!-- Scripts -->
    <script src="script.js"></script>
    
    <!-- PWA Registration -->
    <script>
        if ('serviceWorker' in navigator) {
            window.addEventListener('load', () => {
                navigator.serviceWorker.register('/sw.js')
                    .then(registration => {
                        console.log('SW registered: ', registration);
                    })
                    .catch(registrationError => {
                        console.log('SW registration failed: ', registrationError);
                    });
            });
        }
    </script>
    
    <!-- Google Analytics (optional) -->
    <script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
    <script>
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
        gtag('js', new Date());
        gtag('config', 'GA_MEASUREMENT_ID');
    </script>
</body>
</html>
```

## إضافة ملف التكوين للـ ESLint:

```json:.eslintrc.json
{
    "env": {
        "browser": true,
        "es2021": true
    },
    "extends": "eslint:recommended",
    "parserOptions":