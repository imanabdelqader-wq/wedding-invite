<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>عدّاد زفاف محمود وإيمان</title>

<style>
body{
    margin:0;
    font-family:Tahoma,sans-serif;
    background:linear-gradient(135deg,#f8d7da,#fff,#f6e6ff);
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
}

.card{
    background:white;
    padding:35px;
    border-radius:25px;
    width:90%;
    max-width:500px;
    text-align:center;
    box-shadow:0 10px 30px rgba(0,0,0,.15);
}

h1{
    color:#c2185b;
    margin-bottom:10px;
}

h2{
    color:#555;
    font-weight:normal;
}

#countdown{
    display:flex;
    justify-content:center;
    gap:15px;
    margin:30px 0;
    flex-wrap:wrap;
}

.box{
    background:#c2185b;
    color:white;
    padding:15px;
    border-radius:15px;
    min-width:70px;
}

.box span{
    display:block;
    font-size:30px;
    font-weight:bold;
}

.footer{
    color:#666;
    font-size:18px;
}
</style>
</head>

<body>

<div class="card">

<h1>💍 محمود فحماوي ❤ إيمان عبد القادر</h1>

<h2>يسرّنا دعوتكم لحضور حفل زفافنا</h2>

<p>📍 قاعة مؤتة</p>

<p>📅 الاثنين 27 / 7 / 2026</p>

<div id="countdown">

<div class="box">
<span id="days">0</span>
يوم
</div>

<div class="box">
<span id="hours">0</span>
ساعة
</div>

<div class="box">
<span id="minutes">0</span>
دقيقة
</div>

<div class="box">
<span id="seconds">0</span>
ثانية
</div>

</div>

<div class="footer">
✨ ننتظركم لتشاركونا أجمل لحظات عمرنا ✨
</div>

</div>

<script>

const weddingDate = new Date("July 27, 2026 21:00:00").getTime();

const timer = setInterval(function(){

const now = new Date().getTime();

const distance = weddingDate - now;

const days = Math.floor(distance/(1000*60*60*24));
const hours = Math.floor((distance%(1000*60*60*24))/(1000*60*60));
const minutes = Math.floor((distance%(1000*60*60))/(1000*60));
const seconds = Math.floor((distance%(1000*60))/1000);

document.getElementById("days").innerHTML=days;
document.getElementById("hours").innerHTML=hours;
document.getElementById("minutes").innerHTML=minutes;
document.getElementById("seconds").innerHTML=seconds;

if(distance<0){
clearInterval(timer);
document.getElementById("countdown").innerHTML="<h2>🎉 ألف مبارك الزواج 🎉</h2>";
}

},1000);

</script>

</body>
</html>
