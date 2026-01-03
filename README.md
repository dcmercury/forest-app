# PineForest App

Expo WebView wrapper for [pineforest.ai](https://pineforest.ai).

## Build

```bash
# iOS
eas build --platform ios --profile production
eas submit --platform ios

# Android
eas build --platform android --profile production
eas submit --platform android
```

## Development

```bash
npm install
npx expo start
```

## Configuration

- **Expo Project:** @thepines/pineforest
- **iOS Bundle ID:** com.thepines.pineforest
- **Android Package:** ai.pineforest.app
