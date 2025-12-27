<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<title>Happy New Year 2026</title>

<style>
body{
    margin:0;
    overflow:hidden;
    text-align:center;
    font-family: Arial, sans-serif;
    background: radial-gradient(circle, #1a0026, #000);
    color:white;
}

/* Text */
h1{
    margin-top:80px;
    font-size:42px;
    color:#ffd700;
}
h2{
    margin-top:10px;
    font-size:26px;
    color:#00ffcc;
}
p{
    font-size:20px;
}

/* Input & Button */
input{
    padding:10px;
    font-size:18px;
    border-radius:8px;
    border:none;
    margin-top:15px;
}
button{
    margin-top:20px;
    padding:12px 25px;
    font-size:18px;
    background:#00c853;
    color:white;
    border:none;
    border-radius:10px;
    cursor:pointer;
}

/* Fireworks */
.firework{
    position:absolute;
    width:6px;
    height:6px;
    background:white;
    border-radius:50%;
    animation: explode 1.5s infinite;
}

@keyframes explode{
    0%{transform:scale(0); opacity:1;}
    100%{transform:scale(20); opacity:0;}
}
</style>
</head>

<body>

<h1>🎆 Happy New Year 2026 🎆</h1>
<h2>🕉️ जय श्री राम | जय महाकाल 🕉️</h2>
<p>आपके जीवन में सुख, शांति और सफलता आए</p>

<input type="text" id="name" placeholder="अपना नाम लिखो">
<br>
<button onclick="share()">WhatsApp पर भेजें</button>

<script>
/* WhatsApp Share */
function share(){
    var name=document.getElementById("name").value;
    if(name===""){ alert("नाम लिखो 😊"); return; }

    var msg="🎆 Happy New Year 2026 🎆%0A" +
            "🕉️ जय श्री राम | जय महाकाल 🕉️%0A%0A" +
            "आपको नए साल की शुभकामनाएँ 🌟%0A%0A" +
            "भेजने वाला: " + name;

    window.open("https://wa.me/?text="+msg,"_blank");
}

/* Fireworks Effect */
setInterval(()=>{
    let f=document.createElement("div");
    f.className="firework";
    f.style.left=Math.random()*window.innerWidth+"px";
    f.style.top=Math.random()*window.innerHeight+"px";
    f.style.backgroundColor=
      "hsl("+Math.random()*360+",100%,50%)";
    document.body.appendChild(f);
    setTimeout(()=>f.remove(),1500);
},300);
</script>

</body>
</html>
