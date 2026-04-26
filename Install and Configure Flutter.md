# Experiment 1: Install and Configure Flutter Environment

## Aim
To install and configure Flutter environment in Windows.

## Theory
Cross-platform application development allows building a single application that runs on multiple operating systems using one codebase. This reduces development time and cost.

Flutter is an open-source framework developed by Google used to build cross-platform applications. It uses Dart programming language and provides near-native performance.

Dart is an object-oriented, strongly typed programming language used to build UI for mobile and web applications.

## Requirements

- Windows OS
- Internet connection
- VS Code or Android Studio
- Git (optional but recommended)

## Steps to Install Flutter

### Step 1: Download Flutter SDK

Click the link below to open Flutter installation page:

https://docs.flutter.dev/install/windows

1. Open the link above.
2. Scroll down to "Download the Flutter SDK bundle".
3. Click on the download button:
   flutter_windows_3.41.7-stable.zip
4. Wait for the ZIP file to download.

### Step 2: Extract Flutter SDK

1. Go to Downloads folder.
2. Locate the downloaded ZIP file (flutter_windows_3.41.7-stable.zip).
3. Right-click on the file.
4. Click on "Extract All".
5. Choose a location like:
   C:\flutter
6. Click Extract.

### Step 3: Set Environment Variable (PATH)

1. Press Windows key and search "Environment Variables".
2. Click on "Edit the system environment variables".
3. Click on "Environment Variables".
4. Under System Variables, find "Path" and click Edit.
5. Click on "New".
6. Add this path:
   C:\flutter\bin
7. Click OK and save all settings.

### Step 4: Verify Installation

1. Open Command Prompt.
2. Type the following command:
```
   flutter doctor
```
3. Press Enter.

### Why flutter doctor is used?

The flutter doctor command is used to check whether the Flutter environment is properly installed and configured.
It scans the system and verifies required dependencies such as Flutter SDK, Android toolchain, and connected devices. 
It also shows errors and suggestions to fix setup issues.

### Output

After running flutter doctor:

- Flutter installed successfully
- Some components may show errors like:
  - Android toolchain (not installed)
  - Visual Studio (not installed)

These can be ignored for basic setup.

### Final Verification

Run the command:
```
flutter --version
```
If version is displayed, Flutter is successfully installed.
