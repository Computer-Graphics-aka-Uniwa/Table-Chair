<p align="center">
  <img src="https://www.especial.gr/wp-content/uploads/2019/03/panepisthmio-dut-attikhs.png" alt="UNIWA" width="150"/>
</p>

<p align="center">
  <strong>UNIVERSITY OF WEST ATTICA</strong><br>
  SCHOOL OF ENGINEERING<br>
  DEPARTMENT OF COMPUTER ENGINEERING AND INFORMATICS
</p>

<p align="center">
  <a href="https://www.uniwa.gr" target="_blank">University of West Attica</a> ·
  <a href="https://ice.uniwa.gr" target="_blank">Department of Computer Engineering and Informatics</a>
</p>

<hr/>

<p align="center">
  <strong>Computer Graphics</strong>
</p>

<h1 align="center" style="letter-spacing: 1px;">
  Building a 3D Graphics Scene Using WebGL
</h1>

<p align="center">
  <strong>Vasileios Evangelos Athanasiou</strong><br>
  Student ID: 19390005
</p>

<p align="center">
  <a href="https://github.com/Ath21" target="_blank">GitHub</a> ·
  <a href="https://www.linkedin.com/in/vasilis-athanasiou-7036b53a4/" target="_blank">LinkedIn</a>
</p>

<p align="center">
  <strong>Antonios Kokkinos</strong><br>
  Student ID: 20390107
</p>

<p align="center">
  <a href="https://github.com/KokkinosAntonios" target="_blank">GitHub</a>
</p>

<p align="center">
  <strong>Pantelis Tatsis</strong><br>
  Student ID: 20390226
</p>

<p align="center">
  <a href="https://github.com/PanthegrammerPRO" target="_blank">GitHub</a> ·
  <a href="https://www.linkedin.com/in/pantelis-tatsis-8287852a2/" target="_blank">LinkedIn</a>
</p>

<hr>

<p align="center">
  <strong>Supervision</strong>
</p>

<p align="center">
  Supervisor: Georgios Bardis, Assistant Professor
</p>
<p align="center">
  <a href="https://ice.uniwa.gr/en/emd_person/georgios-bardis/" target="_blank">UNIWA Profile</a>
</p>

</hr>

---

<p align="center">
  Athens, July 2024
</p>

---

<p align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ2ucmdAju5MLVQg4nm-x5ZguP512FUmlGY0w&s" width="250"/>
</p>

---

# INSTALL

## Building a 3D Graphics Scene Using WebGL

This project is a **pure WebGL (HTML + JavaScript)** application and does **not require compilation** or external build tools.  
It runs directly in a modern web browser with **WebGL support**.

---

## 1. Prerequisites

Before running the project, ensure the following requirements are met.

### 1.1 Software Requirements

- **Modern Web Browser** with WebGL enabled:
  - Google Chrome
  - Mozilla Firefox (recommended)
  - Microsoft Edge
- **Local HTTP Server (required for texture loading)**

> **Important**  
> Due to browser security restrictions, WebGL **cannot load textures correctly** when HTML files are opened directly (`file://`).  
> A **local web server is mandatory**.

---

## 2. Repository Setup

### 2.1 Clone the Repository

```bash
git clone https://github.com/Computer-Graphics-aka-Uniwa/Table-Chair.git
```

Alternatively, download the repository as a ZIP archive and extract it locally.

### 2.2 Running the Project

Option 1: Using VS Code Live Server (Recommended)

1. Open the project folder in Visual Studio Code
2. Install the Live Server extension
3. Navigate to:

```bash
src/*_scene.html
```

4. Right-click the file and select "Open with Live Server"
5. The scene you chose will open automatically in your default browser

### 2.3 Using Node.js HTTP Server

If Node.js is installed:

```bash
npm install -g http-server
cd Table-Chair/src
http-server
```

Open the displayed local URL and load the scene you desire.

---

## 3. Controls and Interaction

### 3.1 Scene 1

Camera Controls

- **View Angle**  
  Adjusts the camera’s field of view (degrees)

- **Orthogonal Distance**  
  Controls the distance of the camera from the scene center

- **Camera Position (Radio Buttons)**  
  Select predefined camera viewpoints around the object

- **Redraw**  
  Re-renders the scene with the selected parameters

Interaction Notes

- Scene 1 is static and does not support animation
- No mouse interaction is required
- Camera changes apply immediately after redraw

### 3.2 Scene 2

Camera Controls

- **View Angle**  
  Adjusts the camera’s field of view (degrees)

- **Orthogonal Distance**  
  Controls the distance of the camera from the scene center

- **Camera Position (Radio Buttons)**  
  Select predefined camera viewpoints

- **Redraw**  
  Re-renders the scene with the selected parameters

Interaction Notes

- Scene 2 remains static
- The table and chair are positioned using fixed transformations
- No real-time interaction or animation is present

### 3.3 Scene 3

Camera Controls

- **View Angle**  
  Adjusts the camera’s field of view (degrees)

- **Orthogonal Distance**  
  Controls the distance of the camera from the scene center

- **Camera Position (Radio Buttons)**  
  Select predefined camera viewpoints

- **Redraw**  
  Re-renders the scene with the selected parameters

Interaction Notes

- Scene 3 introduces textured objects but remains static
- No mouse-based interaction is required
- Texture changes are loaded automatically on scene initialization

### 3.3 Scene 4

Camera Controls

- **Mouse Drag**
  Horizontal movement → Rotate camera around the scene
  Vertical movement → Move camera height (Z-axis)

- **Mouse Wheel**
  Tilt the chair forward and backward (0°–90°)

- **UI Controls**
  View Angle: Adjusts the camera’s field of view (degrees)
  Orthogonal Distance: Controls camera distance from the scene center
  Camera Position (Radio Buttons): Select predefined camera viewpoints
  Redraw: Re-renders the scene with the selected parameters
  Start / Stop: Enables or disables automatic camera rotation

---

## 4. Textures

### 4.1 Texture and Asset Notes

All textures are located in:

```bash
src/textures/
```

Texture characteristics:

- JPEG format
- Power-of-two dimensions (e.g., 512×512)

These constraints ensure:

- Correct mipmap generation
- Prevention of black-texture rendering issues in WebGL

---

## 5. Issues and Evaluation

### 5.1 Scene appears black or textures do not load

- Ensure the project is served via HTTP, not opened directly as a file.

### 5.2 Mouse interaction not responding

- Click inside the canvas first to activate mouse focus.

### 5.3 WebGL not supported error

- Verify WebGL is enabled in your browser:
  - Chrome: `chrome://gpu`
  - Firefox: `about:support`

### 5.4 Tested Successfully On

- Mozilla Firefox

### 5.5 Notes for Academic Evaluation

- No external frameworks were used
- All transformations, animations, textures, and interactions are implemented using:
  - `Raw WebGL API`
  - `glMatrix library`

The project fully complies with the Computer Graphics course requirements at UNIWA

---

## 6. Open the Documentation

1. Navigate to the `docs/` directory
2. Open the report corresponding to your preferred language:
   - English: `3D-Graphics-Scene-using-WebGL.pdf`
   - Greek: `3D-Σκηνή-με-WebGL.pdf`
