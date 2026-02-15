# User Approval Status Page

A simple, responsive web page that displays user approval status when users click on email verification/approval links.

## Features

- **Responsive Design**: Works seamlessly on both mobile phones and desktop computers
- **Multiple Status States**:
  - ✓ **Approved/Success**: Green theme indicating successful approval
  - ⏱ **Link Expired**: Orange theme indicating the link has expired
  - ✕ **Error**: Red theme indicating an error occurred
- **Clean UI**: Modern, animated interface with smooth transitions
- **Mobile-Friendly**: Optimized for all screen sizes

## Usage

The page uses URL parameters to determine which status to display. Simply add a `status` parameter to the URL:

### Examples

1. **Approved/Success Status**:
   ```
   https://yourdomain.com/index.html?status=approved
   or
   https://yourdomain.com/index.html?status=success
   ```

2. **Link Expired**:
   ```
   https://yourdomain.com/index.html?status=expired
   ```

3. **Error Status**:
   ```
   https://yourdomain.com/index.html?status=error
   ```

## Email Integration

When sending approval emails, include links like:
```
https://yourdomain.com/index.html?status=approved
```

The page will automatically display the appropriate status message and styling based on the URL parameter.

## Deployment

Simply upload the `index.html` file to your web server or hosting platform. No additional dependencies or build steps required.

## Browser Support

Works on all modern browsers including:
- Chrome
- Firefox
- Safari
- Edge
- Mobile browsers (iOS Safari, Chrome Mobile, etc.)