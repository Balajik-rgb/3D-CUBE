# 3D-CUBE
🧊 3D Cube Using HTML, CSS & JavaScript
Creating a 3D cube using HTML, CSS, and JavaScript is a great way to understand CSS transforms, 3D perspective, and animations.
📌 1️⃣ Project Overview
We will create:
A 3D cube
Rotating animation
Interactive rotation using JavaScript
🛠 2️⃣ Technologies Used
HTML → Structure of cube
CSS → 3D styling & animation
JavaScript → Interaction & control
🏗 3️⃣ Step 1: HTML Structure
Create a file named index.html
Html
Copy code
<!DOCTYPE html>
<html>
<head>
    <title>3D Cube</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="scene">
    <div class="cube" id="cube">
        <div class="face front">Front</div>
        <div class="face back">Back</div>
        <div class="face right">Right</div>
        <div class="face left">Left</div>
        <div class="face top">Top</div>
        <div class="face bottom">Bottom</div>
    </div>
</div>

<button onclick="rotateCube()">Rotate Cube</button>

<script src="script.js"></script>
</body>
</html>
✅ Explanation:
scene → Creates 3D perspective
cube → Main container
face → 6 sides of cube
Button → Rotate cube using JS
🎨 4️⃣ Step 2: CSS Styling (style.css)
Css
Copy code
body {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background: #111;
    color: white;
}

.scene {
    width: 200px;
    height: 200px;
    perspective: 600px;
}

.cube {
    width: 100%;
    height: 100%;
    position: relative;
    transform-style: preserve-3d;
    transform: rotateX(0deg) rotateY(0deg);
    transition: transform 1s;
}

.face {
    position: absolute;
    width: 200px;
    height: 200px;
    background: rgba(0, 150, 255, 0.7);
    border: 2px solid white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;
}

/* Positioning each face */

.front  { transform: rotateY(0deg) translateZ(100px); }
.back   { transform: rotateY(180deg) translateZ(100px); }
.right  { transform: rotateY(90deg) translateZ(100px); }
.left   { transform: rotateY(-90deg) translateZ(100px); }
.top    { transform: rotateX(90deg) translateZ(100px); }
.bottom { transform: rotateX(-90deg) translateZ(100px); }
✅ CSS Explanation
🔹 perspective
Creates depth effect (3D view).
🔹 transform-style: preserve-3d
Allows children elements to maintain 3D position.
🔹 translateZ(100px)
Moves each face outward from center.
Since cube width = 200px, half = 100px.
⚙ 5️⃣ Step 3: JavaScript (script.js)
Javascript
Copy code
let x = 0;
let y = 0;

function rotateCube() {
    x += 90;
    y += 90;
    document.getElementById("cube").style.transform =
        "rotateX(" + x + "deg) rotateY(" + y + "deg)";
}
✅ JavaScript Explanation
x and y track rotation angle
Every click rotates 90°
style.transform dynamically updates cube rotation
🎯 6️⃣ How It Works (Complete Flow)
HTML creates cube structure.
CSS positions 6 faces in 3D space.
JavaScript rotates cube when button is clicked.
perspective makes it look realistic.
🚀 7️⃣ Features
✔ 3D Perspective Effect
✔ Smooth Rotation
✔ Interactive Button
✔ Clean UI
✔ Lightweight Code
💡 8️⃣ Uses of 3D Cube
🎮 Game UI Design
📦 Product Showcase
🎨 Portfolio Websites
📊 3D Data Visualization
🧠 Learning CSS 3D Concepts
🔥 9️⃣ Advanced Improvements (Optional)
You can add:
Auto rotation animation
Mouse drag control
Different colors for each face
Images instead of text
Shadow effects
Example Auto Rotate:
Css
Copy code
.cube {
    animation: spin 5s infinite linear;
}

