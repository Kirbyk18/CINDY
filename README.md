<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para CINDY 💛</title>
    <style>
        body {
            background-color: #0d1117;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            margin: 0;
            overflow: hidden;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        .message-container {
            position: absolute;
            top: 10%;
            text-align: center;
            z-index: 20;
            animation: fadeInText 3s ease-in-out forwards;
            opacity: 0;
            padding: 0 20px;
        }

        .message-container h1 {
            color: #ffeb3b;
            font-size: 3rem;
            margin: 0;
            text-shadow: 0 0 15px rgba(255, 235, 59, 0.6);
        }

        .message-container p {
            color: #fff;
            font-size: 1.5rem;
            margin-top: 10px;
            font-style: italic;
        }

        .bouquet {
            position: relative;
            width: 100vw;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: flex-end;
        }

        .flower-wrapper {
            position: absolute;
            bottom: -20px;
            transform-origin: bottom center;
            animation: sway 4s ease-in-out infinite alternate;
        }

        .stem {
            width: 7px;
            background: linear-gradient(to top, #1b5e20, #4caf50);
            border-radius: 4px;
            position: relative;
            transform-origin: bottom center;
            animation: growStem 2.5s ease-out forwards;
            transform: scaleY(0);
        }

        .leaf {
            position: absolute;
            width: 30px;
            height: 15px;
            background: #4caf50;
            border-radius: 0 15px 0 15px;
            top: 40%;
            left: 100%;
            transform-origin: left bottom;
            transform: rotate(20deg) scale(0);
            animation: growLeaf 1s ease-out forwards;
        }

        .leaf.left {
            left: auto;
            right: 100%;
            border-radius: 15px 0 15px 0;
            transform-origin: right bottom;
            transform: rotate(-20deg) scale(0);
            top: 60%;
        }

        .flower-head {
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%) scale(0);
            animation: bloom 1.5s ease-out forwards;
            z-index: 5;
        }

        .flower-center {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 2;
            border-radius: 50%;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.5);
        }

        /* Girasol clásico */
        .sunflower .flower-center {
            width: 40px;
            height: 40px;
            background: radial-gradient(circle, #3e2723, #5d4037);
        }
        .sunflower .petal {
            position: absolute;
            width: 15px;
            height: 50px;
            background: linear-gradient(to bottom, #fff176, #fbc02d);
            border-radius: 50% 50% 20% 20%;
            bottom: 50%;
            left: 50%;
            margin-left: -7.5px;
            transform-origin: bottom center;
            box-shadow: 0 0 5px rgba(255, 235, 59, 0.4);
        }

        /* Margarita amarilla */
        .daisy .flower-center {
            width: 30px;
            height: 30px;
            background: radial-gradient(circle, #fbc02d, #f57f17);
        }
        .daisy .petal {
            position: absolute;
            width: 10px;
            height: 45px;
            background: linear-gradient(to bottom, #fff59d, #ffee58);
            border-radius: 50px;
            bottom: 50%;
            left: 50%;
            margin-left: -5px;
            transform-origin: bottom center;
            box-shadow: 0 0 3px rgba(255, 255, 255, 0.3);
        }

        /* Corazones amarillos flotantes */
        .yellow-heart {
            position: absolute;
            width: 15px;
            height: 15px;
            background-color: #ffeb3b;
            transform: rotate(-45deg);
            opacity: 0;
            animation: floatHeart 7s linear infinite;
            z-index: 10;
        }
        .yellow-heart::before,
        .yellow-heart::after {
            content: '';
            position: absolute;
            width: 15px;
            height: 15px;
            background-color: #ffeb3b;
            border-radius: 50%;
        }
        .yellow-heart::before {
            top: -7.5px;
            left: 0;
        }
        .yellow-heart::after {
            top: 0;
            left: 7.5px;
        }

        /* Brillos de fondo */
        .sparkle {
            position: absolute;
            background-color: #fff;
            border-radius: 50%;
            opacity: 0;
            animation: floatingSparkle 4s linear infinite;
        }

        /* Animaciones */
        @keyframes sway {
            0% { transform: rotate(calc(var(--angle) - 3deg)); }
            100% { transform: rotate(calc(var(--angle) + 3deg)); }
        }

        @keyframes growStem {
            0% { transform: scaleY(0); }
            100% { transform: scaleY(1); }
        }

        @keyframes growLeaf {
            0% { transform: rotate(var(--rot)) scale(0); }
            100% { transform: rotate(var(--rot)) scale(1); }
        }

        @keyframes bloom {
            0% { transform: translateX(-50%) scale(0); }
            80% { transform: translateX(-50%) scale(1.1); }
            100% { transform: translateX(-50%) scale(1); }
        }

        @keyframes fadeInText {
            0% { opacity: 0; transform: translateY(-20px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        @keyframes floatingSparkle {
            0% { transform: translateY(0) scale(0); opacity: 0; }
            50% { opacity: 1; transform: translateY(-50px) scale(1); }
            100% { transform: translateY(-100px) scale(0); opacity: 0; }
        }

        @keyframes floatHeart {
            0% { transform: translate(0, 0) rotate(-45deg); opacity: 0; }
            20% { opacity: 0.8; }
            80% { opacity: 0.8; }
            100% { transform: translate(var(--moveX), -100vh) rotate(-45deg); opacity: 0; }
        }
    </style>
</head>
<body>

    <div class="message-container">
        <h1>Para CINDY 💛</h1>
        <p>Con mucho cariño de KIrby</p>
    </div>

    <div class="bouquet" id="bouquet"></div>

    <script>
        const bouquet = document.getElementById('bouquet');
        
        // MÁS flores (25 en total) para llenar el espacio
        const numFlowers = 25; 

        for (let i = 0; i < numFlowers; i++) {
            const flowerWrapper = document.createElement('div');
            
            // Decidir si es Girasol o Margarita (50% de probabilidad)
            const isDaisy = Math.random() > 0.5;
            flowerWrapper.className = `flower-wrapper ${isDaisy ? 'daisy' : 'sunflower'}`;

            // CRECIMIENTO DIAGONAL: Esparcimos las flores por todo el ancho de la pantalla
            const leftPosition = 5 + (Math.random() * 90); // Entre 5% y 95% de la pantalla
            flowerWrapper.style.left = `${leftPosition}vw`;

            // Ángulo diagonal para que crezcan apuntando hacia afuera y arriba
            // Si están a la izquierda, se inclinan a la izquierda. Si están a la derecha, a la derecha.
            let angle = (leftPosition - 50) * 0.8; // Ángulo basado en su posición
            angle += (Math.random() * 10 - 5); // Un poco de aleatoriedad
            
            flowerWrapper.style.setProperty('--angle', `${angle}deg`);
            flowerWrapper.style.transform = `rotate(${angle}deg)`;
            
            const height = 150 + Math.random() * 250; // Diferentes alturas
            const delay = Math.random() * 2.5; // Tiempos de crecimiento distintos
            flowerWrapper.style.animationDelay = `${delay}s`;

            // Tallo (Stem)
            const stem = document.createElement('div');
            stem.className = 'stem';
            stem.style.height = `${height}px`;
            stem.style.animationDelay = `${delay}s`;

            // Hojas (Leaves)
            const leafRight = document.createElement('div');
            leafRight.className = 'leaf';
            leafRight.style.setProperty('--rot', '20deg');
            leafRight.style.animationDelay = `${delay + 1}s`;

            const leafLeft = document.createElement('div');
            leafLeft.className = 'leaf left';
            leafLeft.style.setProperty('--rot', '-20deg');
            leafLeft.style.animationDelay = `${delay + 1.2}s`;

            stem.appendChild(leafRight);
            stem.appendChild(leafLeft);

            // Cabeza de la flor (Flower Head)
            const head = document.createElement('div');
            head.className = 'flower-head';
            head.style.animationDelay = `${delay + 1.5}s`;

            // Centro de la flor
            const center = document.createElement('div');
            center.className = 'flower-center';
            head.appendChild(center);

            // Pétalos (Dependiendo del tipo de flor)
            const numPetals = isDaisy ? 24 : 16;
            for (let p = 0; p < numPetals; p++) {
                const petal = document.createElement('div');
                petal.className = 'petal';
                const petalRotation = p * (360 / numPetals);
                // Distancia del centro basada en si es girasol o margarita
                const translateY = isDaisy ? '-20px' : '-25px';
                petal.style.transform = `rotate(${petalRotation}deg) translateY(${translateY})`;
                head.appendChild(petal);
            }

            stem.appendChild(head);
            flowerWrapper.appendChild(stem);
            bouquet.appendChild(flowerWrapper);
        }

        // Crear pocos corazones amarillos flotando en diagonal
        for (let i = 0; i < 7; i++) {
            const heart = document.createElement('div');
            heart.className = 'yellow-heart';
            heart.style.left = `${Math.random() * 100}vw`;
            heart.style.bottom = `-20px`;
            
            // Movimiento diagonal aleatorio
            const moveX = (Math.random() - 0.5) * 50; 
            heart.style.setProperty('--moveX', `${moveX}vw`);
            
            heart.style.animationDelay = `${Math.random() * 5}s`;
            heart.style.animationDuration = `${6 + Math.random() * 4}s`; // Suben despacio
            
            document.body.appendChild(heart);
        }

        // Crear brillos de fondo
        for (let i = 0; i < 40; i++) {
            const sparkle = document.createElement('div');
            sparkle.className = 'sparkle';
            const size = Math.random() * 4 + 1;
            sparkle.style.width = `${size}px`;
            sparkle.style.height = `${size}px`;
            sparkle.style.left = `${Math.random() * 100}vw`;
            sparkle.style.top = `${Math.random() * 100}vh`;
            sparkle.style.animationDelay = `${Math.random() * 5}s`;
            sparkle.style.animationDuration = `${Math.random() * 3 + 2}s`;
            document.body.appendChild(sparkle);
        }
    </script>
</body>
</html>
