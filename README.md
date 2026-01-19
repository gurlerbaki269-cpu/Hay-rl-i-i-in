# Hay-rl-i-i-in
Hayırlı iş
<!DOCTYPE html><html lang="tr">
<head>
<meta charset="UTF-8">
<title>Bir Soru 💚</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
*{box-sizing:border-box;}
body{
    margin:0;
    background:#111;
    color:white;
    font-family:Arial, sans-serif;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    height:100vh;
    text-align:center;
    overflow:hidden;
}
h1{margin-bottom:40px;padding:0 15px;}
button{
    border:none;
    border-radius:14px;
    font-size:1.6rem;
    padding:16px 50px;
    cursor:pointer;
    transition:0.3s ease;
}
#yes{background:#2ecc71;color:black;}
#no{background:#e74c3c;color:white;margin-top:25px;}
#dance{
    display:none;
    position:fixed;
    inset:0;
    background:black;
    z-index:999;
    justify-content:center;
    align-items:center;
}
#dance img{max-width:90%;max-height:90%;}
</style>
</head>
<body>
<h1>Hira benimle çıkar mısın? 💚</h1>
<button id="yes">EVET</button>
<button id="no">HAYIR</button>
<div id="dance">
    <img src="https://media.tenor.com/2roX3uxz_68AAAAC/cat-dance.gif" alt="dance">
</div>
<script>
let noCount = 0;
let yesSize = 1;
let noSize = 1;
const yesBtn = document.getElementById("yes");
const noBtn = document.getElementById("no");
noBtn.onclick = () => {
    noCount++;
    if(noCount <= 5){
        yesSize += 0.25;
        noSize = Math.max(noSize - 0.18, 0.4);
        yesBtn.style.transform = `scale(${yesSize})`;
        noBtn.style.transform = `scale(${noSize})`;
    } else {
        document.body.style.background = "#2ecc71";
        noBtn.style.display = "none";
        yesBtn.style.transform = "scale(3)";
    }
};
yesBtn.onclick = () => {
    document.getElementById("dance").style.display = "flex";
};
</script>
</body>
</html>
