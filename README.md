<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Jessa! 🌿</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
    <style>
        :root {
            --primary-green: #2d6a4f;
            --soft-green: #d8f3dc;
            --accent-green: #95d5b2;
            --dark-green: #081c15;
        }

        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: var(--soft-green);
            font-family: 'Georgia', serif;
            overflow: hidden;
        }

        .card {
            width: 90%;
            max-width: 400px;
            height: 550px;
            background: white;
            border-radius: 30px;
            box-shadow: 0 15px 35px rgba(45, 106, 79, 0.2);
            position: relative;
            padding: 40px;
            text-align: center;
            border: 4px solid var(--accent-green);
        }

        .page {
            display: none;
            height: 80%;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .active { display: flex; }

        h1 { color: var(--primary-green); font-size: 1.8rem; margin-bottom: 10px; }
        p { color: var(--dark-green); line-height: 1.8; font-size: 1.2rem; font-style: italic; }
        .emoji { font-size: 4.5rem; margin-bottom: 20px; filter: drop-shadow(0 5px 5px rgba(0,0,0,0.1)); }
        .slide-num { font-size: 0.8rem; color: var(--accent-green); margin-top: 10px; font-family: sans-serif; }

        .nav-buttons {
            position: absolute;
            bottom: 40px;
            left: 0;
            right: 0;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        button {
            padding: 12px 25px;
            border: none;
            border-radius: 12px;
            background: var(--primary-green);
            color: white;
            cursor: pointer;
            font-weight: bold;
            font-size: 1rem;
            box-shadow: 0 4px 0 #1b4332;
        }

        button:active { transform: translateY(2px); box-shadow: 0 2px 0 #1b4332; }
        button:disabled { background: #b7e4c7; box-shadow: none; cursor: not-allowed; }

        .from-tag {
            margin-top: 20px;
            font-weight: bold;
            color: var(--primary-green);
            font-size: 1.3rem;
        }
    </style>
</head>
<body>

<div class="card animate__animated animate__zoomIn">
    <div id="page1" class="page active animate__animated">
        <div class="emoji">🌿</div>
        <h1>Hey Jessa!</h1>
        <p>I heard today is a very special day...</p >
        <div class="slide-num">1 / 10</div>
    </div>

    <div id="page2" class="page animate__animated">
        <div class="emoji">🍃</div>
        <p>Since green is your favorite color, I wanted to bring a little nature and luck to your screen.</p >
        <div class="slide-num">2 / 10</div>
    </div>

    <div id="page3" class="page animate__animated">
        <div class="emoji">🕯️</div>
        <p>Another year of being incredible, kind, and uniquely you.</p >
        <div class="slide-num">3 / 10</div>
    </div>

    <div id="page4" class="page animate__animated">
        <div class="emoji">🌱</div>
        <p>Like a growing leaf, I hope this year brings you new beginnings and fresh energy.</p >
        <div class="slide-num">4 / 10</div>
    </div>

    <div id="page5" class="page animate__animated">
        <div class="emoji">✨</div>
        <p>May your path always be clear and your heart always be full of peace.</p >
        <div class="slide-num">5 / 10</div>
    </div>

    <div id="page6" class="page animate__animated">
        <div class="emoji">🍀</div>
        <p>You’re the kind of person who makes the world feel a little bit luckier just by being in it.</p >
        <div class="slide-num">6 / 10</div>
    </div>

    <div id="page7" class="page animate__animated">
        <div class="emoji">🍵</div>
        <p>I hope today is as calm and refreshing as your favorite cup of green tea.</p >
        <div class="slide-num">7 / 10</div>
    </div>

    <div id="page8" class="page animate__animated">
        <div class="emoji">🎁</div>
        <p>You deserve all the beautiful things life has to offer today and every day.</p >
        <div class="slide-num">8 / 10</div>
    </div>

    <div id="page9" class="page animate__animated">
        <div class="emoji">💚</div>
        <h1>Happy Birthday, Jessa!</h1>
        <p>May this year be your brightest and most beautiful one yet.</p >
        <div class="slide-num">9 / 10</div>
    </div>

    <div id="page10" class="page animate__animated">
        <div class="emoji">🌳</div>
        <h1>With Love,</h1>
        <div class="from-tag">— Dero</div>
        <p style="margin-top: 20px; font-size: 0.9rem;">(Click 'Back' to read again!)</p >
        <div class="slide-num">10 / 10</div>
    </div>

    <div class="nav-buttons">
        <button id="backBtn" onclick="changePage(-1)" disabled>Back</button>
        <button id="nextBtn" onclick="changePage(1)">Next</button>
    </div>
</div>

<script>
    let currentPage = 1;
    const totalPages = 10;

    function changePage(direction) {
        const currentEl = document.getElementById(`page${currentPage}`);
        currentEl.classList.remove('animate__fadeInRight', 'animate__fadeInLeft', 'active');
        
        currentPage += direction;
        const nextEl = document.getElementById(`page${currentPage}`);
        nextEl.classList.add('active');
        
        if (direction > 0) {
            nextEl.classList.add('animate__fadeInRight');
        } else {
            nextEl.classList.add('animate__fadeInLeft');
        }

        document.getElementById('backBtn').disabled = (currentPage === 1);
        document.getElementById('nextBtn').style.display = (currentPage === totalPages) ? 'none' : 'inline-block';
    }
</script>

</body>
</html>

