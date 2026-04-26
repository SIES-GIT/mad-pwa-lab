# Experiment: Basic Calculator App using Flutter

## Aim
To develop a basic calculator application using Flutter.

---

## Theory

Flutter is a UI toolkit developed by Google used to build cross-platform applications.

In this experiment, a calculator app is developed using Flutter widgets such as TextField, Button, and Text.

---

## Requirements

- Flutter SDK
- VS Code

---

## Steps to Perform

### Step 1: Create Project
```
flutter create calculator_app
```
```
cd calculator_app
```
---

### Step 2: Write Code

Replace main.dart with calculator logic using buttons and input fields.

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
  final t1 = TextEditingController();
  final t2 = TextEditingController();

  String result = "";

  void calculate(String op) {
    double num1 = double.parse(t1.text);
    double num2 = double.parse(t2.text);

    setState(() {
      if (op == "+") result = (num1 + num2).toString();
      if (op == "-") result = (num1 - num2).toString();
      if (op == "*") result = (num1 * num2).toString();
      if (op == "/") {
        if (num2 != 0) {
          result = (num1 / num2).toString();
        } else {
          result = "Cannot divide by 0";
        }
      }
    });
  }

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          title: const Text("Calculator App"),
          centerTitle: true,
        ),
        body: Padding(
          padding: const EdgeInsets.all(20),
          child: Column(
            children: [
              TextField(
                controller: t1,
                keyboardType: TextInputType.number,
                decoration: const InputDecoration(labelText: "Enter number 1"),
              ),
              TextField(
                controller: t2,
                keyboardType: TextInputType.number,
                decoration: const InputDecoration(labelText: "Enter number 2"),
              ),

              const SizedBox(height: 20),

              Row(
                mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                children: [
                  ElevatedButton(onPressed: () => calculate("+"), child: const Text("+")),
                  ElevatedButton(onPressed: () => calculate("-"), child: const Text("-")),
                  ElevatedButton(onPressed: () => calculate("*"), child: const Text("*")),
                  ElevatedButton(onPressed: () => calculate("/"), child: const Text("/")),
                ],
              ),

              const SizedBox(height: 30),

              Text(
                "Result: $result",
                style: const TextStyle(fontSize: 22, fontWeight: FontWeight.bold),
              )
            ],
          ),
        ),
      ),
    );
  }
}
```

---

### Step 3: Run Application
```
flutter run
```
---

## Output

The application takes two numbers as input and performs:

- Addition
- Subtraction
- Multiplication
- Division

Result is displayed on screen dynamically.

---

## Conclusion

Thus, a basic calculator application was successfully developed using Flutter.
