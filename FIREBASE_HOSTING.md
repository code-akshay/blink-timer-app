# Firebase Hosting Setup

This repo is configured so the site root is deployed directly to Firebase Hosting.

After deployment, AdMob should be able to read:

`https://YOUR_SITE.web.app/app-ads.txt`

## 1. Create a Firebase project

Create or select a Firebase project in the Firebase console.

Pick a project ID you want to use for hosting, for example:

`blinktimer-app`

## 2. Update `.firebaserc`

Replace the placeholder project ID in `.firebaserc`:

```json
{
  "projects": {
    "default": "your-project-id"
  }
}
```

## 3. Install the Firebase CLI

```bash
npm install -g firebase-tools
```

## 4. Log in and deploy

From this repo:

```bash
firebase login
firebase deploy --only hosting
```

## 5. Verify the live file

Open:

`https://YOUR_PROJECT_ID.web.app/app-ads.txt`

and confirm it loads with your real AdMob publisher ID.

## 6. Update your store listing

Use the Firebase Hosting site URL as the developer website / marketing URL for the app.

Then wait for AdMob to recrawl the file. Google says this can take at least 24 hours and sometimes longer.
