# Experiment: Deploy Flutter PWA to GitHub Pages

## Aim
To deploy a Flutter web application (PWA) on GitHub Pages.

## Theory

GitHub Pages is a hosting service that allows deployment of static web applications.

Flutter web apps can be deployed by building the project and uploading the build files to a GitHub repository.

The build/web folder contains the final deployable files.

## Steps to Deploy Application

### Step 1: Build Flutter Web Application

Open terminal and run:
```
flutter build web
```
This will generate a build/web folder containing deployable files.

### Step 2: Create GitHub Repository

1. Open GitHub
2. Click on "New Repository"
3. Enter repository name (e.g., pwa-deploy)
4. Select Public
5. Click on Create Repository

### Step 3: Initialize Git and Push Code

Open terminal in project folder and run:

git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/USERNAME/pwa-deploy.git
git push -u origin main

