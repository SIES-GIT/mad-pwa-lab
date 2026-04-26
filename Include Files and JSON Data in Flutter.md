# Experiment: Include Files and JSON Data in Flutter

## Aim
To include files and JSON data in a Flutter application.

---

## Theory

In Flutter, external files such as JSON can be stored in the assets folder and used within the application.

JSON (JavaScript Object Notation) is a lightweight data format used to store structured data.

Steps involved:
- Store JSON file in assets
- Declare it in pubspec.yaml
- Load using rootBundle
- Convert JSON into Dart object using dart:convert

---

## Requirements

- Flutter SDK
- VS Code or Android Studio

---

## Steps to Implement

### Step 1: Create Flutter Project
```
flutter create exp_json
```
### Step 2: Navigate to Project Folder
```
cd exp_json
```
### Step 3: Open in VS Code

code .

---

### Step 4: Create JSON File

1. Create a folder named "assets"
2. Inside it create a file named data.json
3. Add the following content:
```
{
"name": "Flutter App",
"version": "1.0.0",
"features": ["offline mode", "dark theme", "multi-language"]
}
```

---

### Step 5: Declare Assets

Open pubspec.yaml and add:

flutter:
  assets:
  ```
    - assets/data.json
```
---

### Step 6: Modify main.dart

Replace the default code with:
```
import 'package:flutter/material.dart';
import 'dart:convert';
import 'package:flutter/services.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatefulWidget {
  const MyApp({super.key});

  @override
  State<MyApp> createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  String data = "";

  @override
  void initState() {
    super.initState();
    loadJson();
  }

  Future<void> loadJson() async {
    final String response = await rootBundle.loadString('assets/data.json');
    final jsonData = json.decode(response);

    setState(() {
      data = jsonData["name"];
    });
  }

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          title: const Text("JSON Demo"),
        ),
        body: Center(
          child: Text(data),
        ),
      ),
    );
  }
}
```

---

### Step 7: Run the Application
```
flutter run
```
Select Chrome (press 2)

---

## Output

The application loads JSON data from file and displays:

- The value of "name" from JSON file
- Example output: Flutter App

---

## Explanation

- JSON file is stored in assets folder
- rootBundle is used to read file
- dart:convert is used to decode JSON
- Data is displayed using Text widget

---

## Conclusion

Thus, we have successfully included a JSON file in Flutter and displayed its data in the application. This experiment helped in understanding file handling and data parsing in Flutter.

