<!DOCTYPE html>
<html lang="am">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>የህግ ባለሞያ ለኢትዮጵያ</title>

<style>
body{
margin:0;
font-family:Arial;
background:#f5f7fa;
}

header{
background:#0b2e4a;
color:white;
padding:20px;
text-align:center;
}

.profile{
width:120px;
height:120px;
border-radius:50%;
border:3px solid white;
margin-top:10px;
}

nav{
background:#144d73;
padding:10px;
text-align:center;
position:sticky;
top:0;
}

nav a{
color:white;
margin:10px;
text-decoration:none;
font-weight:bold;
}

section{
background:white;
margin:15px;
padding:20px;
border-radius:10px;
box-shadow:0 0 10px rgba(0,0,0,0.1);
}

h2{
color:#0b2e4a;
}

button{
padding:10px 15px;
background:#144d73;
color:white;
border:none;
border-radius:5px;
cursor:pointer;
}

input, select{
padding:10px;
width:90%;
margin-top:10px;
}

.lang{
position:absolute;
top:10px;
right:10px;
}
</style>
</head>

<body>

<header>
<div class="lang">
<select onchange="changeLang(this.value)">
<option value="am">አማርኛ</option>
<option value="en">English</option>
</select>
</div>

<h1 id="title">የህግ ባለሞያ ለኢትዮጵያ</h1>

<img src="https://via.placeholder.com/120" class="profile">

<p id="subtitle">Legal Knowledge • Training • Consultation</p>
</header>

<nav>
<a href="#laws">ህጎች</a>
<a href="#search">ፍለጋ</a>
<a href="#training">ስልጠና</a>
<a href="#consult">ማማከር</a>
<a href="#cassation">ሰበር</a>
<a href="#payment">ክፍያ</a>
</nav>

<!-- LAWS -->
<section id="laws">
<h2>📚 የኢትዮጵያ ህጎች</h2>

<ul>
<li>የወንጀል ህግ</li>
<li>የንግድ ህግ</li>
<li>የውል ህግ</li>
<li>የሲቪል ህግ</li>
</ul>

<p>PDF, Video, Audio እና Image ማጋራት ይቻላል (Backend ሲጨመር)</p>
</section>

<!-- SEARCH -->
<section id="search">
<h2>🔍 የሰበር ውሳኔ ፍለጋ</h2>

<input type="text" placeholder="ፋይል ቁጥር ወይም ዘርፍ">
<br><br>
<button onclick="alert('Search feature backend ይፈልጋል')">ፈልግ</button>
</section>

<!-- TRAINING -->
<section id="training">
<h2>🎓 6 ወር የህግ ስልጠና</h2>
<p>በኦንላይን የህግ ትምህርት (Civil, Criminal, Commercial)</p>
<button>መመዝገብ</button>
</section>

<!-- CONSULTATION -->
<section id="consult">
<h2>⚖️ የህግ ማማከር</h2>
<input type="text" placeholder="ስም">
<input type="text" placeholder="ጥያቄ">
<button>ላክ</button>
</section>

<!-- CASSATION -->
<section id="cassation">
<h2>📄 የሰበር ውሳኔዎች</h2>
<p>500 ETB በመክፈል ሙሉ ውሳኔ ማግኘት</p>
<button>ፈልግ</button>
</section>

<!-- PAYMENT -->
<section id="payment">
<h2>💳 ክፍያ አማራጮች</h2>
<ul>
<li>CBE (Commercial Bank of Ethiopia)</li>
<li>CBE Birr</li>
<li>Telebirr</li>
</ul>
</section>

<!-- SOCIAL -->
<section>
<h2>📢 ማህበራዊ ገፆች</h2>
<p>Facebook | Telegram | YouTube</p>
</section>

<script>
// Language switch (simple demo)
function changeLang(lang){
if(lang=="en"){
document.getElementById("title").innerText="Legal Professional for Ethiopia";
document.getElementById("subtitle").innerText="Law • Training • Consultation";
}else{
document.getElementById("title").innerText="የህግ ባለሞያ ለኢትዮጵያ";
document.getElementById("subtitle").innerText="Legal Knowledge • Training • Consultation";
}
}
</script>

