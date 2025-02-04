# san-valentin
San Valentín, amor, romance, kuromi, cute, pareja 
index.html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Quieres ser mi San Valentín?</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f8e6e0;
            margin: 0;
            overflow: hidden;
        }
        
        .container {
            text-align: center;
        }
        
        .kuromi {
            width: 150px;
            animation: float 3s infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }
        
        .btn {
            display: inline-block;
            margin: 20px;
            padding: 15px 30px;
            font-size: 20px;
            color: #fff;
            background-color: #ff69b4;
            border: none;
            cursor: pointer;
            border-radius: 10px;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #ff1493;
        }
        
        #no {
            position: absolute;
        }
        
        @keyframes celebrate {
            0% { transform: scale(1); }
            50% { transform: scale(1.5); }
            100% { transform: scale(1); }
        }
        
        .celebrate {
            display: none;
            font-size: 24px;
            color: #ff69b4;
            animation: celebrate 1s infinite;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>¿Quieres ser mi San Valentín, Zaid?</h1>
        <img src="https://i.imgur.com/Eo3rB5w.png" alt="Kuromi" class="kuromi">
        <div>
            <button class="btn" id="yes">Sí</button>
            <button class="btn" id="no">No</button>
        </div>
        <div class="celebrate" id="celebrate">
            <p>Sii! te amo mi amor, afortunada de tenerte</p>
        </div>
    </div>

    <script>
        document.getElementById('yes').addEventListener('click', function() {
            document.getElementById('celebrate').style.display = 'block';
        });

        document.getElementById('no').addEventListener('mouseover', function(event) {
            const button = event.target;
            const x = Math.random() * (window.innerWidth - button.clientWidth);
            const y = Math.random() * (window.innerHeight - button.clientHeight);
            button.style.left = `${x}px`;
            button.style.top = `${y}px`;
        });
    </script>
</body>
</html>
