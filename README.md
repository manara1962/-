<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مكتبة المنارة</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f0f0;
            color: #333;
            text-align: center;
            margin: 0;
            padding: 0;
            overflow: hidden; /* لتجنب تمرير الصفحة */
        }

        .container {
            max-width: 600px;
            margin: 50px auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            color: #d35400;
        }

        .social-links a {
            display: inline-block;
            margin: 10px;
            padding: 10px;
            text-decoration: none;
            font-size: 20px;
            border-radius: 5px;
            transition: all 0.3s;
        }

        .facebook { background: #1877f2; color: white; }
        .whatsapp { background: #25d366; color: white; }

        .social-links a:hover {
            transform: scale(1.1);
            opacity: 0.8;
        }

        .mouse-dot {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: red;
            border-radius: 50%;
            pointer-events: none;
            transition: transform 0.1s ease;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>مرحبًا بكم في مكتبة المنارة 📚</h1>
        <p>نوفر لكم جميع خدمات المكتبة والسكريتيريا.</p>

        <h2>تابعونا على:</h2>
        <div class="social-links">
            <a href="https://www.facebook.com/profile.php?id=100076510369066" class="facebook">فيسبوك</a>
            <a href="https://wa.me/213672067786" class="whatsapp">واتساب</a>
        </div>

        <h2>تواصل معنا:</h2>
        <p>📧 البريد الإلكتروني: <a href="mailto:manara1962@gmail.com">manara1962@gmail.com</a></p>
    </div>

    <script>
        // تغيير لون الخلفية عند الضغط (للأجهزة الذكية)
        document.addEventListener("click", (event) => {
            if (!event.target.closest('.container')) {
                document.body.style.backgroundColor = getRandomColor();
            }
        });

        // إنشاء نقطة تتبع لحركة الماوس (للأجهزة المكتبية)
        const mouseDot = document.createElement("div");
        mouseDot.classList.add("mouse-dot");
        document.body.appendChild(mouseDot);

        document.addEventListener("mousemove", (event) => {
            mouseDot.style.left = `${event.pageX}px`;
            mouseDot.style.top = `${event.pageY}px`;
        });

        // دالة للحصول على لون عشوائي
        function getRandomColor() {
            const letters = "0123456789ABCDEF";
            let color = "#";
            for (let i = 0; i < 6; i++) {
                color += letters[Math.floor(Math.random() * 16)];
            }
            return color;
        }
    </script>

</body>
</html>
