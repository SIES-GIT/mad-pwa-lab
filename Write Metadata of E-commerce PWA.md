# Experiment: Write Metadata of E-commerce PWA Web App Manifest

## Aim
To write metadata of an E-commerce PWA web app manifest.

---

## Theory

Flutter is an open-source UI toolkit used to build cross-platform applications.

Flutter Web allows applications to run inside a browser and can be converted into a Progressive Web App (PWA).

In Flutter PWA:

- lib/main.dart → main application code  
- web/manifest.json → metadata for PWA  
- index.html → entry point  

The manifest.json file contains metadata such as app name, icons, theme color, and start URL.

---

## Steps to Implement

### Step 1: Create Flutter Project
```
flutter create exp_pwa
```
### Step 2: Navigate to Project Folder
```
cd exp_pwa
```
### Step 3: Open in VS Code

code .

---

### Step 4: Locate Manifest File

Go to:

web → manifest.json

---

### Step 5: Modify manifest.json
```
{
"name": "ShopEase Online Store",
"short_name": "ShopEase",
"description": "A fast, reliable, and engaging e-commerce PWA for shopping online.",
"start_url": "/index.html",
"scope": "/",
"display": "standalone",
"orientation": "portrait",
"background_color": "#ffffff",
"theme_color": "#1a73e8",
"lang": "en",
"dir": "ltr",
"prefer_related_applications": false,
"categories": ["shopping", "ecommerce", "retail"],
"icons": [
{
"src": "/icons/icon-192.png",
"sizes": "192x192",
"type": "image/png"
},
{
"src": "/icons/icon-512.png",
"sizes": "512x512",
"type": "image/png"
}
],
"screenshots": [
{
"src": "/screenshots/home.png",
"sizes": "1080x1920",
"type": "image/png"
}
]
}
```


---

---

### Step 6: Modify main.dart

1. Go to lib folder
2. Open main.dart file
3. Remove default code
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
          title: const Text("ShopEase Online Store"),
          centerTitle: true,
        ),
        body: Padding(
          padding: const EdgeInsets.all(10),
          child: GridView.count(
            crossAxisCount: 2,
            crossAxisSpacing: 10,
            mainAxisSpacing: 10,
            children: const [
              ProductCard(name: "Shoes", price: "\$49"),
              ProductCard(name: "Watch", price: "\$99"),
              ProductCard(name: "Bag", price: "\$79"),
              ProductCard(name: "Headphones", price: "\$59"),
            ],
          ),
        ),
      ),
    );
  }
}

class ProductCard extends StatelessWidget {
  final String name;
  final String price;

  const ProductCard({super.key, required this.name, required this.price});

  @override
  Widget build(BuildContext context) {
    return Container(
      decoration: BoxDecoration(
        color: Colors.white,
        borderRadius: BorderRadius.circular(15),
        boxShadow: const [
          BoxShadow(color: Colors.grey, blurRadius: 5)
        ],
      ),
      child: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          const Icon(Icons.shopping_bag, size: 40, color: Colors.blue),
          const SizedBox(height: 10),
          Text(name),
          Text(price),
          const SizedBox(height: 10),
          ElevatedButton(
            onPressed: () {},
            child: const Text("Add to Cart"),
          )
        ],
      ),
    );
  }
}
```
### Step 7: Run the Application

flutter run

Select Chrome (press 2)

---

## Output

The application displays an e-commerce layout with:

- Product cards arranged in grid format
- Each card shows product name, price and icon
- "Add to Cart" button for each product

---

## Conclusion

Thus, a Flutter web application was successfully created and executed. The experiment demonstrates PWA configuration using manifest.json and understanding of Flutter web structure.

Replace the existing content with:
