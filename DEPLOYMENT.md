# OxPNS Website Deployment Guide

## Overview
This website is built using static HTML, CSS, and can be deployed to GitHub Pages or any static hosting service.

## Structure
```
/
├── index.html              # Home page
├── course-details.html     # Course Details page
├── registration.html       # Registration page
├── styles.css              # All styling
├── images/                 # Images directory
│   └── README.md          # Instructions for image uploads
└── README.md              # Project documentation
```

## Required Actions Before Deployment

### 1. Upload Images
Add the following images to the `images/` directory:
- `oxford-banner.jpg` - Oxford University banner for home page hero section
- `network-figure.jpg` - Network figure for left and right sidebars on home page
- `course-image.jpg` - Image for left side of Course Details page
- `registration-image.jpg` - Image for left side of Registration page

### 2. Update Registration Links
In `registration.html`, update the Google Form URL in two locations:
- Line 46: Main registration button
- Line 91: Bottom call-to-action button

Replace `https://forms.google.com/your-form-link` with your actual Google Form URL.

### 3. Update Dates
In `registration.html`, line 60, replace `[DATE]` with the actual early bird registration deadline.

## Deploying to GitHub Pages

### Option 1: Deploy from main branch
1. Go to repository Settings
2. Navigate to Pages section
3. Under "Source", select "Deploy from a branch"
4. Choose "main" branch and "/ (root)" folder
5. Click Save
6. Your site will be available at: `https://omidvebrahimi.github.io/OxfordPNS/`

### Option 2: Deploy from gh-pages branch
1. Create a new `gh-pages` branch
2. Copy all website files to the branch
3. Go to repository Settings > Pages
4. Select "gh-pages" branch
5. Your site will be available at: `https://omidvebrahimi.github.io/OxfordPNS/`

## Testing Locally

To test the website locally:

```bash
# Using Python 3
python3 -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (requires http-server package)
npx http-server

# Using PHP
php -S localhost:8000
```

Then open your browser to `http://localhost:8000`

## Browser Compatibility
The website is compatible with:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Customization

### Colors
The website uses Oxford University's official color:
- Primary: `#002147` (Oxford Blue)
- Secondary: `#003d6b` (Lighter Oxford Blue)

To change colors, edit the values in `styles.css`.

### Content
All content is in the HTML files and can be edited directly. The structure is semantic and clearly commented.

## Support
For questions or issues, contact: info@oxpns.org
