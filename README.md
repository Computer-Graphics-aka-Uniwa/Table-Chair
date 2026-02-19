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

# README

## Building a 3D Graphics Scene Using WebGL

This project demonstrates the incremental development of a **3D graphics environment using WebGL**. It was developed as a semester project for the **Computer Graphics** course at the **University of West Attica (UNIWA)**.  
The implementation progresses through multiple stages, starting from basic geometric primitives and evolving into an interactive, animated, and textured 3D scene.

---

## Table of Contents

| Section | Folder / File                            | Description                           |
| ------: | ---------------------------------------- | ------------------------------------- |
|       1 | `assign/`                                | Project assignment material           |
|     1.1 | `assign/project_2023-2024.pdf`           | Assignment description in English     |
|     1.2 | `assign/εργασία_2023-2024.pdf`           | Assignment description in Greek       |
|       2 | `docs/`                                  | Project documentation                 |
|     2.1 | `docs/3D-Graphics-Scene-using-WebGL.pdf` | Documentation in English              |
|     2.2 | `docs/3D-Σκηνή-με-WebGL.pdf`             | Documentation in Greek                |
|       3 | `src/`                                   | WebGL source code and assets          |
|     3.1 | `src/textures/`                          | Texture images used in the 3D scenes  |
|   3.1.1 | `Chair_Texture.jpg`                      | Chair texture                         |
|   3.1.2 | `Floor_Texture.jpg`                      | Floor texture                         |
|   3.1.3 | `Skybox_Texture.jpg`                     | Skybox texture                        |
|   3.1.4 | `Table_Texture.jpg`                      | Table texture                         |
|     3.2 | `src/WebGL-Libraries/`                   | External WebGL helper libraries       |
|   3.2.1 | `gl-matrix-min.js`                       | Matrix and vector mathematics library |
|   3.2.2 | `webgl-debug.js`                         | WebGL debugging utilities             |
|     3.3 | `src/1st_scene.html`                     | First WebGL 3D scene                  |
|     3.4 | `src/2nd_scene.html`                     | Second WebGL 3D scene                 |
|     3.5 | `src/3rd_scene.html`                     | Third WebGL 3D scene                  |
|     3.6 | `src/4th_scene.html`                     | Fourth WebGL 3D scene                 |
|       4 | `README.md`                              | Project documentation                 |
|       5 | `INSTALL.md`                             | Usage instructions                    |

---

## 1. Scene 1: Foundations

- **Cube Formation:**  
  Implementation of a 3D cube using vertex buffers and color buffers.

- **Camera Control:**  
  Integration of `lookAt()` and `perspective()` functions to define the camera position and viewing frustum.

- **User Interface:**  
  Text input fields allow manual entry of viewing angles and orthogonal distances, accompanied by a **Redraw** button that updates the rendered scene in real time.

---

## 2. Scene 2: Geometric Transformations

- **Object Modeling:**  
  Transformation of the initial cube into more complex composite objects, including:
  - Table
  - Stool
  - Chair

- **Matrix Operations:**  
  Extensive use of transformation matrices such as:
  - `fromTranslation()`
  - `fromScaling()`
  - `multiply()`

  These operations enable precise assembly of multi-part objects from simple geometric components.

---

## 3. Scene 3: Animation and Realism

- **Dynamic Motion:**  
  Start and pause controls allow users to activate or stop camera rotation. Rotation is implemented using trigonometric functions (`Math.cos()` and `Math.sin()`).

- **Texture Mapping:**  
  Basic vertex colors are replaced with realistic textures (512×512 JPEG format), significantly improving visual realism.

---

## 4. Scene 4: Environment and Interaction

- **World Building:**  
  A **Skybox** is implemented as the background environment, along with a 2D floor that displays the developers’ names.

- **Mouse Interaction:**
  - Mouse movement controls the animation speed.
  - Mouse wheel input allows the user to tip the chair forward.

- **Easter Egg:**  
  A hidden feature spawns a second chair after the main chair has been tipped over **three times**, adding an element of interactivity and discovery.

---

## 5. Challenges and Solutions

- **Buffer Alignment:**  
  Considerable testing was required to ensure that individual object components (e.g., table legs, chair back) aligned correctly without visible gaps.

- **Texture Loading Issues:**  
  Problems where objects rendered as black were resolved by:
  - Ensuring texture images had **power-of-two dimensions**
  - Correctly configuring texture buffers and parameters in WebGL

- **Interaction Physics:**  
  Mouse wheel logic was refined to restrict chair rotation between **0° and 90°**, preventing the model from clipping through the floor.

---

## 6. Conclusion

This project showcases a step-by-step approach to building a fully interactive 3D WebGL scene. Through progressive development, it combines geometric modeling, transformations, animation, texture mapping, and user interaction, providing a solid practical foundation in modern computer graphics programming.
