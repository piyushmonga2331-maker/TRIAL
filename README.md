# TRIAL
VALENTINES
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Piyush ❤️ Priyanka</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap');

body{
  margin:0;
  font-family:'Poppins',sans-serif;
  background: linear-gradient(135deg,#ff9a9e,#fad0c4);
  height:100vh;
  overflow:hidden;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
}

.container{
  background:white;
  padding:25px;
  border-radius:20px;
  width:90%;
  max-width:380px;
  box-shadow:0 10px 30px rgba(0,0,0,0.2);
  position:relative;
}

h1{
  color:#e63946;
  font-size:24px;
}

button{
  padding:12px 20px;
  border:none;
  border-radius:50px;
  font-size:16px;
  cursor:pointer;
  margin:10px;
  transition:0.3s;
}

#yes{
  background:#e63946;
  color:white;
}

#no{
  background:#444;
  color:white;
  position:absolute;
}

.character{
  font-size:40px;
  position:absolute;
  top:-30px;
  animation: jump 1s infinite;
}

@keyframes jump{
  0%{transform:translateY(0)}
  50%{transform:translateY(-12px)}
  100%{transform:translateY(0)}
}

#photoSection{
  display:none;
  margin-top:15px;
}

.photos{
  display:flex;
  gap:10px;
  justify-content:center;
  margin:10px 0;
}

.photos img{
  width:80px;
  height:80px;
  border-radius:10px;
  object-fit:cover;
}

input{
  padding:8px;
  margin:5px;
  width:90%;
  border-radius:8px;
  border:1px solid #ccc;
}

.success{
  display:none;
  color:#2a9d8f;
  font-weight:600;
  margin-top:15px;
}
</style>
</head>

<body>

<div class="container" id="box">
  <div class="character">🐰</div>
  <h1>Priyanka, will you be my Valentine? ❤️</h1>

  <button id="yes">YES 💖</button>
  <button id="no">NO 😜</button>

  <div id="photoSection">
    <h3>Our Cute Memories 🥹</h3>
    <div class="photos">
      <!-- PUT YOUR IMAGES HERE -->
      <img src="photo1.jpg">
      <img src="photo2.jpg">
    </div>

    <p>Okay okay… pick the date and place then 😏</p>
    <input type="date" placeholder="Select Date">
    <input type="text" placeholder="Where do you want to go?">
  </div>

  <div class="success" id="successMsg">
    Yayyy Budgdi said YES! 💍❤️  
    Piyush is the happiest person alive!!!
  </div>
</div>

<script>
const noBtn = document.getElementById("no");
const box = document.getElementById("box");

noBtn.addEventListener("mouseover", moveButton);
noBtn.addEventListener("click", showPhotos);

function moveButton(){
  const x = Math.random() * (box.clientWidth - 100);
  const y = Math.random() * (box.clientHeight - 50);
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
}

function showPhotos(){
  document.getElementById("photoSection").style.display="block";
}

document.getElementById("yes").onclick = function(){
  document.getElementById("successMsg").style.display="block";
}
</script>

</body>
</html>
