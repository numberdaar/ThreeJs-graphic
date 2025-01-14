# 3D Model Dashboard with Excel Data Integration

This project is a 3D visualization dashboard built with React and Three.js, allowing users to upload Excel files for visualizing node and member data in a 3D environment. It uses React Three Fiber to render 3D objects based on Excel file inputs.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)

## Overview
The application lets users upload an Excel file containing nodes and members data, with each sheet being read and visualized in a 3D canvas. The user can rotate, zoom, and pan the model using the provided 3D controls. The `ExcelReader` component handles reading and parsing Excel files, while the `Fiber` component handles 3D rendering of nodes and connections.

## Features
- **3D Model Rendering**: Display 3D structures from Excel data.
- **Excel Data Parsing**: Use XLSX to read and parse .xlsx files.
- **Orbit Controls**: Allow users to rotate, pan, and zoom the model.
- **Context API**: Global state management for shared Excel data.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/numberdaar/ThreeJs-graphic.git
    cd 3d-model-dashboard
    ```

2. **Install dependencies**:
    ```bash
    npm install
    ```

3. **Start the development server**:
    ```bash
    npm run dev
    ```

4. Open your browser at `http://localhost:3000` to view the dashboard.

## Usage
1. On the dashboard, click "Insert the Excel File" and upload an Excel file containing data.
2. The file should have:
   - **Sheet A** for "members" with "Start Node" and "End Node" columns.
   - **Sheet B** for "nodes" with "Node", "X", "Y", and "Z" columns.
3. Once uploaded, the data will be processed and displayed on the 3D canvas.

## Project Structure
```plaintext
├── public/                     # Static files
│   └── index.html              # Main HTML file
├── src/                        # Source files
│   ├── components/             # Reusable React components
│   │   ├── context.js          # Context for global data management
│   │   ├── Dashboard.jsx       # Main dashboard layout
│   │   ├── ExcelReader.jsx     # Component for file upload and parsing
│   │   └── Fiber.jsx           # 3D model rendering with React Three Fiber
│   ├── App.jsx                 # Main App component
│   ├── index.css               # Global CSS styling
│   └── main.jsx                # Entry point for React app
├── vite.config.js              # Vite configuration
├── package.json                # Project metadata and dependencies
└── README.md                   # This README file
