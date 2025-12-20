# InkThis App

Expo WebView wrapper for [inkthis.ai](https://inkthis.ai).

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

- **Expo Project:** @thepines/inkthis
- **iOS Bundle ID:** com.thepines.inkthis
- **Android Package:** ai.inkthis.app
