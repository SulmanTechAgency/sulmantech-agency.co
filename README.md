# SulmanTech-Agency
"Premium digital agency website for Sulman Tech Agency – HTML, CSS, JS"
/* ===== Base ===== */
body {
  margin:0;
  font-family: Arial, sans-serif;
  background:#0d1b2a;
  color:white;
  overflow-x:hidden;
}
a { text-decoration:none; }
button { cursor:pointer; }

/* ===== Navbar ===== */
.navbar {
  display:flex;
  justify-content:center;
  gap:20px;
  padding:15px;
  background: rgba(0,0,0,0.4);
  position: sticky;
  top:0;
  z-index:10;
}
.navbar a {
  color:#4cc9f0;
  font-weight:bold;
  transition:0.3s;
}
.navbar a:hover { color:#fff; }

/* ===== Hero ===== */
.hero {
  position:relative;
  text-align:center;
  padding:150px 20px;
  overflow:hidden;
}
.hero::before {
  content:"";
  position:absolute;
  top:-50%; left:-50%;
  width:200%; height:200%;
  background: linear-gradient(-45deg,#0d1b2a,#1b263b,#3a0ca3,#4361ee);
  background-size: 400% 400%;
  animation: gradientMove 12s ease infinite;
  z-index:0;
}
@keyframes gradientMove {
  0% { background-position:0% 50%; }
  50% { background-position:100% 50%; }
  100% { background-position:0% 50%; }
}
.hero-content { position:relative; z-index:1; }
.hero h1 { font-size:48px; color:#4cc9f0; margin-bottom:20px; }
.hero p { font-size:20px; opacity:0.9; margin-bottom:30px; }
.btn {
  display:inline-block;
  padding:14px 30px;
  margin:10px;
  background:#4cc9f0;
  color:#0d1b2a;
  font-weight:bold;
  border-radius:8px;
  transition:0.3s;
}
.btn:hover {
  background:#fff;
  color:#000;
  transform:scale(1.05);
}

/* ===== Services Cards ===== */
.card-container {
  display:flex;
  flex-wrap:wrap;
  justify-content:center;
  gap:20px;
  padding:50px 20px;
}
.card {
  background: rgba(27,38,59,0.8);
  padding:30px;
  border-radius:15px;
  width:250px;
  text-align:center;
  transition:0.3s;
}
.card:hover { transform: scale(1.05); }
.card h3 { color:#4cc9f0; margin-bottom:10px; }
.card p { opacity:0.9; margin-bottom:15px; }
.card .btn { display:block; }

/* ===== AI Chat Placeholder ===== */
.chat-box {
  position:fixed;
  bottom:20px;
  right:20px;
  background: rgba(27,38,59,0.95);
  width:300px;
  max-height:400px;
  border-radius:10px;
  overflow:hidden;
  display:flex;
  flex-direction:column;
  z-index:50;
}
.chat-header { background:#4cc9f0; padding:10px; font-weight:bold; color:#0d1b2a; }
.chat-messages { flex:1; padding:10px; overflow-y:auto; }
.chat-input { display:flex; border-top:1px solid #333; }
.chat-input input {
  flex:1;
  padding:8px;
  border:none;
  border-radius:0;
}
.chat-input button { padding:8px; background:#4cc9f0; border:none; color:#0d1b2a; font-weight:bold; }

/* ===== My Account ===== */
.account-box {
  max-width:400px;
  margin:50px auto;
  background: rgba(27,38,59,0.8);
  padding:30px;
  border-radius:15px;
  text-align:center;
}
.account-box input {
  padding:10px;
  margin:10px 0;
  width:90%;
  border-radius:5px;
  border:none;
}
.account-box button { width:45%; margin:5px; }
.hidden { display:none; }

/* ===== Responsive ===== */
@media(max-width:768px) {
  .card-container { flex-direction:column; align-items:center; }
}

