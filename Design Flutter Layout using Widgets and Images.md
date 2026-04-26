# Experiment 4: Design Flutter Layout using Widgets and Images

## Aim
To design a layout of Flutter App using layout widgets and images.

## Theory

Flutter layout is built using widgets. Layout widgets help in arranging UI elements on the screen.

Types of layout widgets:

1. Single Child Widgets:
Center, Container, Padding, Align

2. Multiple Child Widgets:
Row, Column, ListView, GridView

These widgets help in designing structured and responsive user interfaces.

## Steps to Create Flutter Layout Project

### Step 1: Create Flutter Project

1. Open Command Prompt.
2. Run the command:
```
   flutter create exp3_layout
```
### Step 2: Navigate to Project Folder
```
cd exp3_layout
```
### Step 3: Open Project in VS Code

code .

### Step 4: Add Image to Project

1. Create a new folder named "assets" in the project root.
2. Add an image file inside the folder (example: image.png).
3. Open pubspec.yaml file.
4. Add the following lines:

flutter:

  assets:
```
    - assets/image.png
```
### Step 5: Design UI Layout

1. Go to lib folder.
2. Open main.dart file.
3. Remove the default code.
4. Paste the following code:

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
          title: const Text("Layout with Image"),
          centerTitle: true,
        ),
        body: Center(
          child: Container(
            padding: const EdgeInsets.all(20),
            decoration: BoxDecoration(
              color: Colors.lightBlue,
              borderRadius: BorderRadius.circular(15),
            ),
            child: Column(
              mainAxisSize: MainAxisSize.min,
              children: [
                Image.asset(
                  'assets/image.png',
                  height: 120,
                ),
                const SizedBox(height: 10),
                const Text(
                  "Flutter Layout Demo",
                  style: TextStyle(fontSize: 18, color: Colors.white),
                ),
              ],
            ),
          ),
        ),
      ),
    );
  }
}
```
### Step 6: Run the Application

flutter run

Select Chrome (press 2)

---

## Output

The application displays:

- AppBar with title
- A colored container in center
- Image displayed inside container
- Text below the image

---

## Conclusion

Thus, we have successfully designed a Flutter layout using widgets like Container, 
Column, Center, and Image. This experiment helped in understanding layout design 
and image integration in Flutter applications.
