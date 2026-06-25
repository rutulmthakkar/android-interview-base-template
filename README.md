# Android Interview Base Template

A pre-configured Android project template built with modern Android development best practices. Clone this repo at the start of any coding interview to skip boilerplate setup and focus on the actual problem.

## What's Included

| Layer | Library | Version |
|---|---|---|
| UI | Jetpack Compose + Material 3 | BOM 2025.02.00 |
| DI | Hilt | 2.55 |
| Navigation | Navigation Compose | 2.8.7 |
| Networking | Retrofit 2 + OkHttp (logging interceptor) | 2.11.0 / 4.12.0 |
| Image Loading | Coil 3 (Compose + OkHttp backend) | 3.0.4 |
| Local DB | Room | 2.6.1 |
| Unit Testing | JUnit 4 + MockK | 4.13.2 / 1.14.11 |
| Instrumented Testing | Espresso + Compose UI Test | — |

### Architecture & Tooling
- **Language**: Kotlin 2.1.0
- **Build system**: Gradle 9.4.1 with Kotlin DSL (`build.gradle.kts`)
- **Dependency catalog**: `gradle/libs.versions.toml`
- **Annotation processing**: KSP (Kotlin Symbol Processing)
- **Edge-to-edge UI** enabled by default

## Android OS Support

| Property | Value |
|---|---|
| `minSdk` | 24 (Android 7.0 Nougat) |
| `targetSdk` | 35 (Android 15) |
| `compileSdk` | 35 |
| **JVM target** | Java 17 |

Covers ~98% of active Android devices.

## Project Structure

```
app/src/main/java/com/example/basetemplate/
├── MainActivity.kt          # Entry point, Compose host
├── MainApplication.kt       # @HiltAndroidApp application class
└── ui/theme/
    ├── Color.kt
    ├── Theme.kt
    └── Type.kt
```

## How to Use for an Interview

1. Clone the repo and open in Android Studio.
2. Rename the package if needed (`com.example.basetemplate` → your preferred namespace).
3. Start building — Hilt, Room, Retrofit, Navigation, and Coil are all wired up and ready.

### Suggested folder structure to add

```
feature/
├── data/
│   ├── local/        # Room DAOs, entities
│   ├── remote/       # Retrofit API interfaces, DTOs
│   └── repository/
├── domain/
│   ├── model/
│   └── usecase/
└── presentation/
    ├── screen/
    └── viewmodel/
```

## Requirements

- Android Studio Hedgehog (2023.1.1) or newer
- JDK 17+
