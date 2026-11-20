# Mindly AI – Android app

## Step 1: Deploy the server (holds your API key)
1. Get an API key at console.anthropic.com.
2. Upload the `server` folder to Render, Railway or Fly.io (all have free/cheap tiers).
3. Set environment variable ANTHROPIC_API_KEY = your key. Start command: npm start
4. Copy the https URL it gives you.

## Step 2: Connect the app
Open www/index.html and set API_URL to your server URL.

## Step 3: Build the Android app
Install Node 18+, Android Studio, then in this folder:

    npm install
    npx cap add android
    npx cap sync
    npx cap open android

In Android Studio: Build > Generate Signed Bundle / APK > Android App Bundle (.aab).
Create and SAVE your keystore file and passwords safely. You need them for every update.

## Step 4: Play Store
- Upload the .aab in Play Console (use a NEW package name, not your existing app's).
- Google requires AI apps to let users report offensive AI content, so add a
  "Report" button/link (e.g. a mailto link) before submitting.
- Fill in the privacy policy and Data safety form (messages are sent to your server).
