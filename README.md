# RotaryPay Web Redirect Page

This is a web redirect page for the RotaryPay application's authentication flows. It handles email confirmation, password reset, and other authentication redirects from Supabase.

## Purpose

When users receive authentication emails (like email confirmation or password reset) and click on the links, this page:

1. Captures the authentication parameters from the URL
2. Attempts to redirect to the RotaryPay mobile app using the custom URL scheme
3. Provides a fallback UI if the app isn't installed on the device

## How It Works

The page uses JavaScript to:
- Extract authentication parameters from the URL
- Create a deep link with the custom URL scheme `rotarytransactionapp://`
- Redirect the user to the app
- Show a helpful message if redirection doesn't happen automatically

## Deployment

This page should be deployed to a web hosting service like Vercel, Netlify, or GitHub Pages. After deployment, update your Supabase project settings to use this URL for redirects.

## Configuration

In your Supabase dashboard:
1. Go to Authentication → URL Configuration
2. Set the Site URL to your deployed web page URL
3. Add the same URL to the Redirect URLs list
