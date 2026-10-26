
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Bestie 🎂</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', sans-serif;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    overflow: hidden;
    background: linear-gradient(135deg, #ff758c, #ff7eb3, #a18cd1);
    color: white;
}

.card {
    width: 90%;
    max-width: 430px;
    padding: 35px 22px;
    border-radius: 25px;
    background: rgba(255,255,255,0.18);
    border: 2px solid rgba(255,255,255,0.5);
    box-shadow: 0 10px 40px rgba(0,0,0,0.2);
    backdrop-filter: blur(10px);
    animation: appear 1.2s ease;
    z-index: 2;
}

h1 {
    font-size: 2.4rem;
    margin-bottom: 15px;
    animation: glow 2s infinite alternate;
}

.cake {
    font-size: 75px;
    margin: 15px;
    animation: bounce 1.5s infinite;
}

p {
    font-size: 17px;
    line-height: 1.8;
    margin: 15px 0;
}

button {
    padding: 13px 25px;
    border: none;
    border-radius: 30px;
    background: #fff;
    color: #e84393;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
    margin-top: 15px;
}

button:hover {
    transform: scale(1.08);
}

#surprise {
    display: none;
    font-size: 18px;
    margin-top: 20px;
    line-height: 1.8;
}

.floating {
    position: absolute;
    bottom: -60px;
    font-size: 30px;
    animation: floatUp 8s linear infinite;
    z-index: 1;
}

@keyframes floatUp {
    from { transform: translateY(0) rotate(0); opacity: 1; }
    to { transform: translateY(-120vh) rotate(360deg); opacity: 0; }
}

@keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-12px); }
}

@keyframes glow {
    from { text-shadow: 0 0 5px #fff; }
    to { text-shadow: 0 0 20px #fff, 0 0 30px #ffdfef; }
}

@keyframes appear {
    from { opacity: 0; transform: scale(0.7); }
    to { opacity: 1; transform: scale(1); }
}
</style>
</head>

<body>

<div class="card">
    <div class="cake">🎂</div>

    <h1>Happy Birthday! 🎉</h1>

    <p>
        To my amazing Bestie 💖<br>
        You are not just my friend,<br>
        you are a beautiful part of my life! 🫶
    </p>

    <p>
        May your life be filled with love,
        laughter, success and endless happiness! ✨
    </p>

    <h2>Stay Happy Forever! 💕</h2>

    <button onclick="showSurprise()">
        🎁 Open Your Surprise
    </button>

    <div id="surprise">
        💝 Dear Bestie,<br>
        Thank you for being a wonderful friend.
        May all your dreams come true!
        Keep smiling and shining forever. 🌟<br>
        Love you, Bestie! 🥰🎂
    </div>
</div>

<script>
function showSurprise() {
    document.getElementById("surprise").style.display = "block";

    for (let i = 0; i < 35; i++) {
        let item = document.createElement("div");
        item.className = "floating";
        item.innerHTML = ["🎈", "💖", "🎉", "✨", "💕"][
            Math.floor(Math.random() * 5)
        ];
        item.style.left = Math.random() * 100 + "vw";
        item.style.animationDuration = (4 + Math.random() * 5) + "s";
        document.body.appendChild(item);

        setTimeout(() => item.remove(), 9000);
    }
}
</script>

</body>
</html>

