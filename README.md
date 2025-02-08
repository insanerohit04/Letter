<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Love Letter</title>
    <style>
        /* Background & Font */
        body {
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            font-family: 'Georgia', serif;
            text-align: center;
            color: white;
            padding: 50px;
            margin: 0;
        }

        /* Letter Box */
        .letter {
            background: rgba(0, 0, 0, 0.5);
            padding: 30px;
            max-width: 600px;
            margin: auto;
            border-radius: 15px;
            box-shadow: 0 0 15px rgba(255, 255, 255, 0.3);
        }

        /* Title */
        h1 {
            font-size: 30px;
            color: #ffccd5;
        }

        /* Paragraphs */
        p {
            font-size: 18px;
            line-height: 1.6;
        }

        /* Signature */
        .signature {
            margin-top: 20px;
            font-style: italic;
            font-size: 20px;
            color: #ff99aa;
        }

        /* Floating Hearts */
        .heart {
            position: fixed; /* Keeps hearts within viewport */
            top: 100vh; /* Starts below the screen */
            color: #ff4d6d;
            font-size: 24px;
            animation: float 5s infinite ease-in-out;
            opacity: 0.7;
        }

        @keyframes float {
            0% { transform: translateY(0); opacity: 0.9; }
            50% { opacity: 0.5; }
            100% { transform: translateY(-110vh); opacity: 0; }
        }
    </style>
</head>
<body>
    <!-- Floating Hearts -->
    <script>
        function createHeart() {
            const heart = document.createElement("div");
            heart.innerHTML = "❤️";
            heart.classList.add("heart");
            document.body.appendChild(heart);
            
            let size = Math.random() * 20 + 10; 
            heart.style.fontSize = size + "px";
            heart.style.left = Math.random() * window.innerWidth + "px";
            heart.style.animationDuration = Math.random() * 3 + 2 + "s";
            
            setTimeout(() => { heart.remove(); }, 5000);
        }

        setInterval(createHeart, 300);
    </script>

    <!-- Love Letter -->
    <div class="letter">
        <h1>To the One Who Holds My Heart,</h1>
        <p>From the first moment I met you, something inside me changed. Your presence feels like home, your smile like a warm sunrise. I never knew that one person could mean so much until you came into my life.</p>
        <p>Today, on this special day, I want to tell you something straight from my heart—I love you. Not just in words, but in every little moment, every thought, and every dream I have. You are the reason my world feels brighter, my days feel special, and my heart beats a little faster.</p>
        <p>I don’t know what the future holds, but I know one thing for sure—I want you to be a part of it. I want to laugh with you, stand by you, and share this beautiful journey of life together.</p>
        <p><strong>So, with all my heart, I ask—Will you be mine?</strong></p>
        <p class="signature">Forever yours,<br> Rohit</p>
    </div>
</body>
</html>
