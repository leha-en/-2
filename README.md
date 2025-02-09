<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f0f0f0;
        }

        .owl-container {
            width: 300px;
            height: 400px;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: white;
            box-shadow: 0 0 15px rgba(128, 0, 255, 0.7); /* Объемная фиолетовая рамка */
        }

        img {
            max-width: 80%;
            max-height: 80%;
        }
    </style>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мой сайт</title>
    <style>
        .line {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 200px;
            height: 5px;
            background-color: blue;
            transition: all 0.1s ease-in-out;
        }
    </style>
</head>
<body>
    <div class="owl-container">
        <h1><img alt="надип"></h1>
    </div>
<!-- Ваш контент -->

    <script>
        document.addEventListener('mousemove', function(event) {
            const line = document.querySelector('.line');
            if (!line) return;

            let angle = Math.atan2(event.clientY - window.innerHeight / 2, event.clientX - window.innerWidth / 2);
            angle = angle * 180 / Math.PI + 180;

            line.style.transform = `translate(-50%, -50%) rotate(${angle}deg)`;
        });

        window.onload = function() {
            const line = document.createElement('div');
            line.className = 'line';
            document.body.appendChild(line);
        };
    </script>


    
</body>
</html>
