# User Approval Status Page

A simple, responsive web page that displays user approval status when users click on email verification/approval links.

## 🌐 Live Demo

This page is hosted directly on GitHub Pages. No external hosting required!

**Base URL**: `https://fahimsadi.github.io/status/`

## Features

- **Responsive Design**: Works seamlessly on both mobile phones and desktop computers
- **Multiple Status States**:
  - ✓ **Approved/Success**: Green theme indicating successful approval
  - ⏱ **Link Expired**: Orange theme indicating the link has expired
  - ✕ **Error**: Red theme indicating an error occurred
- **Clean UI**: Modern, animated interface with smooth transitions
- **Mobile-Friendly**: Optimized for all screen sizes
- **GitHub Pages Hosted**: Automatically deployed, no external hosting needed

## Usage

The page uses URL parameters to determine which status to display. Simply add a `status` parameter to the URL:

### Live Examples

1. **Approved/Success Status**:
   ```
   https://fahimsadi.github.io/status/?status=approved
   or
   https://fahimsadi.github.io/status/?status=success
   ```
   [→ Try it now](https://fahimsadi.github.io/status/?status=approved)

2. **Link Expired**:
   ```
   https://fahimsadi.github.io/status/?status=expired
   ```
   [→ Try it now](https://fahimsadi.github.io/status/?status=expired)

3. **Error Status**:
   ```
   https://fahimsadi.github.io/status/?status=error
   ```
   [→ Try it now](https://fahimsadi.github.io/status/?status=error)

## Email Integration

When sending approval emails, include links like:
```
https://fahimsadi.github.io/status/?status=approved
```

The page will automatically display the appropriate status message and styling based on the URL parameter.

## Deployment

This repository is automatically deployed to GitHub Pages via GitHub Actions. Any changes pushed to the `main` branch will be automatically deployed.

### Setup Instructions

1. The repository includes a GitHub Actions workflow (`.github/workflows/pages.yml`) that automatically deploys to GitHub Pages
2. Enable GitHub Pages in repository settings:
   - Go to Settings → Pages
   - Under "Source", select "GitHub Actions"
3. Push changes to the `main` branch to trigger automatic deployment

No build steps or external hosting required!

## Browser Support

Works on all modern browsers including:
- Chrome
- Firefox
- Safari
- Edge
- Mobile browsers (iOS Safari, Chrome Mobile, etc.)