<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mo.Na Love Page</title>
    <style>
        body {
            background-color: #ffebf0;
            font-family: 'Arial', sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            overflow: hidden;
        }

        h1 {
            font-size: 60px;
            color: #d63384;
            font-weight: bold;
            margin-top: 20px;
            animation: fadeIn 2s ease-in-out;
        }

        .container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin: auto;
            padding: 20px;
            background: white;
            box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.2);
            border-radius: 15px;
            margin-top: 30px;
            animation: slideIn 1.5s ease-in-out;
        }

        img {
            width: 100%;
            border-radius: 15px;
        }

        .dates {
            font-size: 20px;
            color: #d63384;
            margin-top: 15px;
            font-weight: bold;
            opacity: 0;
            animation: fadeIn 2s ease-in-out forwards;
        }

        .dates:nth-child(1) { animation-delay: 1s; }
        .dates:nth-child(2) { animation-delay: 2s; }
        .dates:nth-child(3) { animation-delay: 3s; }
#naa {
color: rgb(21, 255, 0);
}
        .input-box {
            margin-top: 20px;
        }

        textarea {
            width: 80%;
            height: 100px;
            border-radius: 10px;
            border: 2px solid #d63384;
            padding: 10px;
            font-size: 18px;
            resize: none;
        }

        .hearts, .flowers {
            position: absolute;
            width: 30px;
            height: 30px;
            animation: floatUp 4s infinite;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes slideIn {
            from { transform: translateY(-50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        @keyframes floatUp {
            from { transform: translateY(0); opacity: 1; }
            to { transform: translateY(-100px); opacity: 0; }
        }
    </style>
</head>
<body>

    <h1>Mo.Na</h1>

    <div class="container">
        <img src="https://source.unsplash.com/600x400/?couple,hug" alt="Loving Couple">
        <div class="dates">2004/8/2</div>
        <div class="dates">2005/12/24</div>
        <div class="dates">2024/11/13</div>

        <div class="input-box">
            <textarea placeholder="اكتب شيئًا خاصًا هنا..." id="naa">Я люблю тебя💞😍</textarea>
        </div>
    </div>

    <script>
        function createFloatingElement(type) {
            const element = document.createElement("div");
            element.classList.add(type);
            element.innerHTML = type === "hearts" ? "❤" : "🌸";
            document.body.appendChild(element);

            let startX = Math.random() * window.innerWidth;
            let startY = window.innerHeight;
            let duration = Math.random() * 3 + 2;

            element.style.left = startX + "px";
            element.style.top = startY + "px";
            element.style.animationDuration = duration + "s";

            setTimeout(() => {
                element.remove();
            }, duration * 1000);
        }

        setInterval(() => createFloatingElement("hearts"), 800);
        setInterval(() => createFloatingElement("flowers"), 1200);
    </script>

</body>
</html>
