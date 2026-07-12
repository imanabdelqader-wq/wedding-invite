<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>دعوة زفاف محمود وإيمان</title>

<link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Cairo:wght@400;700&display=swap" rel="stylesheet">

<link rel="stylesheet" href="style.css">

</head>

<body>

<div class="flowers left">🌷🌷🌷</div>
<div class="flowers right">🌷🌷🌷</div>

<div class="card">

<p class="verse">
وَمِنْ آيَاتِهِ أَنْ خَلَقَ لَكُم مِّنْ أَنفُسِكُمْ أَزْوَاجًا لِّتَسْكُنُوا إِلَيْهَا
وَجَعَلَ بَيْنَكُم مَّوَدَّةً وَرَحْمَةً ۚ إِنَّ فِي ذَٰلِكَ لَآيَاتٍ
لِّقَوْمٍ يَتَفَكَّرُونَ
</p>


<h3>عائلة السيد</h3>
<h2>عبد الحكيم عبد القادر</h2>

<h3>عائلة السيد</h3>
<h2>محمد فحماوي</h2>


<p class="invite">
بكل الود والحب يتشرفون بدعوتكم لحضور حفل زفاف
</p>


<h1>محمود فحماوي</h1>
<span class="and">♥</span>
<h1>إيمان عبد القادر</h1>


<h2 class="hall">قاعات مؤتة</h2>


<div id="countdown"></div>


<a class="button" href="https://maps.app.goo.gl/cTVhy5NQSXxVDeRg8" target="_blank">
موقع القاعة
</a>


<p class="children">
يمنع اصطحاب الأطفال<br>
شاكرين تفهمكم وتعاونكم
</p>


</div>


<script src="script.js"></script>

</body>
</html>
body{
margin:0;
background:#f3e4cc;
font-family:'Cairo',sans-serif;
color:#5a4030;
text-align:center;
}


.card{
background:#fff8eb;
max-width:650px;
margin:40px auto;
padding:35px;
border-radius:25px;
box-shadow:0 0 25px #c9a97a;
position:relative;
}


.verse{
font-family:'Amiri',serif;
font-size:23px;
line-height:2;
}


h1{
font-family:'Amiri',serif;
font-size:42px;
margin:10px;
}


h2{
font-family:'Amiri',serif;
}


.invite{
font-size:22px;
margin:25px;
}


.and{
font-size:30px;
color:#b88a5a;
}


.hall{
font-size:30px;
margin:25px;
}


#countdown{
font-size:25px;
font-weight:bold;
margin:25px;
}


.button{
display:inline-block;
background:#b89062;
color:white;
padding:14px 35px;
border-radius:30px;
text-decoration:none;
font-size:20px;
}


.children{
margin-top:35px;
font-size:18px;
}


.flowers{
position:fixed;
font-size:45px;
top:50%;
transform:translateY(-50%);
}


.left{
left:10px;
}


.right{
right:10px;
}


@media(max-width:600px){

.card{
margin:15px;
padding:20px;
}

.verse{
font-size:18px;
}

h1{
font-size:34px;
}

.flowers{
font-size:30px;
}

}
let weddingDate = new Date("July 27, 2026 21:00:00").getTime();


let timer = setInterval(function(){

let now = new Date().getTime();

let distance = weddingDate - now;


let days = Math.floor(distance/(1000*60*60*24));
let hours = Math.floor((distance%(1000*60*60*24))/(1000*60*60));
let minutes = Math.floor((distance%(1000*60*60))/(1000*60));
let seconds = Math.floor((distance%(1000*60))/1000);


document.getElementById("countdown").innerHTML =
days+" يوم | "+hours+" ساعة | "+minutes+" دقيقة | "+seconds+" ثانية";


if(distance < 0){
clearInterval(timer);
document.getElementById("countdown").innerHTML="تم بحمد الله 🤍";
}


},1000);