</body>
</html>
index.html<!DOCTYPE html>
<html lang="am">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>የህግ ባለሞያ ለኢትዮጵያ</title>

<style>
body{
font-family:Arial,sans-serif;
margin:0;
background:#f4f4f4;
}

header{
background:#003366;
color:white;
padding:20px;
text-align:center;
}

nav{
background:#0055aa;
padding:10px;
text-align:center;
}

nav a{
color:white;
margin:10px;
text-decoration:none;
font-weight:bold;
}

section{
background:white;
margin:20px;
padding:20px;
border-radius:10px;
box-shadow:0 0 5px gray;
}

footer{
background:#003366;
color:white;
text-align:center;
padding:15px;
}

.btn{
background:#0055aa;
color:white;
padding:10px 20px;
border:none;
border-radius:5px;
cursor:pointer;
}

input, textarea, select{
width:100%;
padding:10px;
margin:10px 0;
}
</style>
</head>

<body>

<header>
<h1>የህግ ባለሞያ ለኢትዮጵያ</h1>
<p>Ethiopian Legal Education & Consultation Platform</p>
</header>

<nav>
<a href="#laws">ህጎች</a>
<a href="#training">ስልጠና</a>
<a href="#cassation">ሰበር ውሳኔ</a>
<a href="#consultation">ማማከር</a>
<a href="#payment">ክፍያ</a>
<a href="#contact">አግኙን</a>
</nav>

<section>
<h2>Admin Login</h2>
<form>
<input type="text" placeholder="Username">
<input type="password" placeholder="Password">
<button class="btn">Login</button>
</form>
<p>Admin: Yonatan Dawit Mengistu</p>
</section>

<section id="laws">
<h2>የኢትዮጵያ ህጎች</h2>

<h3>Documents</h3>
<input type="file">

<h3>Videos</h3>
<input type="file">

<h3>Audio Files</h3>
<input type="file">
</section>

<section id="consultation">
<h2>የህግ ማማከር አገልግሎት</h2>

<form>
<input type="text" placeholder="ሙሉ ስም">
<input type="email" placeholder="ኢሜይል">
<textarea placeholder="ጥያቄዎን ያስገቡ"></textarea>
<button class="btn">ላክ</button>
</form>
</section>

<section id="training">
<h2>6 ወር የህግ ስልጠና</h2>

<ul>
<li>የህገ-መንግስት ህግ</li>
<li>የፍትሐብሔር ህግ</li>
<li>የወንጀል ህግ</li>
<li>የስራ ህግ</li>
<li>የንግድ ህግ</li>
<li>የማስረጃ ህግ</li>
</ul>

<button class="btn">Register</button>
</section>

<section id="cassation">
<h2>የኢፌድሪ ሰበር ሰሚ ችሎት ውሳኔዎች</h2>

<input type="text" placeholder="የፋይል ቁጥር ወይም ርዕስ">

<select>
<option>የወንጀል ህግ</option>
<option>የፍትሐብሔር ህግ</option>
<option>የንግድ ህግ</option>
<option>የቤተሰብ ህግ</option>
</select>

<p>የውሳኔ ማግኛ ክፍያ: 500 ETB</p>

<button class="btn">Search</button>
</section>

<section id="payment">
<h2>የክፍያ አማራጮች</h2>

<ul>
<li>Commercial Bank of Ethiopia (CBE)</li>
<li>CBE Birr</li>
<li>TeleBirr</li>
</ul>
</section>

<section id="contact">
<h2>Social Media</h2>

<p>Facebook</p>
<p>YouTube</p>
<p>Telegram</p>
<p>TikTok</p>
<p>LinkedIn</p>
</section>

<footer>
<p>© 2026 የህግ ባለሞያ ለኢትዮጵያ</p>
<p>Admin: Yonatan Dawit Mengistu</p>
</footer>

</body>
</html>
