# love-stars.html  
<div dir="rtl"># </div>  
<!DOCTYPE html>  
<html lang="ar">  
<head>  
<meta charset="UTF-8">  
<title>**نجوم** **حبنا** ✨</title>  
  
<style>  
body {  
    margin: 0;  
    font-family: 'Tahoma', sans-serif;  
    background: url("https://images.unsplash.com/photo-1444703686981-a3abbc4d4fe3") no-repeat center center fixed;  
    background-size: cover;  
    height: 100vh;  
    overflow: hidden;  
    color: white;  
}  
  
/* **عنوان** */  
#title {  
    text-align: center;  
    margin-top: 15px;  
    font-size: 26px;  
    text-shadow: 0 0 10px pink;  
}  
  
/* **عداد** **السنة** */  
#countdown {  
    text-align: center;  
    margin-top: 10px;  
    font-size: 18px;  
    color: pink;  
}  
  
/* **النجوم** */  
.star {  
    position: absolute;  
    font-size: 28px;  
    color: gold;  
    cursor: pointer;  
    animation: float 6s infinite ease-in-out, twinkle 2s infinite alternate;  
}  
  
@keyframes float {  
    0% { transform: translateY(0); }  
    50% { transform: translateY(-20px); }  
    100% { transform: translateY(0); }  
}  
  
@keyframes twinkle {  
    from { opacity: 0.6; }  
    to { opacity: 1; }  
}  
  
/* **نافذة** **الحب** */  
#popup {  
    display: none;  
    position: fixed;  
    top: 50%;  
    left: 50%;  
    transform: translate(-50%, -50%);  
    background: rgba(0,0,0,0.85);  
    padding: 25px;  
    width: 320px;  
    border-radius: 20px;  
    text-align: center;  
    box-shadow: 0 0 25px pink;  
}  
  
#popup button {  
    margin-top: 15px;  
    padding: 8px 20px;  
    border: none;  
    border-radius: 15px;  
    background: pink;  
    font-size: 14px;  
    cursor: pointer;  
}  
</style>  
</head>  
  
<body>  
  
<!-- **موسيقى** -->  
<audio autoplay loop>  
  <source src="https://cdn.pixabay.com/audio/2022/03/15/audio_24c9c1d5e4.mp3" type="audio/mpeg">  
</audio>  
  
<div id="title">✨ **نجوم** **حبنا** ✨</div>  
<div id="countdown"></div>  
  
<!-- **النجوم** -->  
<div class="star" style="top:15%; left:20%;" onclick="showLove(0)">⭐</div>  
<div class="star" style="top:30%; left:70%;" onclick="showLove(1)">⭐</div>  
<div class="star" style="top:45%; left:40%;" onclick="showLove(2)">⭐</div>  
<div class="star" style="top:65%; left:60%;" onclick="showLove(3)">⭐</div>  
<div class="star" style="top:20%; left:50%;" onclick="showLove(4)">⭐</div>  
<div class="star" style="top:80%; left:25%;" onclick="showLove(5)">⭐</div>  
<div class="star" style="top:55%; left:15%;" onclick="showLove(6)">⭐</div>  
<div class="star" style="top:10%; left:80%;" onclick="showLove(7)">⭐</div>  
<div class="star" style="top:40%; left:85%;" onclick="showLove(8)">⭐</div>  
<div class="star" style="top:75%; left:45%;" onclick="showLove(9)">⭐</div>  
<div class="star" style="top:60%; left:75%;" onclick="showLove(10)">⭐</div>  
<div class="star" style="top:35%; left:10%;" onclick="showLove(11)">⭐</div>  
  
<!-- **نافذة** -->  
<div id="popup">  
    <p id="loveText"></p>  
    <button onclick="closeLove()">**إغلاق** 💕</button>  
</div>  
  
<script>  
// ✏️ **عدّل** **الاسم** **هون**  
const herName = "**حبيبتي**";  
  
// **رسائل** **الحب**  
const messages = [  
`**أول** **نجمة** **إلك** **يا** ${herName}**،** **بحبك** **حب** **ما** **إلو** **نهاية** ❤️`,  
`**معك** **عرفت** **شو** **يعني** **حب** **حقيقي،** **وكل** **سنة** **وأنا** **معك** 🌹`,  
`**السنة** **الجديدة** **رح** **تكون** **أحلى** **بس** **لأنك** **معي** ✨`,  
`**إنتي** **مش** **بس** **حب،** **إنتي** **روحي** **وكل** **دنيتي** 💖`,  
`**وجودك** **بحياتي** **هو** **أعظم** **هدية** 🌸`,  
`**بحبك** **قد** **عدد** **نجوم** **السما** ⭐`,  
`**كل** **لحظة** **معك** **بتساوي** **عمر** **من** **السعادة** 💕`,  
`**وعد** **مني**: **كل** **سنة** **جديدة** **وأنا** **جنبك** 🫶`,  
`**إنتي** **أحلى** **شي** **صار** **معي** **بهاي** **السنة** 📖❤️`,  
`**معك** **بنسى** **العالم** **وبعيش** **للحب** **بس** 💗`,  
`**هاي** **السنة** **كانت** **جميلة،** **بس** **إنتي** **خليتيها** **مثالية** ✨`,  
`**آخر** **نجمة** **وأصدق** **كلمة**: **بحبك** **اليوم** **وبكرة** **وكل** **السنين** 💞`  
];  
  
// **إظهار** **الرسالة**  
function showLove(i) {  
    document.getElementById("loveText").innerText = messages[i];  
    document.getElementById("popup").style.display = "block";  
}  
  
function closeLove() {  
    document.getElementById("popup").style.display = "none";  
}  
  
// **عداد** **السنة** **الجديدة**  
function updateCountdown() {  
    const now = new Date();  
    const newYear = new Date(now.getFullYear() + 1, 0, 1);  
    const diff = newYear - now;  
  
    const days = Math.floor(diff / (1000 * 60 * 60 * 24));  
    const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);  
    const minutes = Math.floor((diff / (1000 * 60)) % 60);  
    const seconds = Math.floor((diff / 1000) % 60);  
  
    document.getElementById("countdown").innerText =  
        `⏳ **باقي** ${days} **يوم** ${hours} **ساعة** ${minutes} **دقيقة** ${seconds} **ثانية** **على** **السنة** **الجديدة** **معنا** 💕`;  
}  
  
setInterval(updateCountdown, 1000);  
updateCountdown();  
</script>  
  
</body>  
</html>  
