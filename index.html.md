<!DOCTYPE html>  
<html lang="sq">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>PD Vlorë</title>  
  
<style>  
body { font-family: Arial; margin:0; background:#f4f6f9; }  
header { background:#0033a0; color:white; padding:15px; text-align:center; }  
.section { padding:30px; text-align:center; }  
.card { background:white; padding:15px; margin:10px; display:inline-block; width:250px; }  
button { padding:10px; margin:5px; }  
input, textarea { padding:10px; width:80%; margin:5px; }  
#adminPanel { display:none; }  
</style>  
</head>  
  
<body>  
  
<header>  
<h1>Partia Demokratike</h1>  
<p>Dega Vlorë (PD Vlorë)</p>  
</header>  
  
<div class="section">  
<h2>Lajmet</h2>  
<div id="posts">Duke u ngarkuar...</div>  
</div>  
  
<div class="section">  
<h2>Admin Login</h2>  
<input type="email" id="email" placeholder="Email"><br>  
<input type="password" id="password" placeholder="Password"><br>  
<button onclick="login()">Login</button>  
</div>  
  
<div class="section" id="adminPanel">  
<h2>Posto Lajm</h2>  
<input type="text" id="title" placeholder="Titulli"><br>  
<textarea id="content" placeholder="Përmbajtja"></textarea><br>  
<button onclick="addPost()">Posto</button>  
</div>  
  
<!-- Firebase SDK -->  
<script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-app-compat.js"></script>  
<script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-auth-compat.js"></script>  
<script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-firestore-compat.js"></script>  
  
<script>  
// 🔴 YOU WILL REPLACE THIS PART  
const firebaseConfig = {  
  apiKey: "PASTE_HERE",  
  authDomain: "PASTE_HERE",  
  projectId: "PASTE_HERE"  
};  
  
firebase.initializeApp(firebaseConfig);  
const db = firebase.firestore();  
  
// LOAD POSTS  
async function loadPosts() {  
  const snapshot = await db.collection("posts").orderBy("date","desc").get();  
  const postsDiv = document.getElementById("posts");  
  postsDiv.innerHTML = "";  
  
  snapshot.forEach(doc => {  
    const data = doc.data();  
    postsDiv.innerHTML += `  
      <div class="card">  
        <h3>${data.title}</h3>  
        <p>${data.content}</p>  
      </div>  
    `;  
  });  
}  
loadPosts();  
  
// LOGIN  
function login() {  
  const email = emailInput.value;  
  const password = passwordInput.value;  
  
  firebase.auth().signInWithEmailAndPassword(email, password)  
    .then(() => {  
      adminPanel.style.display = "block";  
      alert("Logged in!");  
    })  
    .catch(() => alert("Login error"));  
}  
  
// ADD POST  
function addPost() {  
  const title = titleInput.value;  
  const content = contentInput.value;  
  
  db.collection("posts").add({  
    title,  
    content,  
    date: new Date()  
  }).then(() => {  
    loadPosts();  
    alert("Post added!");  
  });  
}  
</script>  
  
</body>  
</html>  
