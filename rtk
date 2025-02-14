<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>วาเลนไทม์</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&display=swap" rel="stylesheet">

    <style>
        body {
            font-family: 'Roboto', sans-serif;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #fce4e1;
            margin: 0;
            color: #333;
            position: relative;
            padding: 20px;
        }

        h1 {
            font-size: 36px;
            color: #ff8da3;
            margin-bottom: 10px;
            text-align: center;
            z-index: 10;
        }

        .form-container {
            text-align: center;
            background-color: #fff;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            width: 90%;
            max-width: 400px;
            margin-bottom: 30px;
        }

        input {
            padding: 12px 20px;
            font-size: 16px;
            border: 1px solid #ff8da3;
            border-radius: 6px;
            width: 100%;
            margin-bottom: 20px;
            box-sizing: border-box;
            transition: border-color 0.3s ease;
        }

        input:focus {
            border-color: #ff4c71;
            outline: none;
        }

        .click-button {
            padding: 12px 24px;
            font-size: 18px;
            background-color: #ff8da3;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 6px;
            width: 100%;
            transition: background-color 0.3s ease;
        }

        .click-button:hover {
            background-color: #ff4c71;
        }

        .cat-container {
            display: none;
            position: relative;
            width: 100%;
            height: 300px;
            margin-top: 50px;
            z-index: 1;
        }

        .cat {
            font-size: 50px;
            position: absolute;
            top: 50%;
            left: 0;
            cursor: pointer;
            z-index: 5;
        }

        .target-area {
            position: absolute;
            bottom: 10px;
            left: 70%;
            font-size: 50px;
            display: none;
            z-index: 5;
        }

        .envelope {
            width: 80%;
            max-width: 500px;
            height: 300px;
            background-color: #fff;
            border-radius: 10px;
            border: 2px solid #ff8da3;
            position: relative;
            display: none;
            overflow: hidden;
            text-align: center;
            padding-top: 100px;
            transition: opacity 1s ease-out;
        }

        .envelope:before {
            content: '';
            position: absolute;
            top: -40px;
            left: 50%;
            transform: translateX(-50%);
            width: 200%;
            height: 40px;
            background-color: #ff8da3;
            border-radius: 50%;
        }

        .envelope .flap {
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            height: 80%;
            background-color: #ff8da3;
            border-radius: 0 0 30px 30px;
            transition: all 1s ease-in-out;
            z-index: 10;
        }

        .envelope.open .flap {
            transform: translateX(-50%) rotateX(180deg);
        }

        .open-envelope-btn {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background-color: #fff;
            color: #ff8da3;
            font-size: 16px;
            font-weight: bold;
            border: 2px solid #ff8da3;
            cursor: pointer;
            z-index: 20;
            transition: all 0.3s ease;
        }

        .open-envelope-btn:hover {
            background-color: #ff8da3;
            color: white;
        }

        .greeting {
            font-size: 32px;
            color: #ff4c71;
            display: none;
            margin-top: 30px;
            z-index: 10;
            position: relative;
            padding: 40px;
            text-align: center;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #fff;
            border-radius: 20px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
            margin-top: 50px;
            width: 90%;
            max-width: 500px;
            opacity: 0;
        }

        .greeting span {
            font-weight: bold;
            font-size: 36px;
            color: #ff4c71;
        }

        .heart-container {
            position: absolute;
            top: 20%;
            left: 50%;
            transform: translateX(-50%);
            z-index: 5;
            width: 100%;
            text-align: center;
        }

        .heart-container i {
            font-size: 30px;
            color: #ff4c71;
            animation: heartAnimation 2s ease-in-out infinite;
            display: inline-block;
            margin: 0 15px;
        }

        .heart-container i:nth-child(even) {
            animation-delay: 0.5s;
        }

        @keyframes heartAnimation {
            0% {
                transform: translateY(0);
                opacity: 1;
            }
            50% {
                transform: translateY(-30px);
                opacity: 0.6;
            }
            100% {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .instruction {
            font-size: 22px;
            color: #ff8da3;
            font-weight: bold;
            text-align: center;
            margin-top: 20px;
        }

    </style>
</head>
<body>

    <div class="form-container">
        <label for="name" style="font-size: 18px; color: #ff8da3;">ใส่ชื่อหน่อยงับบ</label>
        <input type="text" id="name" placeholder="ใส่ตรงนี้เลยย" autocomplete="off" />
        <button class="click-button" onclick="startGame()">เริ่ม</button>
    </div>

    <div class="cat-container" id="catContainer">
        <div class="cat" id="cat">🐱</div>
        <div class="target-area" id="targetArea">🐟</div>
        <p class="instruction">เอาแมวไปใกล้ๆ น้อนปลาหน่อยน้าา</p>
    </div>

    <div class="envelope" id="envelope">
        <div class="flap"></div>
        <button class="open-envelope-btn" onclick="openEnvelope()">กดเปิด</button>
    </div>

    <div class="greeting" id="greeting">
        <p>Happy Valentine นะครับ  <span id="userName"></span></p>
        <div class="heart-container">
            <i>❤️</i>
            <i>❤️</i>
            <i>❤️</i>
            <i>❤️</i>
            <i>❤️</i>
        </div>
        <!-- แมวตัวขนาดปานกลางในหน้าสุดท้าย -->
        <div id="finalCat" class="cat" style="font-size: 80px;">🐱</div>
    </div>

    <script>
        let isDragging = false;
        let offsetX, offsetY;
        let cat = document.getElementById('cat');

        function startGame() {
            var name = document.getElementById('name').value;
            if (name) {
                document.querySelector('.form-container').style.display = 'none';
                document.getElementById('catContainer').style.display = 'block';
                document.getElementById('userName').textContent = name;
                document.getElementById('targetArea').style.display = 'block'; 
                enableDrag();
            } else {
                alert('กรุณากรอกชื่อก่อน');
            }
        }

        function enableDrag() {
            cat.addEventListener('mousedown', (e) => {
                isDragging = true;
                offsetX = e.clientX - cat.offsetLeft;
                offsetY = e.clientY - cat.offsetTop;
            });

            document.addEventListener('mousemove', (e) => {
                if (isDragging) {
                    requestAnimationFrame(() => {
                        cat.style.left = e.clientX - offsetX + 'px';
                        cat.style.top = e.clientY - offsetY + 'px';
                    });
                }
            });

            document.addEventListener('mouseup', () => {
                isDragging = false;
                checkPosition();
            });
        }

        function checkPosition() {
            const cat = document.getElementById('cat');
            const target = document.getElementById('targetArea');

            const catRect = cat.getBoundingClientRect();
            const targetRect = target.getBoundingClientRect();

            if (
                catRect.left < targetRect.left + targetRect.width &&
                catRect.left + catRect.width > targetRect.left &&
                catRect.top < targetRect.top + targetRect.height &&
                catRect.top + catRect.height > targetRect.top
            ) {
                document.getElementById('catContainer').style.display = 'none';
                document.getElementById('envelope').style.display = 'block';
            }
        }

        function openEnvelope() {
            document.getElementById('envelope').classList.add('open');
            setTimeout(function() {
                document.getElementById('greeting').style.display = 'block';
                document.getElementById('greeting').style.opacity = '1';
            }, 1000);

            document.getElementById('envelope').style.opacity = '0';
        }

        // ฟังก์ชันสำหรับแมวขยับแบบสุ่ม
        const finalCat = document.getElementById('finalCat');
        finalCat.addEventListener('click', function() {
            const randomX = Math.random() * (window.innerWidth - finalCat.offsetWidth);
            const randomY = Math.random() * (window.innerHeight - finalCat.offsetHeight);
            finalCat.style.left = randomX + 'px';
            finalCat.style.top = randomY + 'px';
            finalCat.style.position = 'absolute';
        });
    </script>

</body>
</html>
