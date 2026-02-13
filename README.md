<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Veronica 💘</title>

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:#ffe6f0;
    font-family:Arial, sans-serif;
    overflow:hidden;
}

.card{
    background:white;
    padding:30px;
    border-radius:20px;
    box-shadow:0 10px 30px rgba(0,0,0,0.15);
    text-align:center;
}

h1{
    margin-bottom:20px;
}

button{
    padding:12px 20px;
    margin:10px;
    border:none;
    border-radius:12px;
    font-size:16px;
    cursor:pointer;
    transition:0.2s;
}

#yes{
    background:#ff3b7a;
    color:white;
}

#no{
    background:#ddd;
}

#message{
    margin-top:15px;
    font-weight:bold;
    color:#ff3b7a;
}
</style>
</head>

<body>

<div class="card">
    <h1>Veronica, tu veux être ma Valentine ? 💘</h1>
    <button id="yes">Oui 😍</button>
    <button id="no">Non 🙈</button>
    <p id="message"></p>
</div>

<script>
const noBtn = document.getElementById("no");
const yesBtn = document.getElementById("yes");
const message = document.getElementById("message");

// Le bouton NON bouge à chaque tentative
function moveNo(){
    const x = Math.random() * 300 - 150;
    const y = Math.random() * 200 - 100;
    noBtn.style.transform = `translate(${x}px, ${y}px)`;
}

noBtn.addEventListener("click", moveNo);
noBtn.addEventListener("touchstart", moveNo);

yesBtn.addEventListener("click", function(){
    message.innerHTML = "Je savais 😍💍";
});
</script>

</body>
</html>
