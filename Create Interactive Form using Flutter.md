# Experiment: Create Interactive Form using Flutter

## Aim
To create an interactive form using Form widget in Flutter.

---

## Theory

Flutter Form is used to collect user input such as name, email, etc.

It allows validation of input fields and provides user interaction.

Key Components:
- Form: Container for input fields
- TextFormField: Used to take input
- GlobalKey: Used for form validation
- ElevatedButton: Used to submit form

---

## Steps to Create Form Application

### Step 1: Create Flutter Project

Open Command Prompt and run:
```
flutter create exp_form
```
### Step 2: Navigate to Project Folder
```
cd exp_form
```
### Step 3: Open Project in VS Code

code .

---

### Step 4: Modify main.dart file

1. Open lib/main.dart
2. Remove default code
3. Paste the following code
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
  final _formKey = GlobalKey<FormState>();
  String name = "";
  String email = "";

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          title: const Text("Form Demo"),
          centerTitle: true,
        ),
        body: Builder(
          builder: (context) => Center(
            child: Padding(
              padding: const EdgeInsets.all(20),
              child: Form(
                key: _formKey,
                child: Column(
                  mainAxisSize: MainAxisSize.min,
                  children: [

                    TextFormField(
                      decoration: const InputDecoration(labelText: "Name"),
                      validator: (value) {
                        if (value!.isEmpty) return "Enter name";
                        return null;
                      },
                      onSaved: (value) => name = value!,
                    ),

                    TextFormField(
                      decoration: const InputDecoration(labelText: "Email"),
                      validator: (value) {
                        if (value!.isEmpty) return "Enter email";
                        return null;
                      },
                      onSaved: (value) => email = value!,
                    ),

                    const SizedBox(height: 15),

                    ElevatedButton(
                      onPressed: () {
                        if (_formKey.currentState!.validate()) {
                          _formKey.currentState!.save();

                          ScaffoldMessenger.of(context).showSnackBar(
                            SnackBar(
                              content: Text("Name: $name, Email: $email"),
                            ),
                          );
                        }
                      },
                      child: const Text("Submit"),
                    ),
                  ],
                ),
              ),
            ),
          ),
        ),
      ),
    );
  }
}
```
---

### Step 5: Run the Application

flutter run

Select Chrome (press 2)

---

## Output

The application displays:

- Input field for Name
- Input field for Email
- Submit button

When the user enters data and clicks Submit:
- Validation is performed
- Data is displayed using Snackbar

---

## Conclusion

Thus, we have successfully created an interactive form using Flutter Form widget.
This experiment helped in understanding user input handling and validation in Flutter applications.
