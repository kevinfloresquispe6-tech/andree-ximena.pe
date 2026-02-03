<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Ximena & Andree</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display&family=Rock+Salt&display=swap" rel="stylesheet">

<style>
*{box-sizing:border-box}

body{
    margin:0;
    font-family:'Playfair Display', serif;
    background:#0e0e0e;
    color:#000;
    overflow-x:hidden;
}

/* AUDIO */
audio{display:none}

/* ================= PORTADA ================= */
header{
    min-height:100vh;
    background:
        linear-gradient(rgba(0,0,0,.35), rgba(0,0,0,.55)),
        url("imagenes/cora.jpg") center/cover no-repeat;
    background-attachment:fixed;
    padding:80px 8%;
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:60px;
    position:relative;
}

/* TEXTO */
.hero-text{
    max-width:520px;
    color:#fff;
    z-index:5;
}

.hero-text h1{
    font-family:'Rock Salt', cursive;
    font-size:3.8em;
}

.hero-text p{
    font-size:1.25em;
}

/* BOTONES */
.buttons{margin-top:30px}

.buttons button{
    background:#fff;
    border:3px solid #000;
    padding:14px 28px;
    margin:8px;
    cursor:pointer;
    transition:.3s;
}

.buttons button:hover{
    background:#000;
    color:#fff;
}

/* FOTOS DERECHA */
.hero-photos{
    display:flex;
    gap:35px;
    z-index:4;
}

/* POLAROID */
.polaroid{
    background:#fff;
    padding:12px;
    width:220px;
    box-shadow:0 18px 35px rgba(0,0,0,.7);
    transition:.4s;
}

.polaroid:hover{
    transform:scale(1.08) rotate(1deg);
}

.polaroid img,
.polaroid video{
    width:100%;
    height:210px;
    object-fit:cover;
}

/* GUITARRAS */
.guitar{
    position:absolute;
    top:-150px;
    width:60px;
    opacity:.6;
    animation:fall linear infinite;
    pointer-events:none;
}

@keyframes fall{
    from{transform:translateY(-200px) rotate(0deg);opacity:0}
    to{transform:translateY(120vh) rotate(360deg);opacity:1}
}

/* SECCIONES */
section{
    padding:120px 10%;
    display:none;
    animation:fadeSlide .8s ease;
}

@keyframes fadeSlide{
    from{opacity:0; transform:translateY(40px)}
    to{opacity:1; transform:translateY(0)}
}

/* XIMENA */
#ella{
    background:
        linear-gradient(rgba(255,255,255,.65), rgba(255,230,240,.65)),
        url("imagenes/star.jpg") center/cover fixed;
}

/* NOSOTROS */
#nosotros{
    background:
        linear-gradient(rgba(255,255,255,.7), rgba(240,240,240,.7)),
        url("imagenes/star.jpg") center/cover fixed;
}

/* MOMENTOS */
#momentos{
    background:
        linear-gradient(rgba(0,0,0,.45), rgba(0,0,0,.65)),
        url("imagenes/cora.jpg") center/cover fixed;
    color:#fff;
}

/* TITULOS */
section h2{
    font-family:'Rock Salt', cursive;
    font-size:2.8em;
    margin-bottom:50px;
}

/* FLEX */
.flex{
    display:flex;
    flex-wrap:wrap;
    gap:40px;
    align-items:center;
}

.media-row{
    display:flex;
    gap:30px;
    flex-wrap:wrap;
    justify-content:center;
    margin-top:40px;
}

/* MOSAICO */
.mosaic{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:40px;
}

.mosaic .polaroid:nth-child(2n){transform:rotate(3deg)}
.mosaic .polaroid:nth-child(3n){transform:rotate(-4deg)}

/* FOOTER */
footer{
    background:#000;
    color:#fff;
    text-align:center;
    padding:40px;
}
</style>
</head>

<body>

