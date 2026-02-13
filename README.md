<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<title>❤️ بسملة</title>

<style>
body{
  margin:0;
  font-family: Arial;
  background: linear-gradient(135deg,#ff4e50,#fc913a);
  color:white;
  text-align:center;
}

h1{
  margin-top:60px;
  font-size:60px;
}

p{
  font-size:28px;
}

#counter{
  font-size:40px;
  margin-top:20px;
  font-weight:bold;
}

button{
  margin-top:40px;
  padding:15px 30px;
  font-size:22px;
  border:none;
  border-radius:15px;
  background:white;
  color:#ff4e50;
  cursor:pointer;
}
</style>
</head>

<body>

<h1>❤️ بسملة ❤️</h1>

<p>بحبك 💖</p>

<div id="counter"></div>

<button onclick="playSong()">اضغطي هنا 🎵</button>

<audio id="song" src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3"></audio>

<script>
var startDate = new Date("2025-10-12");

function updateCounter(){
  var now = new Date();
  var diff = now - startDate;

  var days = Math.floor(diff / (1000*60*60*24));
  var hours = Math.floor(diff / (1000*60*60)) % 24;
  var minutes = Math.floor(diff / (1000*60)) % 60;
  var seconds = Math.floor(diff / 1000) % 60;

  document.getElementById("counter").innerHTML =
    days + " يوم 💕 " +
    hours + " ساعة 💕 " +
    minutes + " دقيقة 💕 " +
    seconds + " ثانية";
}

setInterval(updateCounter,1000);

function playSong(){
  document.getElementById("song").play();
}
</script>

</body>
</html>
