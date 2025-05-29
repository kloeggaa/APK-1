# BertaPan

<div align="center">
  <img src="app/src/main/res/drawable/logo.png" alt="BertaPan Logo" width="200"/>
</div>

## About

BertaPan is a simple Android application that serves as a basic template for Android development. It demonstrates the fundamental setup of an Android project with a clean and modern user interface.

## Features

- Basic Android application structure
- Clean Material Design implementation
- Custom app icon and branding
- Minimal and lightweight

## Project Structure

The project follows standard Android development practices:
- Java-based Android application
- Gradle build system
- Material Design components integration
- Resource management (drawables, layouts, etc.)

## Linux Setup & Installation

### Prerequisites
1. Install Java Development Kit (JDK):
```bash
sudo apt update
sudo apt install openjdk-17-jdk
```

2. Download and set up Android Command Line Tools:
```bash
# Create Android SDK directory
mkdir -p ~/Android/Sdk
cd ~/Android/Sdk

# Download Command Line Tools
wget https://dl.google.com/android/repository/commandlinetools-linux-9477386_latest.zip
unzip commandlinetools-linux-9477386_latest.zip

# Set up environment variables (add to ~/.bashrc)
export ANDROID_HOME=~/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/cmdline-tools/latest/bin
```

3. Install required Android SDK components:
```bash
# Accept licenses
sdkmanager --licenses

# Install required SDK components
sdkmanager "platform-tools" "platforms;android-33" "build-tools;33.0.2"
```

### Building the Project

1. Clone the repository:
```bash
git clone https://github.com/kloeggaa/APK-1.git
cd APK-1
```

2. Build the project:
```bash
# For debug build
./gradlew assembleDebug

# For release build
./gradlew assembleRelease
```

### Running in Emulator

1. Install Android Emulator components:
```bash
sdkmanager "emulator" "system-images;android-33;google_apis;x86_64"
```

2. Create an Android Virtual Device (AVD):
```bash
# Create a new AVD
avdmanager create avd -n test_device -k "system-images;android-33;google_apis;x86_64"
```

3. Start the emulator:
```bash
# Start emulator in background
emulator -avd test_device &
```

4. Install and run the app:
```bash
# Install debug build
adb install app/build/outputs/apk/debug/app-debug.apk

# Or install release build
adb install app/build/outputs/apk/release/app-release.apk
```

## Development

This project is built with:
- Java
- Android SDK
- Material Design Components
- Gradle build system

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

- Developer: kloeggaa
- Email: no.denial000@passmail.net
- GitHub: [kloeggaa](https://github.com/kloeggaa) 