<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fortnite Loadout</title>

<style>
body{
    background:#121212;
    color:white;
    text-align:center;
    font-family:Arial, sans-serif;
}

#mapa-container{
    position:relative;
    display:inline-block;
}

#mapa{
    max-width:90%;
    border:2px solid white;
    border-radius:10px;
}

.marcador{
    position:absolute;
    width:20px;
    height:20px;
    background:red;
    border:2px solid white;
    border-radius:50%;
    transform:translate(-50%, -50%);
    pointer-events:none;
}
</style>
</head>

<body>

<h1>Fortnite Loadout</h1>
<p>Clique no mapa para marcar seu local de drop.</p>

<div id="mapa-container">
    <img src="mapinha.jpg" id="mapa" alt="Mapa Fortnite">
</div>

<script>
const mapa = document.getElementById("mapa");
const container = document.getElementById("mapa-container");

mapa.addEventListener("click", function(e){

    const marcador = document.createElement("div");
    marcador.classList.add("marcador");

    marcador.style.left = e.offsetX + "px";
    marcador.style.top = e.offsetY + "px";

    container.appendChild(marcador);
});
</script>

</body>
</html>
