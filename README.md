# flashmd-android

Android flashcard app that parses Markdown files into decks and studies them using SM-2 spaced repetition. Fully local, no backend.

## Requirements

- Android Studio Hedgehog or later
- Android SDK 26+
- JDK 17

## Build & Run

```bash
git clone https://github.com/johnfire/flashmd-android
cd flashmd-android

# Generate Gradle wrapper (requires Gradle 8.7 installed locally)
gradle wrapper

# Build debug APK
./gradlew assembleDebug

# Install on connected device/emulator
./gradlew installDebug
```

Or open the project in Android Studio and click **Run**.

## Markdown Format

A single `.md` file = one deck. Cards follow this pattern:

```
# Deck Title

## Category Name

**1. TERM — Full Term Name**
Definition paragraph.

Second paragraph if needed.
```

## Running Unit Tests

```bash
./gradlew test
```

## Tech Stack

| Layer | Choice |
|-------|--------|
| Language | Kotlin |
| UI | Jetpack Compose + Material3 |
| Database | Room (SQLite) |
| DI | Hilt |
| Navigation | Compose Navigation |
| Architecture | MVVM + Repository |
| Min SDK | 26 (Android 8) |

## License

MIT — Copyright (c) 2025 Christopher Rehm