@keyframes spin {
    from { transform: rotateX(0deg) rotateY(0deg); }
    to { transform: rotateX(360deg) rotateY(360deg); }
}
📌 Final Output Result
You will see:
A blue 3D cube
Clicking button rotates cube
Smooth 3D animation effect
🧊 3D Cube Using HTML, CSS & JavaScript
Creating a 3D cube using HTML, CSS, and JavaScript is a great way to understand CSS transforms, 3D perspective, and animations.
📌 1️⃣ Project Overview
We will create:
A 3D cube
Rotating animation
Interactive rotation using JavaScript
🛠 2️⃣ Technologies Used
HTML → Structure of cube
CSS → 3D styling & animation
JavaScript → Interaction & control
🏗 3️⃣ Step 1: HTML Structure
Create a file named index.html
Html
Copy code
<!DOCTYPE html>
<html>
<head>
    <title>3D Cube</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="scene">
    <div class="cube" id="cube">
        <div class="face front">Front</div>
        <div class="face back">Back</div>
        <div class="face right">Right</div>
        <div class="face left">Left</div>
        <div class="face top">Top</div>
        <div class="face bottom">Bottom</div>
    </div>
</div>

<button onclick="rotateCube()">Rotate Cube</button>

<script src="script.js"></script>
</body>
</html>
✅ Explanation:
scene → Creates 3D perspective
cube → Main container
face → 6 sides of cube
Button → Rotate cube using JS
🎨 4️⃣ Step 2: CSS Styling (style.css)
Css
Copy code
body {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background: #111;
    color: white;
}

.scene {
    width: 200px;
    height: 200px;
    perspective: 600px;
}

.cube {
    width: 100%;
    height: 100%;
    position: relative;
    transform-style: preserve-3d;
    transform: rotateX(0deg) rotateY(0deg);
    transition: transform 1s;
}

.face {
    position: absolute;
    width: 200px;
    height: 200px;
    background: rgba(0, 150, 255, 0.7);
    border: 2px solid white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;
}

/* Positioning each face */

.front  { transform: rotateY(0deg) translateZ(100px); }
.back   { transform: rotateY(180deg) translateZ(100px); }
.right  { transform: rotateY(90deg) translateZ(100px); }
.left   { transform: rotateY(-90deg) translateZ(100px); }
.top    { transform: rotateX(90deg) translateZ(100px); }
.bottom { transform: rotateX(-90deg) translateZ(100px); }
✅ CSS Explanation
🔹 perspective
Creates depth effect (3D view).
🔹 transform-style: preserve-3d
Allows children elements to maintain 3D position.
🔹 translateZ(100px)
Moves each face outward from center.
Since cube width = 200px, half = 100px.
⚙ 5️⃣ Step 3: JavaScript (script.js)
Javascript
Copy code
let x = 0;
let y = 0;

function rotateCube() {
    x += 90;
    y += 90;
    document.getElementById("cube").style.transform =
        "rotateX(" + x + "deg) rotateY(" + y + "deg)";
}
✅ JavaScript Explanation
x and y track rotation angle
Every click rotates 90°
style.transform dynamically updates cube rotation
🎯 6️⃣ How It Works (Complete Flow)
HTML creates cube structure.
CSS positions 6 faces in 3D space.
JavaScript rotates cube when button is clicked.
perspective makes it look realistic.
🚀 7️⃣ Features
✔ 3D Perspective Effect
✔ Smooth Rotation
✔ Interactive Button
✔ Clean UI
✔ Lightweight Code
💡 8️⃣ Uses of 3D Cube
🎮 Game UI Design
📦 Product Showcase
🎨 Portfolio Websites
📊 3D Data Visualization
🧠 Learning CSS 3D Concepts
🔥 9️⃣ Advanced Improvements (Optional)
You can add:
Auto rotation animation
Mouse drag control
Different colors for each face
Images instead of text
Shadow effects
Example Auto Rotate:
Css
Copy code
.cube {
    animation: spin 5s infinite linear;
}

@keyframes spin {
    from { transform: rotateX(0deg) rotateY(0deg); }
    to { transform: rotateX(360deg) rotateY(360deg); }
}
📌 Final Output Result
You will see:
A blue 3D cube
Clicking button rotates cube
Smooth 3D animation effect

https://www.linkedin.com/in/


<img width="1361" height="767" alt="Screenshot 2026-03-02 131558" src="https://github.com/user-attachments/assets/67686a8b-ae83-44bc-b043-8ddfe472c81f" />
<img width="1363" height="767" alt="Screenshot 2026-03-02 131518" src="https://github.com/user-attachments/assets/4bcbead3-03b0-4513-83d4-930e547317e1" />
<img width="1345" height="730" alt="Screenshot 2026-03-02 131625" src="https://github.com/user-attachments/assets/5bcd954a-8700-4f01-9f20-3e94d121bd9a" />

