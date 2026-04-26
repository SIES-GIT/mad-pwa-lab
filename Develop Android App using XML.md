# Experiment: Develop Android App using XML

## Aim
To develop Android application using XML in Android Studio.

---

## Theory

Android applications use XML (Extensible Markup Language) to design user interface.

XML defines layout of the application such as TextView, Button, ImageView, etc.

It separates design from logic, where:
- XML → UI design
- Java/Kotlin → functionality

All XML layout files are stored inside:
res/layout folder

---

## Requirements

- Android Studio
- Java or Kotlin support
- Emulator or physical device

---

## Steps to Develop Android App

### Step 1: Open Android Studio

1. Open Android Studio
2. Click on "New Project"

---

### Step 2: Create New Project

1. Select "Empty Activity"
2. Click Next
3. Enter project name (e.g., ExpXMLApp)
4. Select Language: Java or Kotlin
5. Click Finish
6. Wait for project to load

---

### Step 3: Locate XML File

1. Go to:
   app → res → layout → activity_main.xml
2. Open activity_main.xml file

---

### Step 4: Design UI using XML

1. Remove existing code
2. Paste the following code:

```
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="20dp">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello Android"
        android:textSize="24sp"/>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Click Me"/>

</LinearLayout>
```
### Step 5: Run the Application

1. Click on the Run (▶️) button in Android Studio.
2. Select an available device or emulator.
3. Wait for the application to build and launch.

---

## Output

After running the application, the following output is observed:

- A screen appears with a clean user interface.
- A TextView displaying the text "Hello Android" is shown.
- A Button labeled "Click Me" is displayed below the text.
- Both components are aligned at the center of the screen.
- The layout is arranged vertically using LinearLayout.

---

## Explanation of Output

- LinearLayout is used with vertical orientation, so elements are placed one below another.
- The gravity property is set to "center", which aligns all components to the center of the screen.
- TextView is used to display static text.
- Button is used for user interaction (clickable element).

---

## Conclusion

Thus, we have successfully designed and executed an Android user interface using XML in Android Studio. 
This experiment helped in understanding how UI components are arranged and displayed using layout structures in Android applications.
