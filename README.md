<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Me perdonas, mi niña?</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #ffcce7; /* Fondo rosa suave */
            text-align: center;
            overflow: hidden;
        }
        .container {
            width: 80%;
            position: relative;
        }
        h1 {
            font-size: 2em;
            color: #333;
        }
        .button-container {
            margin-top: 20px;
        }
        .button {
            padding: 10px 20px;
            font-size: 1.2em;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            transition: all 0.3s;
        }
        #yesButton {
            background-color: #ff69b4;
            color: white;
            display: none;
        }
        #noButton {
            background-color: #ff1493;
            color: white;
        }
        #message {
            display: none;
            font-size: 1.5em;
            color: #333;
            margin-top: 20px;
        }
        /* Stickers */
        .sticker {
            position: absolute;
            width: 50px;
            height: 50px;
            opacity: 0.7;
        }
        .sticker-heart {
            top: 10%;
            left: 20%;
        }
        .sticker-star {
            top: 80%;
            right: 15%;
        }
        .sticker-flower {
            top: 50%;
            left: 70%;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>¿Me perdonas, mi niña?</h1>
        <div class="button-container">
            <button id="yesButton" class="button" onclick="showMessage()">Sí</button>
            <button id="noButton" class="button" onclick="makeYesBigger()">No</button>
        </div>
        <p id="message">Gracias, mi niña. Te quiero ❤️</p>

        <!-- Stickers decorativos -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Emoji_u2764.svg/1024px-Emoji_u2764.svg.png" alt="corazón" class="sticker sticker-heart">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/34/Emoji_u2b50.svg/1024px-Emoji_u2b50.svg.png" alt="estrella" class="sticker sticker-star">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/Emoji_u1f33a.svg/1024px-Emoji_u1f33a.svg.png" alt="flor" class="sticker sticker-flower">
    </div>

    <script>
        let yesButton = document.getElementById("yesButton");
        let noButton = document.getElementById("noButton");

        function makeYesBigger() {
            yesButton.style.display = "inline-block";
            yesButton.style.transform = "scale(1.1)";
            yesButton.style.fontSize = parseFloat(getComputedStyle(yesButton).fontSize) * 1.1 + "px";
            noButton.style.transform = "scale(0.9)";
            if (parseFloat(getComputedStyle(yesButton).fontSize) > 40) {
                noButton.style.display = "none";
                yesButton.style.width = "100%";
            }
        }

        function showMessage() {
            document.getElementById("message").style.display = "block";
            document.querySelector(".button-container").style.display = "none";
        }
    </script>

</body>
</html>
