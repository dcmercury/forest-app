# Submitting PineForest to App Stores

## Quick Reference

```bash
# iOS - Build and Submit
eas build --platform ios --profile production
eas submit --platform ios

# Android - Build and Submit
eas build --platform android --profile production
eas submit --platform android
```

---

## iOS Submission

### Prerequisites
- Apple Developer account
- App created in [App Store Connect](https://appstoreconnect.apple.com)

### Steps

1. **Build the app**
   ```bash
   eas build --platform ios --profile production
   ```
   - Version auto-increments automatically
   - Build runs in EAS cloud (~15-20 min)

2. **Submit to App Store Connect**
   ```bash
   eas submit --platform ios
   ```
   
   **Prompts you'll see:**
   
   - **"What would you like to submit?"** → Select **"Select a build from EAS"**
   - **"Which build would you like to submit?"** → Pick your latest build from the list
   - **"Do you want to log in to your Apple account?"** → Yes
   - **Apple ID** → `chiefhornet@yahoo.com`
   - **Select Team** → Kendall Wouters - Individual
   - **Select Provider** → Kendall Wouters
   
   Build uploads to App Store Connect (~2-5 min)

3. **Complete in App Store Connect**
   - Go to [App Store Connect](https://appstoreconnect.apple.com)
   - Select PineForest → Add build to a new version
   - Fill in release notes, screenshots, etc.
   - Submit for review

---

## Android Submission

### Prerequisites
- Google Play Developer account
- App created in [Google Play Console](https://play.google.com/console)

### Steps

1. **Build the app**
   ```bash
   eas build --platform android --profile production
   ```

2. **Submit to Google Play**
   ```bash
   eas submit --platform android
   ```
   - Select internal/alpha/beta/production track when prompted
   - Provide service account key when prompted

3. **Complete in Google Play Console**
   - Review the uploaded build
   - Add release notes
   - Roll out to selected track

---

## App Identifiers

| Platform | Identifier |
|----------|------------|
| iOS Bundle ID | `com.thepines.pineforest` |
| Android Package | `ai.pineforest.app` |
| Expo Owner | `@thepines` |

---

## Version Management

Versions are managed remotely by EAS:
- `"appVersionSource": "remote"` in `eas.json`
- `"autoIncrement": true` for production builds
- No need to manually update version numbers

---

## Troubleshooting

### "Build not found"
Run `eas build:list` to see available builds, then specify one:
```bash
eas submit --platform ios --id <build-id>
```

### Credentials issues
Re-configure credentials:
```bash
eas credentials
```

### Check build status
```bash
eas build:list
```
