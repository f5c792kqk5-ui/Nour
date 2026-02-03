# Nour
&lt;!DOCTYPE html>&lt;html>&lt;body style="display:flex;justify-content:center;align-items:center;height:100vh;background:#ffe6f0;font-size:2rem;color:#ff4d88;">نور أحبك &lt;span style="animation:beat 1s infinite;">💗&lt;/span>&lt;style>@keyframes beat{0%,100%{transform:scale(1)}50%{transform:scale(1.3)}}&lt;/style>&lt;/body>&lt;/html>
<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<title>نور 💗 من صهيب</title>
<style>
* { box-sizing: border-box; }
body {
  margin: 0;
  height: 100vh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #ffe6f0, #fff5fa);
  font-family: 'Poppins', sans-serif;
}

.container {
  text-align: center;
  z-index: 2;
}

h1 {
  font-size: 3rem;
  color: #ff4d88;
  animation: pulse 1.5s infinite alternate;
}

@keyframes pulse {
  from { transform: scale(1); }
  to { transform: scale(1.1); }
}

.buttons {
  margin-top: 30px;
  position: relative;
  height: 80px;
}

button {
  padding: 12px 30px;
  font-size: 1.1rem;
  border: none;
  border-radius: 30px;
  cursor: pointer;
  transition: 0.3s ease;
  position: absolute;
}

.yes {
  background: #7ed957;
  color: white;
  left: 50%;
  transform: translateX(-120%);
}

.no {
  background: #ff6b6b;
  color: white;
  left: 50%;
  transform: translateX(20%);
}

.message {
  display: none;
  margin-top: 30px;
  font-size: 2rem;
  color: #ff4d88;
  animation: pop 0.8s ease forwards;
}

@keyframes pop {
  from { transform: scale(0); opacity: 0; }
  to { transform: scale(1); opacity: 1; }
}

.heart {
  position: absolute;
  bottom: -50px;
  font-size: 24px;
  animation: floatUp linear infinite;
  opacity: 0.8;
}

@keyframes floatUp {
  from { transform: translateY(0) scale(1); opacity: 1; }
  to { transform: translateY(-110vh) scale(1.5); opacity: 0; }
}

audio { display: none; }

@keyframes shake {
  0% { transform: translate(0,0); }
  25% { transform: translate(-2px,2px); }
  50% { transform: translate(2px,-2px); }
  75% { transform: translate(-2px,2px); }
  100% { transform: translate(0,0); }
}

.shake { animation: shake 0.2s infinite; }
</style>
</head>

<body>

<div class="container">
<h1 class="shake">نور، حبيبتي 💗💗</h1>

<div class="buttons">
  <button class="yes" onclick="sayYes()">Yes 💕</button>
  <button class="no" onmouseover="moveNo()">No 😜</button>
</div>

<div class="message" id="message">
نور، كل لحظة أفكر فيك، قلبي يهتز فرحًا، كأن الدنيا كلها ضحكت لي. أحبك أكثر من أي شيء، أحب ضحكتك، نظرتك، وحتى صمتك الجميل. معك أشعر بالأمان، بالدفء، وكأن كل شيء يصبح أسهل. كل نبضة من قلبي تنادي باسمك، وكل لحظة تمرّ بدونك تبدو طويلة. أحبك بلا شروط، بلا حدود، بلا قيود. 💖
</div>
</div>

<audio autoplay loop>
  <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_4b3b1cdb28.mp3" type="audio/mpeg">
</audio>

<script>
function moveNo() {
  const noBtn = document.querySelector('.no');
  const x = Math.random() * 200 - 100;
  const y = Math.random() * 100 - 50;
  noBtn.style.transform = `translate(${x}px, ${y}px)`;
}

function sayYes() {
  document.getElementById('message').style.display = 'block';
}

function createHeart() {
  const heart = document.createElement("div");
  heart.classList.add("heart");
  heart.innerText = "💗";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.animationDuration = (3 + Math.random() * 3) + "s";
  heart.style.fontSize = (20 + Math.random() * 20) + "px";
  document.body.appendChild(heart);
  setTimeout(() => { heart.remove(); }, 6000);
}

setInterval(createHeart, 300);

// اهتزاز خفيف عند فتح الصفحة
if(navigator.vibrate){ navigator.vibrate([100,50,100]); }
</script>

</body>
</html>
