# GitHub Pages Setup Guide

Follow these steps to enable GitHub Pages for this repository and make your status page accessible at `https://fahimsadi.github.io/status/`

## Step 1: Merge This PR

1. Review and approve this pull request
2. Merge it to the `main` branch

## Step 2: Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/fahimsadi/status`
2. Click on **Settings** (top menu)
3. In the left sidebar, click **Pages**
4. Under **Build and deployment**:
   - **Source**: Select **GitHub Actions** from the dropdown
5. The workflow will automatically trigger and deploy your site

## Step 3: Wait for Deployment

1. Go to the **Actions** tab in your repository
2. You should see the "Deploy to GitHub Pages" workflow running
3. Wait for it to complete (usually takes 1-2 minutes)
4. Once complete, your site will be live!

## Step 4: Test Your Site

Visit these URLs to test each status:

- ✓ **Approved**: https://fahimsadi.github.io/status/?status=approved
- ⏱ **Expired**: https://fahimsadi.github.io/status/?status=expired
- ✕ **Error**: https://fahimsadi.github.io/status/?status=error

## Using the URLs in Emails

When sending approval emails, use these URLs:

```html
<!-- For approved users -->
<a href="https://fahimsadi.github.io/status/?status=approved">Click here to continue</a>

<!-- For expired links -->
<a href="https://fahimsadi.github.io/status/?status=expired">Link expired</a>

<!-- For errors -->
<a href="https://fahimsadi.github.io/status/?status=error">View error details</a>
```

## Troubleshooting

**Site not showing up?**
- Make sure you've selected "GitHub Actions" as the source in Pages settings
- Check the Actions tab to ensure the workflow completed successfully
- Wait a few minutes for DNS propagation

**Getting 404 errors?**
- Verify the workflow ran successfully
- Check that the `.nojekyll` file is present in the repository
- Try accessing the site in an incognito/private window

**Need to redeploy?**
- Any push to the `main` branch will automatically trigger a new deployment
- Or manually trigger the workflow from the Actions tab

## That's it! 🎉

Your status page is now hosted on GitHub Pages with no external hosting required!
