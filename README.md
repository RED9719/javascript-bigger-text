# javascript-bigger-text
            <!DOCTYPE html>
<html>
<head>
    <title>Font Size Animation</title>
    <style>
        #text {
            color: red;
            font-size: 5pt;
        }
    </style>
</head>
<body>
    <div id="text">Bigger Text</div>

    <script>
        let fontSize = 5;
        const textElement = document.getElementById("text");
        let increasing = true;

        function changeFontSize() {
            if (increasing) {
                fontSize++;
                if (fontSize >= 50) {
                    increasing = false;
                    textElement.innerText = "Smaller Text";
                    textElement.style.color = "green";
                }
            } else {
                fontSize--;
                if (fontSize <= 5) {
                    clearInterval(interval);
                }
            }
            textElement.style.fontSize = fontSize + "pt";
        }

        const interval = setInterval(changeFontSize, 10);
    </script>
</body>
</html>
