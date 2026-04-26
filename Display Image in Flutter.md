# Experiment 3: Display Image in Flutter

## Aim
To display an image in Flutter application.

## Theory

Flutter allows displaying images using Image widget.

Images can be loaded from assets folder using Image.asset().

Assets must be declared in pubspec.yaml file.

---

## Steps to Create Image Application

### Step 1: Create Flutter Project

flutter create exp3_image

### Step 2: Navigate to Project Folder

cd exp3_image

### Step 3: Open in VS Code

code .

---

### Step 4: Add Image to Project

1. Create a folder named "assets"
2. Add an image file (image.png)
3. Open pubspec.yaml
4. Add:

flutter:
  assets:
```
    - assets/image.png
```
---

### Step 5: Modify main.dart

1. Open lib/main.dart
2. Remove default code
3. Paste the following code
```
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          title: const Text("Image Demo"),
          centerTitle: true,
        ),
        body: Center(
          child: Image.asset('assets/image.png'),
        ),
      ),
    );
  }
}
```
---

### Step 6: Run the Application

flutter run

Select Chrome (press 2)

---

## Output

The application displays an image at the center of the screen.

---

## Conclusion

Thus, we have successfully displayed an image in Flutter using Image widget. This experiment helped in understanding how to use assets in Flutter applications.
