<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Join Korean Server</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;800&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background: url('https://i.imgur.com/A8cpXid.webp') no-repeat center center/cover;
    color: white;
    overflow: hidden;
}

/* NAVBAR */
.navbar {
    position: fixed;
    top: 0;
    width: 100%;
    display: flex;
    align-items: center;
    padding: 15px 40px;
    background: rgba(0,0,0,0.5);
    backdrop-filter: blur(10px);
    z-index: 10;
}

.logo {
    font-weight: 800;
    font-size: 26px;
    margin-right: 40px;
}

.nav-links {
    display: flex;
    gap: 25px;
    font-size: 14px;
}

.nav-links a {
    color: white;
    text-decoration: none;
    opacity: 0.8;
    cursor: pointer;
}

.nav-links a:hover {
    opacity: 1;
}

/* HERO */
.hero {
    height: 100vh;
    display: flex;
    align-items: center;
    padding: 70px 8% 0;
}

.content {
    max-width: 700px;
}

.tag {
    display: inline-block;
    background: #ff7eb9;
    padding: 8px 18px;
    border-radius: 20px;
    font-size: 13px;
    margin-bottom: 20px;
}

h1 {
    font-size: 64px;
    font-weight: 800;
    line-height: 1.1;
    margin: 0 0 20px;
}

.highlight {
    color: #ff8ecf;
}

p {
    font-size: 18px;
    opacity: 0.9;
    margin-bottom: 30px;
}

/* BUTTON */
.btn {
    display: inline-block;
    padding: 16px 40px;
    background: #ff8ecf;
    color: white;
    border-radius: 12px;
    text-decoration: none;
    font-weight: 600;
    font-size: 18px;
    cursor: pointer;
}

/* SOCIALS */
.socials {
    position: fixed;
    top: 55px;
    right: 15px;
    z-index: 100;
    font-size: 12px;
    color: #ff8ecf;
    text-align: right;
}

.socials img {
    width: 45px;
    height: 45px;
    margin-top: 5px;
    border-radius: 10px;
    cursor: pointer;
}

/* MODAL */
.modal {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.75);
    justify-content: center;
    align-items: center;
    z-index: 999;
}

.modal-content {
    background: rgba(20,20,20,0.95);
    padding: 20px;
    width: 85%;
    max-width: 450px;
    border-radius: 14px;
}

.close {
    float: right;
    cursor: pointer;
    font-size: 18px;
}

/* SERVER BUTTONS */
.server {
    background: #ff8ecf;
    margin: 6px 0;
    padding: 10px;
    border-radius: 10px;
    cursor: pointer;
    font-weight: 600;
}

.server:hover {
    opacity: 0.85;
}

.full {
    display: none;
    margin-top: 10px;
    background: rgba(0,0,0,0.5);
    padding: 10px;
    border-radius: 10px;
}

.retry {
    margin-top: 10px;
    background: white;
    color: black;
    padding: 8px;
    border-radius: 8px;
    cursor: pointer;
}
</style>
</head>

<body>

<!-- NAVBAR -->
<div class="navbar">
    <div class="logo">ADOPT ME!</div>

    <div class="nav-links">
        <a onclick="openDiscover()">DISCOVER</a>
        <a href="#">NEWS</a>
        <a href="#">MEDIA</a>
        <a href="#">NEXT UPDATE</a>
        <a href="#">SUPPORT</a>
    </div>
</div>

<!-- HERO -->
<div class="hero">
    <div class="content">

        <div class="tag">KOREA SERVER OFFICIAL</div>

        <h1>JOIN <span class="highlight">KOREAN</span><br>SERVER</h1>

        <p>Lower ping, relaxed trading, and smooth experience.</p>

        <div class="btn" onclick="openServer()">Join Servers</div>

    </div>
</div>

<!-- SOCIALS -->
<div class="socials">
    <div>Our Socials</div>

    <img src="https://i.imgur.com/58ZFOb9.jpeg"
    onclick="event.stopPropagation(); window.open('https://discord.gg/J2w82mGZX','_blank')">
</div>

<!-- SERVER MODAL -->
<div class="modal" id="serverModal">
    <div class="modal-content">

        <span class="close" onclick="closeServer()">X</span>

        <h3>SERVERS</h3>

        <!-- FIXED SERVER 1 & 2 -->
        <div class="server" onclick="openServerLink()">Server 1</div>
        <div class="server" onclick="openServerLink()">Server 2</div>

        <div class="server" onclick="full()">Server 3</div>
        <div class="server" onclick="full()">Server 4</div>
        <div class="server" onclick="full()">Server 5</div>
        <div class="server" onclick="full()">Server 6</div>

        <div class="full" id="fullBox">
            ❌ Server Full
            <div class="retry" onclick="retry()">Retry</div>
        </div>

    </div>
</div>

<!-- DISCOVER MODAL -->
<div class="modal" id="discoverModal">
    <div class="modal-content">

        <span class="close" onclick="closeDiscover()">X</span>

        <h2>About Korean Server</h2>

        <p>
            This Korean Adopt Me trading server is built for a relaxed and friendly experience.
            Players can trade freely without strict value pressure, making it more fun and less stressful.
            <br><br>
            You can meet international traders, join events, and enjoy smooth low-ping gameplay.
            The community is active, beginner-friendly, and focused on enjoyable trading instead of strict rules.
            <br><br>
            Whether you are new or experienced, this server gives you a chill environment to enjoy Adopt Me at your own pace.
        </p>

    </div>
</div>

<script>
function openServer(){
    document.getElementById("serverModal").style.display = "flex";
}

function closeServer(){
    document.getElementById("serverModal").style.display = "none";
}

function full(){
    document.getElementById("fullBox").style.display = "block";
}

function retry(){
    document.getElementById("fullBox").style.display = "none";
}

/* FIXED SERVER LINK */
function openServerLink(){
    window.open("https://www.roblox.et/games/920587237/Adopt-Me?privateServerLinkCode=32102348504223285674649197659220", "_blank");
}

/* DISCOVER */
function openDiscover(){
    document.getElementById("discoverModal").style.display = "flex";
}

function closeDiscover(){
    document.getElementById("discoverModal").style.display = "none";
}
</script>

</body>DO
