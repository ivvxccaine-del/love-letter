<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Love Letter 💌</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400&display=swap');

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  background: linear-gradient(135deg, #ffb6c1, #ffe4ec);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Poppins', sans-serif;
  overflow-x: hidden;
}

/* ---------- ENVELOPE ---------- */
#envelope-container {
  cursor: pointer;
  animation: float 3s ease-in-out infinite;
}

.envelope {
  width: 260px;
  height: 170px;
  background: #fff;
  position: relative;
  border-radius: 10px;
  box-shadow: 0 15px 30px rgba(0,0,0,0.15);
}

.envelope:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  border-left: 130px solid transparent;
  border-right: 130px solid transparent;
  border-top: 90px solid #ffd1dc;
}

.heart {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: #ff4d6d;
  color: #fff;
  padding: 18px 22px;
  border-radius: 50%;
  font-weight: bold;
  box-shadow: 0 0 15px rgba(255,77,109,0.7);
  animation: pulse 1.5s infinite;
}

/* ---------- LETTER ---------- */
#letter-container {
  display: none;
  max-width: 800px;
  background: #fffafc;
  padding: 40px;
  border-radius: 18px;
  box-shadow: 0 20px 50px rgba(0,0,0,0.2);
  animation: fadeIn 1.5s ease forwards;
  overflow-y: auto;
  max-height: 90vh;
}

#letter-container h1 {
  font-family: 'Great Vibes', cursive;
  font-size: 48px;
  color: #ff4d6d;
  text-align: center;
  margin-bottom: 30px;
}

#letter-container p {
  font-size: 16px;
  line-height: 1.8;
  white-space: pre-wrap;
}

.signature {
  margin-top: 40px;
  text-align: right;
  font-family: 'Great Vibes', cursive;
  font-size: 30px;
}

/* ---------- HEARTS ---------- */
.heart-float {
  position: fixed;
  bottom: 0;
  font-size: 24px;
  animation: rise 4s linear forwards;
  pointer-events: none;
}

/* ---------- ANIMATIONS ---------- */
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

@keyframes pulse {
  0% { transform: translate(-50%, -50%) scale(1); }
  50% { transform: translate(-50%, -50%) scale(1.1); }
  100% { transform: translate(-50%, -50%) scale(1); }
}

@keyframes fadeIn {
  from { opacity: 0; transform: scale(0.9); }
  to { opacity: 1; transform: scale(1); }
}

@keyframes rise {
  0% {
    transform: translateY(0) scale(1);
    opacity: 1;
  }
  100% {
    transform: translateY(-100vh) scale(1.5);
    opacity: 0;
  }
}
</style>
</head>

<body>

<div id="envelope-container">
  <div class="envelope">
    <div class="heart">CLICK ME</div>
  </div>
</div>

<div id="letter-container">
  <h1>To the love of my life, Isaac</h1>

  <p>
First of all I just wanted to say that you mean the world to me, I may not able to tell you this everyday (am not a very "words of affirmation" type of person) but somehow it still puzzles me how you could make me discover something in me that I've never known before. You have this effect on me that I can do things I never thought I could do.

At this point I'm really starting to question myself "do I really know myself?" because now I finally understand the thing old people say that "Love can change you" and it did change me, in a way I never expected, you made me feel more confident about myself and to the things I do—you even made me love myself more, you made me wanted to live longer to see the day when we'll spend with each other for eternity (Dramatic? I know).

You made me act like a whole different person (heck, I didn't even think that I will be as cringe as I am today). And like I've told you, I had never been in a relationship before because I really don't want commitments especially when I don't like things that aren't certain, BUT YOU SIRRRR! Is a different breed, I don't know how you made me HAVE A DAMN PLAN about our future, considering I'm the type of person who acts on impulse.

You made me feel like maybe I'm meant for something good and that I need to be careful of my choices coz it can affect everything I am trying so hard to change and with everything that we have between us right now...I never want it to end.

I love you so muchhh my husband, my baby, my good boy, the love of my life, mi amor, my honeyy!!! And thank you for being the best thing that has ever happened to me, and now I can't even imagine my future without you.

You're the best thing that has ever happened to me this year and I wanted to be with you REALLY. I'm dead serious about all the plans I've made and every single thing I've told you...I really wanted to have a life with you Isaac and I mean it.

I love you so damn much, so much that I wanted to be the best version of myself, and be the best partner to you.
  </p>

  <div class="signature">
    — Your Wife 💋🫶
  </div>
</div>

<script>
const envelope = document.getElementById('envelope-container');
const letter = document.getElementById('letter-container');

envelope.addEventListener('click', () => {
  envelope.style.display = 'none';
  letter.style.display = 'block';
});

letter.addEventListener('scroll', () => {
  if (letter.scrollTop + letter.clientHeight >= letter.scrollHeight - 10) {
    scatterHearts();
  }
});

function scatterHearts() {
  for (let i = 0; i < 25; i++) {
    const heart = document.createElement('div');
    heart.className = 'heart-float';
    heart.innerText = '💖';
    heart.style.left = Math.random() * 100 + 'vw';
    heart.style.animationDuration = (3 + Math.random() * 2) + 's';
    document.body.appendChild(heart);

    setTimeout(() => heart.remove(), 5000);
  }
}
</script>

</body>
</html>
