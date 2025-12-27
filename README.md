# Ex.07 Design of Interactive Image Gallery
## Date:27-12-2025

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM:
```
image.html
<head>
    <title>Interactive Image Gallery</title>
    <link href="img.css" rel="stylesheet">
</head>
<body>
    <header class="header">
        <h1>Image Gallery</h1>
    </header>

    <div class="container">
        <div class="card">
            <img id="galleryImage" src="aot.jpeg"alt="Gallery Image">
            <p class="caption" id="caption">Attack On Titan</p>

            <div class="buttons">
                <button onclick="prevImage()">Previous</button>
                <button onclick="nextImage()">Next</button>
            </div>
        </div>
    </div>

    <footer class="footer">
        MANIGANDAN.S(25004934)
    </footer>

    <script>
        let gallery = [
            { src: "aot.jpeg", text: "Attack On Titan" },
            { src: "bleach.jpeg", text: "Bleach" },
            { src: "demonslayer.jpeg", text: "Demon Slayer" },
            { src: "solo.jpeg", text: "Solo Levelling" },
            { src: "wano.jpg", text: "One Piece" }
        ];
        let index = 0;
        function nextImage() {
            index++;
            if (index >= gallery.length) {
                index = 0;
            }
            updateImage();
        }
        function prevImage() {
            index--;
            if (index < 0) {
                index = gallery.length - 1;
            }
            updateImage();
        }
        function updateImage() {
            document.getElementById("galleryImage").src = gallery[index].src;
            document.getElementById("caption").innerText = gallery[index].text;
        }
    </script>
</body>
</html>

img.css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background-image:url(BG.jpeg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position:center;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

.header {
    background-color: rgba(1, 18, 19, 0.679);
    color: white;
    text-align: center;
    padding: 15px;
}

.container {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
}

.card {
    background:linear-gradient(45deg,gray,cyan,gray);
    padding: 15px;
    border-radius: 12px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    text-align: center;
    width: 500px;
}

.card img {
    width: 420px;
    height: 220px;
    object-fit: cover;
    border-radius: 10px;
    margin-bottom: 10px;
}

.caption {
    margin: 15px 0;
    font-size: 16px;
    font-weight: bold;
    color: antiquewhite;
}

.buttons {
    display: flex;
    justify-content: center;
    gap: 15px;
}

.buttons button {
    background-color: rgb(174, 173, 173);
    color: rgba(255, 255, 255, 0.773);
    border: none;
    padding: 10px 18px;
    border-radius: 8px;
    cursor: pointer;
}

.buttons button:hover {
    background-color: rgba(128, 39, 39, 0.875);
}

.footer {
    background-color: rgba(5, 4, 4, 0.693);
    color: white;
    text-align: center;
    padding: 12px;
}

```
## OUTPUT:
![alt text](<Screenshot (79)-1.png>)
![alt text](<Screenshot (80).png>)
![alt text](<Screenshot (81).png>)
![alt text](<Screenshot (82).png>)
![alt text](<Screenshot (83).png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