<!-- 🎵 AUDIO -->
<audio id="musica" loop>
    <source src="imagenes/Ojos de Ángel (Acústico) [eIzSjDdvOmU] (2).mp3" type="audio/mpeg">
</audio>

<header>
    <div class="hero-text">
        <h1>Ximena & Andree</h1>
        <p>Amor intenso, imperfecto y real.<br>Un 14 de febrero hecho con el corazón.</p>

        <div class="buttons">
            <button onclick="go('ella')">Ximena</button>
            <button onclick="go('nosotros')">Nosotros</button>
            <button onclick="go('momentos')">Momentos</button>
        </div>
    </div>

    <div class="hero-photos">
        <div class="polaroid"><img src="imagenes/1.jpg"></div>
        <div class="polaroid"><img src="imagenes/2.jpg"></div>
    </div>

    <img src="imagenes/guitarra.png" class="guitar" style="left:10%;animation-duration:14s;">
    <img src="imagenes/guitarra.png" class="guitar" style="left:40%;animation-duration:18s;">
    <img src="imagenes/guitarra.png" class="guitar" style="left:70%;animation-duration:16s;">
</header>

<section id="ella">
    <h2>Ximena</h2>
    <div class="flex">
        <p>Misteriosa, intensa y hermosa. El caos que aprendí a amar.</p>
        <div class="polaroid"><img src="imagenes/3.jpg"></div>
        <div class="polaroid"><img src="imagenes/4.jpg"></div>
        <div class="polaroid"><img src="imagenes/5.jpg"></div>
    </div>
</section>

<section id="nosotros">
    <h2>Nuestra Historia</h2>

    <p style="max-width:850px;margin-bottom:40px">
        En tus ojos encuentro algo que no sabía nombrar, una calma que me mira distinto,
        como si el mundo se cambiase cuando me observas, son tus ojos de ángel,
        los que me devuelven la fe cuando todo pesa, y en ellos aprendo a quedarme.
        Eres tú, mi música que necesito para existir sin ruido, la que, a tu lado
        hacemos serena música, la melodía que aparece cuando existe el silencio,
        mi canción que amo, mi canción que es sentida, la que acompaña incluso cuando
        no suena. Contigo es respirar al ritmo de alguien más, sé que contigo bastará
        recordarte, tus ojos guiándome y tu música manteniéndome en pie.
    </p>

    <div class="media-row">
        <div class="polaroid"><img src="imagenes/6.jpg"></div>
        <div class="polaroid"><img src="imagenes/7.jpg"></div>
        <div class="polaroid"><video src="imagenes/cd.mp4" controls></video></div>
        <div class="polaroid"><video src="imagenes/cf.mp4" controls></video></div>
    </div>
</section>

<section id="momentos">
    <h2>Momentos Eternos</h2>
    <div class="mosaic">
        <div class="polaroid"><img src="imagenes/8.jpg"></div>
        <div class="polaroid"><img src="imagenes/9.jpg"></div>
        <div class="polaroid"><img src="imagenes/10.jpg"></div>
        <div class="polaroid"><img src="imagenes/11.jpg"></div>
        <div class="polaroid"><img src="imagenes/12.jpg"></div>
        <div class="polaroid"><img src="imagenes/13.jpg"></div>
        <div class="polaroid"><img src="imagenes/14.jpg"></div>
        <div class="polaroid"><img src="imagenes/15.jpg"></div>
        <div class="polaroid"><img src="imagenes/16.jpg"></div>
        <div class="polaroid"><img src="imagenes/17.jpg"></div>
        <div class="polaroid"><img src="imagenes/rd.jpg"></div>
    </div>
</section>

<footer>
    Hecho con amor oscuro — Andree 🖤
</footer>

<script>
function go(id){
    const audio = document.getElementById("musica");
    audio.play().catch(()=>{});

    document.querySelectorAll("section").forEach(s=>s.style.display="none");
    const sec = document.getElementById(id);
    sec.style.display="block";
    sec.scrollIntoView({behavior:"smooth"});
}
</script>

</body>
</html>
