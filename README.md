# Fakepixel Smooth FPS PRO

Client-only Minecraft Forge 1.8.9 performance-settings mod project.

## Target setup
- Minecraft 1.8.9
- Forge 11.15.1.2318
- Java 8
- Intended launcher: Zalith Launcher on Android

## Included optimizations
- Minimal-particles mode (configurable)
- Entity shadows off (configurable)
- Render distance setting (configurable, 2–16 chunks)
- FPS cap setting (configurable, 30–120 FPS)
- Restores the previous vanilla settings after leaving a world

These settings may reduce rendering load, but cannot guarantee higher FPS or remove network/server lag. This client-side mod does not modify Fakepixel server data or gameplay.

## Build
Use a Java 8 JDK and Gradle 2.14.1 with network access to the Forge Maven repository:

```sh
gradle setupDecompWorkspace
gradle build
```

The compiled JAR is expected in `build/libs/`.

## Honest build status
This package contains source code, not a compiled JAR. The current environment has Java 21, no Gradle installation, and no network/DNS access to fetch the legacy ForgeGradle 2.1 dependencies. It has therefore not been compiled or tested in Minecraft. Do not install this ZIP as a mod.

Configuration file: `config/Fakepixel_Smooth_FPS_PRO.cfg`.

## Build the JAR on Android using GitHub Actions
1. Extract this ZIP.
2. Create a GitHub repository and upload the contents of this project.
3. Open the repository's **Actions** tab.
4. Select **Build Fakepixel Smooth FPS PRO** and tap **Run workflow**.
5. When the workflow finishes, open its run and download the artifact named **Fakepixel-Smooth-FPS-PRO-1.8.9**.
6. Extract the artifact ZIP. The mod JAR is in `build/libs` (or at the top level of the artifact ZIP).
7. Put the JAR in `.minecraft/mods` for your Forge 1.8.9 profile.

Build requirements: Java 8 and Gradle 2.14.1. This project targets Forge 11.15.1.2318. The workflow performs the build; in-game compatibility still needs testing in your launcher.
