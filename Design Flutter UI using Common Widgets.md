# Experiment 2: Design Flutter UI using Common Widgets

## Aim
To design Flutter UI by including common widgets such as Text, Buttons, Container, Scaffold, AppBar, Row and Column.

## Theory

Flutter UI is built using widgets. Widgets are the basic building blocks of a Flutter application.

There are two types of widgets:

1. Stateless Widget:
These widgets do not change during runtime. Their properties remain constant.

2. Stateful Widget:
These widgets can change their state during runtime based on user interaction or data.

Common widgets used:
- Text: Displays text on screen
- Container: Used for styling and layout
- AppBar: Top bar of the application
- Scaffold: Basic structure of app
- Row: Horizontal layout
- Column: Vertical layout

## Steps to Create Flutter UI

### Step 1: Create Flutter Project

1. Open Command Prompt.
2. Run the command:
```
   flutter create myapp
```
3. Navigate to project folder:
```
   cd myapp
```
4. Open project in VS Code.

### Step 2: Modify main.dart file

1. Go to lib folder.
2. Open main.dart file.
3. Remove the default code.
4. Paste the following code:
```
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatefulWidget {
  const MyApp({super.key});

  @override
  State<MyApp> createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  String message = "Hello Flutter";

  void changeText() {
    setState(() {
      message = "Button Pressed!";
    });
  }

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          title: const Text("My Flutter App"),
          centerTitle: true,
        ),
        body: Center(
          child: Container(
            padding: const EdgeInsets.all(20),
            color: Colors.blue, // change this color
            child: Column(
              mainAxisSize: MainAxisSize.min,
              children: [
                Text(
                  message,
                  style: const TextStyle(color: Colors.white, fontSize: 18),
                ),
                const SizedBox(height: 10),
                ElevatedButton(
                  onPressed: changeText,
                  child: const Text("Press"),
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
### Step 3: Run the Application

1. Open terminal in VS Code.
2. Run the command:
```
   flutter run
```
4. Select Chrome (press 2).
5. The application will launch in the browser.

## Output

The application displays a simple user interface with:

- AppBar at the top with title "My Flutter App"
- A colored container in the center
- Text displayed inside the container
- A button below the text

When the button is clicked, the text changes dynamically.

## Conclusion

Thus, we have successfully designed a Flutter UI using common widgets such as MaterialApp, Scaffold, AppBar, Container, Text, Column, and Button. 
This experiment helped in understanding the basic structure of a Flutter application and how widgets are used to build UI.
