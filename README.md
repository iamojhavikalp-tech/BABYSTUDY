<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BabyStudy - Study Together</title>

    <link rel="stylesheet" href="style.css">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

    <script defer src="app.js"></script>
</head>

<body>

<div class="background"></div>

<!-- Navbar -->
<nav class="navbar">
    <div class="logo">
        📚 <span>BabyStudy</span>
    </div>

    <div class="nav-links">
        <a href="#features">Features</a>
        <a href="#about">About</a>
        <button id="loginBtn">Login</button>
    </div>
</nav>

<!-- Hero -->
<section class="hero">

    <div class="hero-left">

        <h1>
            Study Smarter.<br>
            Compete Better.<br>
            Grow Together.
        </h1>

        <p>
            BabyStudy helps students stay focused with study timers,
            leaderboards, groups, analytics, and daily goals.
        </p>

        <button id="startBtn">
            Get Started
        </button>

    </div>

    <div class="hero-right">

        <div class="hero-card">

            <h2>Today's Progress</h2>

            <div class="progress-circle">
                65%
            </div>

            <p>Goal: 15 Hours</p>

        </div>

    </div>

</section>

<!-- Features -->

<section id="features" class="features">

<h2>Features</h2>

<div class="feature-grid">

<div class="feature-card">
⏱️
<h3>Study Timer</h3>
<p>Stopwatch & Pomodoro</p>
</div>

<div class="feature-card">
🏆
<h3>Leaderboards</h3>
<p>Daily, Weekly & Monthly</p>
</div>

<div class="feature-card">
👥
<h3>Groups</h3>
<p>Create private study groups</p>
</div>

<div class="feature-card">
📈
<h3>Analytics</h3>
<p>Charts & Heatmaps</p>
</div>

<div class="feature-card">
🎯
<h3>Daily Goals</h3>
<p>Track your progress</p>
</div>

<div class="feature-card">
🔥
<h3>Study Streak</h3>
<p>Stay consistent every day</p>
</div>

</div>

</section>

<!-- Login Modal -->

<div class="modal" id="loginModal">

<div class="login-box">

<h2>Welcome Back 👋</h2>

<input
type="email"
id="email"
placeholder="Email">

<input
type="password"
id="password"
placeholder="Password">

<button id="emailLogin">
Login
</button>

<button id="googleLogin">
Continue with Google
</button>

<p>
Don't have an account?
<a href="#" id="signupLink">Create Account</a>
</p>

</div>

</div>

<!-- Signup Modal -->

<div class="modal" id="signupModal">

<div class="login-box">

<h2>Create Account</h2>

<input
type="text"
id="name"
placeholder="Full Name">

<input
type="email"
id="signupEmail"
placeholder="Email">

<input
type="password"
id="signupPassword"
placeholder="Password">

<button id="signupBtn">
Create Account
</button>

<p>
Already have an account?
<a href="#" id="loginLink">
Login
</a>
</p>

</div>

</div>

<!-- Footer -->

<footer>

<h3>BabyStudy</h3>

<p>
Built for students who want consistency,
focus and growth.
</p>

<p>

© 2026 BabyStudy Project

</p>

</footer>

</body>
</html>
/* ===========================
   BABY STUDY PROJECT v1.0
   style.css (Part 1B-1)
=========================== */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

:root{
    --primary:#38BDF8;
    --secondary:#8B5CF6;
    --dark:#020617;
    --card:rgba(15,23,42,.75);
    --text:#ffffff;
    --gray:#94A3B8;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:'Poppins',sans-serif;
    background:var(--dark);
    color:var(--text);
    overflow-x:hidden;
}

/* Animated Background */

.background{
    position:fixed;
    inset:0;
    z-index:-2;
    background:
    radial-gradient(circle at top left,#2563eb 0%,transparent 35%),
    radial-gradient(circle at bottom right,#8b5cf6 0%,transparent 35%),
    radial-gradient(circle at center,#0ea5e9 0%,transparent 45%),
    #020617;
}

.background::after{
    content:"";
    position:absolute;
    inset:0;
    background:linear-gradient(
        120deg,
        rgba(255,255,255,.04),
        transparent,
        rgba(255,255,255,.04)
    );
    animation:bgMove 12s linear infinite;
}

@keyframes bgMove{

0%{
transform:translateX(-100%);
}

100%{
transform:translateX(100%);
}

}

/* Navbar */

.navbar{

position:fixed;

top:0;

left:0;

width:100%;

display:flex;

justify-content:space-between;

align-items:center;

padding:18px 8%;

background:rgba(2,6,23,.65);

backdrop-filter:blur(20px);

border-bottom:1px solid rgba(255,255,255,.08);

z-index:999;

}

.logo{

font-size:28px;

font-weight:700;

display:flex;

align-items:center;

gap:10px;

}

.logo span{

color:var(--primary);

}

.nav-links{

display:flex;

align-items:center;

gap:25px;

}

.nav-links a{

text-decoration:none;

color:white;

font-weight:500;

transition:.3s;

}

.nav-links a:hover{

color:var(--primary);

}

.nav-links button{

background:var(--primary);

color:white;

border:none;

padding:12px 24px;

border-radius:12px;

cursor:pointer;

font-weight:600;

transition:.3s;

}

.nav-links button:hover{

transform:translateY(-2px);

box-shadow:0 0 20px rgba(56,189,248,.4);

}

/* Hero */

.hero{

min-height:100vh;

display:flex;

justify-content:space-between;

align-items:center;

padding:120px 8%;

gap:70px;

flex-wrap:wrap;

}

.hero-left{

flex:1;

min-width:320px;

}

.hero-left h1{

font-size:64px;

line-height:1.15;

margin-bottom:25px;

}

.hero-left p{

font-size:19px;

color:var(--gray);

line-height:1.8;

max-width:650px;

margin-bottom:35px;

}

.hero-left button{

padding:18px 38px;

font-size:18px;

border:none;

border-radius:16px;

background:linear-gradient(
135deg,
var(--primary),
var(--secondary)
);

color:white;

cursor:pointer;

font-weight:700;

transition:.35s;

}

.hero-left button:hover{

transform:translateY(-4px);

box-shadow:0 20px 40px rgba(56,189,248,.3);

}

/* Hero Card */

.hero-right{

flex:1;

display:flex;

justify-content:center;

align-items:center;

}

.hero-card{

width:360px;

padding:35px;

background:var(--card);

border-radius:28px;

backdrop-filter:blur(20px);

border:1px solid rgba(255,255,255,.08);

text-align:center;

box-shadow:0 25px 45px rgba(0,0,0,.35);

}

.hero-card h2{

margin-bottom:25px;

}

.progress-circle{

width:180px;

height:180px;

margin:auto;

border-radius:50%;

display:flex;

justify-content:center;

align-items:center;

font-size:38px;

font-weight:700;

background:conic-gradient(
var(--primary) 65%,
rgba(255,255,255,.08) 0
);

margin-bottom:20px;

}
/* ===========================
   Features Section
=========================== */

.features{
    padding:100px 8%;
}

.features h2{
    text-align:center;
    font-size:42px;
    margin-bottom:50px;
}

.feature-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.feature-card{
    background:var(--card);
    backdrop-filter:blur(20px);
    border:1px solid rgba(255,255,255,.08);
    border-radius:22px;
    padding:35px;
    text-align:center;
    transition:.35s;
    cursor:pointer;
}

.feature-card:hover{
    transform:translateY(-10px);
    border-color:var(--primary);
    box-shadow:0 20px 40px rgba(56,189,248,.25);
}

.feature-card h3{
    margin:18px 0 12px;
    font-size:24px;
}

.feature-card p{
    color:var(--gray);
    line-height:1.7;
}

/* ===========================
   Login & Signup Modal
=========================== */

.modal{
    position:fixed;
    inset:0;
    display:none;
    justify-content:center;
    align-items:center;
    background:rgba(0,0,0,.65);
    backdrop-filter:blur(10px);
    z-index:1000;
}

.login-box{
    width:95%;
    max-width:430px;
    background:var(--card);
    backdrop-filter:blur(20px);
    border-radius:24px;
    border:1px solid rgba(255,255,255,.08);
    padding:35px;
}

.login-box h2{
    text-align:center;
    margin-bottom:25px;
}

.login-box input{
    width:100%;
    margin:12px 0;
    padding:15px;
    border:none;
    border-radius:14px;
    background:#0f172a;
    color:white;
    font-size:16px;
}

.login-box input:focus{
    outline:2px solid var(--primary);
}

.login-box button{
    width:100%;
    margin-top:15px;
    padding:15px;
    border:none;
    border-radius:14px;
    background:linear-gradient(135deg,var(--primary),var(--secondary));
    color:white;
    font-size:17px;
    font-weight:600;
    cursor:pointer;
    transition:.3s;
}

.login-box button:hover{
    transform:translateY(-3px);
}

.login-box p{
    text-align:center;
    margin-top:18px;
}

.login-box a{
    color:var(--primary);
    text-decoration:none;
}

/* ===========================
   Footer
=========================== */

footer{
    padding:50px 8%;
    text-align:center;
    color:var(--gray);
}

footer h3{
    color:white;
    margin-bottom:15px;
}

footer p{
    margin:8px 0;
}

/* ===========================
   Scrollbar
=========================== */

::-webkit-scrollbar{
    width:10px;
}

::-webkit-scrollbar-track{
    background:#020617;
}

::-webkit-scrollbar-thumb{
    background:var(--primary);
    border-radius:20px;
}

/* ===========================
   Animations
=========================== */

.hero,
.features,
footer{
    animation:fadeUp .8s ease;
}

@keyframes fadeUp{

from{
    opacity:0;
    transform:translateY(40px);
}

to{
    opacity:1;
    transform:translateY(0);
}

}

/* ===========================
   Responsive
=========================== */

@media(max-width:900px){

.hero{
    flex-direction:column;
    text-align:center;
}

.hero-left h1{
    font-size:42px;
}

.hero-card{
    width:100%;
    max-width:360px;
}

.navbar{
    padding:16px 5%;
}

.nav-links{
    gap:15px;
}

}

@media(max-width:600px){

.logo{
    font-size:22px;
}

.nav-links a{
    display:none;
}

.hero{
    padding:100px 6%;
}

.hero-left h1{
    font-size:34px;
}

.hero-left p{
    font-size:16px;
}

.features{
    padding:70px 6%;
}

.features h2{
    font-size:32px;
}

.login-box{
    padding:25px;
}

}
/* =====================================
   BABY STUDY PROJECT
   app.js (Part 1C-1)
===================================== */

// --------------------------
// Elements
// --------------------------

const loginModal = document.getElementById("loginModal");
const signupModal = document.getElementById("signupModal");

const loginBtn = document.getElementById("loginBtn");
const startBtn = document.getElementById("startBtn");

const signupLink = document.getElementById("signupLink");
const loginLink = document.getElementById("loginLink");

// Login Form
const email = document.getElementById("email");
const password = document.getElementById("password");

// Signup Form
const nameInput = document.getElementById("name");
const signupEmail = document.getElementById("signupEmail");
const signupPassword = document.getElementById("signupPassword");

// Buttons
const emailLogin = document.getElementById("emailLogin");
const googleLogin = document.getElementById("googleLogin");
const signupBtn = document.getElementById("signupBtn");

// --------------------------
// Modal Controls
// --------------------------

function openLogin() {
    loginModal.style.display = "flex";
    signupModal.style.display = "none";
}

function openSignup() {
    signupModal.style.display = "flex";
    loginModal.style.display = "none";
}

function closeModals() {
    loginModal.style.display = "none";
    signupModal.style.display = "none";
}

// --------------------------
// Event Listeners
// --------------------------

loginBtn.addEventListener("click", openLogin);

startBtn.addEventListener("click", openLogin);

signupLink.addEventListener("click", (e) => {
    e.preventDefault();
    openSignup();
});

loginLink.addEventListener("click", (e) => {
    e.preventDefault();
    openLogin();
});

// Close modal when clicking outside

window.addEventListener("click", (event) => {

    if (event.target === loginModal) {
        closeModals();
    }

    if (event.target === signupModal) {
        closeModals();
    }

});

// ESC Key

document.addEventListener("keydown", (event) => {

    if (event.key === "Escape") {
        closeModals();
    }

});

// --------------------------
// Validation
// --------------------------

function validateEmail(emailValue) {

    const pattern =
        /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

    return pattern.test(emailValue);

}

function validatePassword(passwordValue) {

    return passwordValue.length >= 6;

}

function showError(message) {

    alert(message);

}

function showSuccess(message) {

    alert(message);

}

// --------------------------
// Login Validation
// --------------------------

emailLogin.addEventListener("click", () => {

    const userEmail = email.value.trim();
    const userPassword = password.value;

    if (!validateEmail(userEmail)) {

        return showError("Please enter a valid email.");

    }

    if (!validatePassword(userPassword)) {

        return showError(
            "Password must be at least 6 characters."
        );

    }

    console.log("Login validation successful.");

    // Firebase login comes in Part 1C-2

});

// --------------------------
// Signup Validation
// --------------------------

signupBtn.addEventListener("click", () => {

    const fullName = nameInput.value.trim();

    const userEmail = signupEmail.value.trim();

    const userPassword = signupPassword.value;

    if (fullName.length < 3) {

        return showError(
            "Name must contain at least 3 characters."
        );

    }

    if (!validateEmail(userEmail)) {

        return showError("Invalid email.");

    }

    if (!validatePassword(userPassword)) {

        return showError(
            "Password must contain at least 6 characters."
        );

    }

    console.log("Signup validation successful.");

    // Firebase signup comes in Part 1C-2

});

// --------------------------
// Google Login
// --------------------------

googleLogin.addEventListener("click", () => {

    console.log("Google Login Clicked");

    // Firebase Google Login
    // Added in Part 1C-2

});
/* ======================================
   BABY STUDY PROJECT
   Privacy First Google Login
====================================== */

googleLogin.addEventListener("click", async () => {

    try {

        const provider = new firebase.auth.GoogleAuthProvider();

        const result = await firebase.auth().signInWithPopup(provider);

        const user = result.user;

        // Ask for BabyStudy username
        let username = prompt("Choose your BabyStudy username:");

        if (!username || username.trim().length < 3) {
            alert("Username must be at least 3 characters.");
            return;
        }

        username = username.trim();

        // Generate BabyStudy ID
        const babyStudyID =
            "BSP-" +
            Math.random().toString(36).substring(2,8).toUpperCase();

        // Only save safe information
        const profile = {
            uid: user.uid,
            username: username,
            babyStudyID: babyStudyID,
            level: 1,
            xp: 0,
            streak: 0,
            studyHours: 0,
            dailyGoal: 10,
            role: "member",
            createdAt: new Date().toISOString()
        };

        localStorage.setItem(
            "babyStudyUser",
            JSON.stringify(profile)
        );

        window.location.href = "dashboard.html";

    } catch (error) {

        alert(error.message);

    }

});
function createMemberCard(member){

    return `
        <div class="member-card">

            <div class="avatar">
                ${member.username.charAt(0).toUpperCase()}
            </div>

            <div class="member-info">

                <h3>${member.username}</h3>

                <p>ID : ${member.babyStudyID}</p>

                <p>🔥 ${member.streak} Day Streak</p>

                <p>⏱ ${member.studyHours.toFixed(1)} Hours</p>

                <p>⭐ Level ${member.level}</p>

            </div>

        </div>
    `;

}
/* =====================================
   BABY STUDY PROJECT
   app.js (Part 1C-2)
   Firebase Authentication
===================================== */

// Firebase Services
const auth = firebase.auth();
const db = firebase.firestore();

// Google Provider
const provider = new firebase.auth.GoogleAuthProvider();

// -------------------------
// Google Login
// -------------------------

googleLogin.addEventListener("click", async () => {

    try {

        const result = await auth.signInWithPopup(provider);

        const user = result.user;

        // Check if profile already exists
        const doc = await db.collection("users")
            .doc(user.uid)
            .get();

        if (!doc.exists) {

            let username = "";

            while (true) {

                username = prompt(
                    "Choose a unique BabyStudy username:"
                );

                if (!username) continue;

                username = username.trim();

                if (username.length >= 3) break;

                alert("Username must be at least 3 characters.");

            }

            const babyID =
                "BSP-" +
                Math.random()
                .toString(36)
                .substring(2,8)
                .toUpperCase();

            await db.collection("users")
                .doc(user.uid)
                .set({

                    username: username,

                    babyID: babyID,

                    role: "member",

                    level: 1,

                    xp: 0,

                    streak: 0,

                    totalHours: 0,

                    todayHours: 0,

                    weeklyHours: 0,

                    monthlyHours: 0,

                    dailyGoal: 10,

                    groups: [],

                    achievements: [],

                    createdAt:
                        firebase.firestore.FieldValue.serverTimestamp()

                });

        }

        window.location.href = "dashboard.html";

    }

    catch(error){

        console.error(error);

        alert(error.message);

    }

});

// -------------------------
// Auto Login
// -------------------------

auth.onAuthStateChanged((user)=>{

    if(user){

        console.log("Signed In");

    }

});
/* =====================================
   BABY STUDY PROJECT
   app.js (Part 1C-3)
   Session & Dashboard Protection
===================================== */

// Keep user logged in
auth.setPersistence(firebase.auth.Auth.Persistence.LOCAL)
.then(() => {
    console.log("Session persistence enabled.");
})
.catch(console.error);

// Check authentication state
auth.onAuthStateChanged(async (user) => {

    // User not logged in
    if (!user) {

        // Protect dashboard pages
        if (
            window.location.pathname.includes("dashboard.html")
        ) {
            window.location.href = "index.html";
        }

        return;
    }

    // Load profile
    try {

        const doc = await db.collection("users")
            .doc(user.uid)
            .get();

        if (!doc.exists) return;

        const profile = doc.data();

        // Update dashboard UI if elements exist
        const usernameEl = document.getElementById("username");
        const babyIdEl = document.getElementById("babyID");
        const levelEl = document.getElementById("level");

        if (usernameEl)
            usernameEl.textContent = profile.username;

        if (babyIdEl)
            babyIdEl.textContent = profile.babyID;

        if (levelEl)
            levelEl.textContent = "Level " + profile.level;

    } catch (err) {
        console.error(err);
    }

});

// Logout
function logout() {

    auth.signOut()
        .then(() => {

            window.location.href = "index.html";

        })
        .catch(console.error);

}

// Logout Button
const logoutBtn = document.getElementById("logoutBtn");

if (logoutBtn) {

    logoutBtn.addEventListener("click", logout);

}

// Loading Screen
window.addEventListener("load", () => {

    const loader = document.getElementById("loader");

    if (loader) {

        loader.style.opacity = "0";

        setTimeout(() => {

            loader.style.display = "none";

        }, 400);

    }

});
<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>BabyStudy Dashboard</title>

<link rel="stylesheet" href="dashboard.css">

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<script defer src="firebase.js"></script>
<script defer src="dashboard.js"></script>
<script defer src="timer.js"></script>
<script defer src="subjects.js"></script>
<script defer src="goals.js"></script>

</head>

<body>

<div id="loader">
    <h2>Loading BabyStudy...</h2>
</div>

<!-- Sidebar -->

<aside class="sidebar">

    <div class="logo">
        📚 BabyStudy
    </div>

    <ul>

        <li class="active">🏠 Dashboard</li>

        <li>⏱ Timer</li>

        <li>📚 Subjects</li>

        <li>👥 Groups</li>

        <li>🏆 Leaderboard</li>

        <li>📈 Analytics</li>

        <li>⚙ Settings</li>

    </ul>

</aside>

<!-- Main -->

<main class="main">

<header class="topbar">

<div>

<h2 id="username">
Loading...
</h2>

<p id="babyID">
BSP-XXXXXX
</p>

</div>

<div class="profile">

<span id="level">
Level 1
</span>

<button id="logoutBtn">

Logout

</button>

</div>

</header>

<!-- Stats -->

<section class="stats-grid">

<div class="card">

<h3>Today's Study</h3>

<h1 id="todayHours">

0.0h

</h1>

</div>

<div class="card">

<h3>Daily Goal</h3>

<h1 id="goalHours">

10h

</h1>

</div>

<div class="card">

<h3>Current Streak</h3>

<h1 id="streak">

0 🔥

</h1>

</div>

<div class="card">

<h3>XP</h3>

<h1 id="xp">

0

</h1>

</div>

</section>

<!-- Timer -->

<section class="timer-card">

<h2>Study Timer</h2>

<select id="subjectSelect">

<option>Physics ⚛️</option>

<option>Chemistry 🧪</option>

<option>Mathematics 📐</option>

<option>Revision 📖</option>

</select>

<div id="timer">

00:00:00

</div>

<div class="buttons">

<button id="startTimer">

▶ Start

</button>

<button id="pauseTimer">

⏸ Pause

</button>

<button id="resetTimer">

🔄 Reset

</button>

</div>

</section>

<!-- Daily Goal -->

<section class="goal-card">

<h2>

Daily Goal

</h2>

<input
type="number"
id="dailyGoalInput"
min="1"
max="24"
value="10">

<button id="saveGoal">

Save Goal

</button>

<div class="progress-bar">

<div id="progressFill">

</div>

</div>

<p id="goalPercent">

0%

</p>

</section>
<!-- Subjects Section -->

<section class="subject-card">

<h2>📚 My Subjects</h2>

<div class="subject-input">

<input 
type="text"
id="newSubject"
placeholder="Add new subject">

<button id="addSubject">
Add
</button>

</div>


<div id="subjectList">

<div class="subject-item">
<span>⚛️ Physics</span>
<span>0h</span>
</div>

<div class="subject-item">
<span>🧪 Chemistry</span>
<span>0h</span>
</div>

<div class="subject-item">
<span>📐 Mathematics</span>
<span>0h</span>
</div>

</div>

</section>


<!-- Tasks -->

<section class="task-card">

<h2>✅ Daily Tasks</h2>

<div class="task-input">

<input
type="text"
id="taskInput"
placeholder="Enter task">

<button id="addTask">
+
</button>

</div>


<div id="taskList">

</div>

</section>


<!-- Group Preview -->

<section class="group-card">

<h2>👥 My Study Groups</h2>


<div class="group-box">

<h3>
No Group Joined
</h3>

<p>
Create or join a study group to compete with friends.
</p>


<button id="createGroup">

Create Group

</button>


<button id="joinGroup">

Join Group

</button>


</div>


</section>


<!-- Leaderboard Preview -->

<section class="leaderboard-card">

<h2>
🏆 Daily Ranking
</h2>


<div class="leader-row top">

<span>
🥇 QuantumJEE
</span>

<span>
15.2h
</span>

</div>


<div class="leader-row">

<span>
🥈 PhysicsMaster
</span>

<span>
12.8h
</span>

</div>


<div class="leader-row">

<span>
🥉 MathWizard
</span>

<span>
10.5h
</span>

</div>


<button id="openLeaderboard">

View Full Leaderboard

</button>


</section>



<!-- Analytics Preview -->


<section class="analytics-card">


<h2>
📊 Analytics
</h2>


<div class="analytics-grid">


<div>
<!-- Challenges -->

<section class="challenge-card">

<h2>🔥 Active Challenges</h2>

<div class="challenge-box">

<h3>
10 Days Focus Challenge
</h3>

<p>
Complete daily targets and climb the leaderboard.
</p>

<div class="challenge-progress">

<div id="challengeFill"></div>

</div>

<p>
Day 3 / 10
</p>

<button id="joinChallenge">
Join Challenge
</button>

</div>

</section>



<!-- Notifications -->

<section class="notification-card">

<h2>
🔔 Notifications
</h2>


<div id="notificationList">

<div class="notification">

🎯 Daily goal reminder:
Complete your target today.

</div>


<div class="notification">

🏆 New ranking update available.

</div>


</div>

</section>



<!-- Settings -->

<section class="settings-card">

<h2>
⚙ Settings
</h2>


<div class="setting-item">

<span>
🌙 Dark Mode
</span>

<input type="checkbox" id="darkMode">

</div>


<div class="setting-item">

<span>
🔔 Notifications
</span>

<input type="checkbox" checked>

</div>


<div class="setting-item">

<span>
🔒 Private Profile
</span>

<input type="checkbox" checked>

</div>


</section>



<!-- Mobile Navigation -->

<nav class="mobile-nav">


<button>
🏠
<br>
Home
</button>


<button>
⏱
<br>
Timer
</button>


<button>
👥
<br>
Groups
</button>


<button>
🏆
<br>
Rank
</button>


<button>
👤
<br>
Profile
</button>


</nav>



</main>


<!-- Scripts -->

<script src="dashboard.js"></script>
<script src="timer.js"></script>
<script src="subjects.js"></script>
<script src="goals.js"></script>


</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   dashboard.css
   Module 2B-1
================================== */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

:root{

    --primary:#38bdf8;
    --secondary:#8b5cf6;
    --bg:#020617;
    --card:rgba(15,23,42,.75);
    --text:#ffffff;
    --muted:#94a3b8;

}


body{

    font-family:'Poppins',sans-serif;

    background:
    radial-gradient(circle at top left,#2563eb,transparent 35%),
    radial-gradient(circle at bottom right,#7c3aed,transparent 35%),
    var(--bg);

    color:white;

    min-height:100vh;

}



/* Loader */

#loader{

    position:fixed;

    inset:0;

    display:flex;

    justify-content:center;

    align-items:center;

    background:#020617;

    z-index:9999;

}



/* Sidebar */

.sidebar{

    position:fixed;

    left:0;

    top:0;

    width:260px;

    height:100vh;

    padding:30px 20px;

    background:rgba(15,23,42,.75);

    backdrop-filter:blur(20px);

    border-right:1px solid rgba(255,255,255,.1);

}



.logo{

    font-size:25px;

    font-weight:700;

    margin-bottom:40px;

    color:var(--primary);

}



.sidebar ul{

    list-style:none;

}



.sidebar li{

    padding:16px;

    margin:10px 0;

    border-radius:14px;

    cursor:pointer;

    transition:.3s;

    color:#cbd5e1;

}



.sidebar li:hover,
.sidebar li.active{

    background:linear-gradient(
    135deg,
    var(--primary),
    var(--secondary)
    );

    color:white;

}



/* Main Area */

.main{

    margin-left:260px;

    padding:30px;

}



/* Topbar */

.topbar{

    display:flex;

    justify-content:space-between;

    align-items:center;

    margin-bottom:30px;

}



.topbar h2{

    font-size:30px;

}



#babyID{

    color:var(--muted);

}



.profile{

    display:flex;

    gap:15px;

    align-items:center;

}



#logoutBtn{

    padding:12px 20px;

    border:none;

    border-radius:12px;

    background:#ef4444;

    color:white;

    cursor:pointer;

}



/* Stats */

.stats-grid{

    display:grid;

    grid-template-columns:
    repeat(auto-fit,minmax(220px,1fr));

    gap:20px;

}



.card{

    background:var(--card);

    backdrop-filter:blur(20px);

    border-radius:22px;

    padding:25px;

    border:1px solid rgba(255,255,255,.08);

    transition:.3s;

}



.card:hover{

    transform:translateY(-5px);

}



.card h3{

    color:var(--muted);

    margin-bottom:15px;

}



.card h1{

    font-size:35px;

}
/* ==================================
   BABY STUDY PROJECT
   dashboard.css
   Module 2B-2
================================== */


/* Timer Card */

.timer-card,
.goal-card,
.subject-card,
.task-card,
.group-card,
.leaderboard-card,
.analytics-card,
.profile-card,
.challenge-card,
.notification-card,
.settings-card{

    background:var(--card);

    backdrop-filter:blur(20px);

    border-radius:24px;

    padding:30px;

    margin-top:25px;

    border:1px solid rgba(255,255,255,.08);

}


.timer-card h2,
.goal-card h2,
.subject-card h2,
.task-card h2{

    margin-bottom:20px;

}


/* Subject Select */

#subjectSelect{

    width:100%;

    padding:15px;

    border:none;

    border-radius:14px;

    background:#0f172a;

    color:white;

    font-size:16px;

}



/* Timer */

#timer{

    font-size:70px;

    font-weight:700;

    text-align:center;

    margin:30px 0;

    color:var(--primary);

    letter-spacing:3px;

}



/* Timer Buttons */

.buttons{

    display:flex;

    gap:15px;

    justify-content:center;

    flex-wrap:wrap;

}


.buttons button{

    padding:14px 25px;

    border:none;

    border-radius:14px;

    cursor:pointer;

    color:white;

    font-weight:600;

    transition:.3s;

}


#startTimer{

    background:#22c55e;

}


#pauseTimer{

    background:#f59e0b;

}


#resetTimer{

    background:#ef4444;

}


.buttons button:hover{

    transform:translateY(-3px);

}



/* Goal Section */

#dailyGoalInput{

    padding:14px;

    width:120px;

    border-radius:12px;

    border:none;

    background:#0f172a;

    color:white;

}


#saveGoal{

    padding:14px 25px;

    margin-left:10px;

    border:none;

    border-radius:12px;

    background:var(--primary);

    color:white;

    cursor:pointer;

}


.progress-bar{

    width:100%;

    height:18px;

    background:#1e293b;

    border-radius:20px;

    margin-top:25px;

    overflow:hidden;

}


#progressFill{

    height:100%;

    width:0%;

    background:linear-gradient(
    90deg,
    var(--primary),
    var(--secondary)
    );

    transition:.5s;

}



/* Subject Manager */

.subject-input,
.task-input{

    display:flex;

    gap:10px;

}


.subject-input input,
.task-input input{

    flex:1;

    padding:15px;

    border:none;

    border-radius:12px;

    background:#0f172a;

    color:white;

}


.subject-input button,
.task-input button{

    width:60px;

    border:none;

    border-radius:12px;

    background:var(--primary);

    color:white;

    font-size:22px;

    cursor:pointer;

}



.subject-list{

    margin-top:20px;

}


.subject-item{

    display:flex;

    justify-content:space-between;

    padding:16px;

    margin-top:12px;

    background:#0f172a;

    border-radius:14px;

}



/* Tasks */


.task-item{

    display:flex;

    justify-content:space-between;

    align-items:center;

    margin-top:12px;

    padding:15px;

    background:#0f172a;

    border-radius:14px;

}


.task-item.completed{

    opacity:.6;

    text-decoration:line-through;

}



/* Leaderboard */


.leader-row{

    display:flex;

    justify-content:space-between;

    align-items:center;

    padding:18px;

    background:#0f172a;

    border-radius:15px;

    margin-top:12px;

}


.leader-row.top{

    border:1px solid #eab308;

    background:rgba(234,179,8,.15);

}


#openLeaderboard{

    margin-top:20px;

    padding:14px 25px;

    border:none;

    border-radius:14px;

    background:linear-gradient(
    135deg,
    var(--primary),
    var(--secondary)
    );

    color:white;

    cursor:pointer;

}
/* ==================================
   BABY STUDY PROJECT
   dashboard.css
   Module 2B-3
================================== */


/* Group Section */

.group-box{

    background:#0f172a;

    padding:25px;

    border-radius:18px;

    text-align:center;

}


.group-box h3{

    margin-bottom:15px;

}


.group-box p{

    color:var(--muted);

    margin-bottom:20px;

}


.group-box button{

    padding:14px 22px;

    margin:8px;

    border:none;

    border-radius:12px;

    cursor:pointer;

    background:linear-gradient(
    135deg,
    var(--primary),
    var(--secondary)
    );

    color:white;

    font-weight:600;

}



/* Analytics */

.analytics-grid{

    display:grid;

    grid-template-columns:
    repeat(auto-fit,minmax(180px,1fr));

    gap:20px;

}


.analytics-grid div{

    background:#0f172a;

    padding:25px;

    border-radius:18px;

    text-align:center;

}


.analytics-grid h3{

    color:var(--muted);

    margin-bottom:10px;

}


.analytics-grid p{

    font-size:25px;

    font-weight:700;

    color:var(--primary);

}



/* Profile */

.profile-box{

    display:flex;

    align-items:center;

    gap:20px;

    background:#0f172a;

    padding:25px;

    border-radius:20px;

}


.avatar{

    width:70px;

    height:70px;

    display:flex;

    align-items:center;

    justify-content:center;

    border-radius:50%;

    background:linear-gradient(
    135deg,
    var(--primary),
    var(--secondary)
    );

    font-size:32px;

    font-weight:700;

}



/* Challenges */

.challenge-box{

    background:#0f172a;

    padding:25px;

    border-radius:18px;

}


.challenge-box h3{

    margin-bottom:10px;

}


.challenge-box p{

    color:var(--muted);

}


.challenge-progress{

    width:100%;

    height:15px;

    background:#1e293b;

    border-radius:20px;

    margin:20px 0;

    overflow:hidden;

}


#challengeFill{

    width:30%;

    height:100%;

    background:linear-gradient(
    90deg,
    #22c55e,
    var(--primary)
    );

}


#joinChallenge{

    padding:13px 25px;

    border:none;

    border-radius:12px;

    background:#22c55e;

    color:white;

    cursor:pointer;

}



/* Notifications */


.notification{

    background:#0f172a;

    padding:16px;

    border-radius:14px;

    margin-top:12px;

    color:#cbd5e1;

}



/* Settings */


.setting-item{

    display:flex;

    justify-content:space-between;

    align-items:center;

    padding:18px;

    background:#0f172a;

    border-radius:14px;

    margin-top:12px;

}


.setting-item input{

    width:20px;

    height:20px;

}



/* Mobile Navigation */


.mobile-nav{

    display:none;

}



/* Responsive */


@media(max-width:900px){


.sidebar{

    width:80px;

}


.logo{

    font-size:0;

}


.logo:first-letter{

    font-size:30px;

}


.sidebar li{

    font-size:0;

    text-align:center;

}


.sidebar li::first-letter{

    font-size:25px;

}


.main{

    margin-left:80px;

}


}



@media(max-width:600px){


.sidebar{

    display:none;

}


.main{

    margin-left:0;

    padding:20px;

}


.topbar{

    flex-direction:column;

    align-items:flex-start;

    gap:20px;

}


#timer{

    font-size:45px;

}


.mobile-nav{

    display:flex;

    position:fixed;

    bottom:0;

    left:0;

    width:100%;

    height:70px;

    background:rgba(15,23,42,.9);

    backdrop-filter:blur(20px);

    justify-content:space-around;

    align-items:center;

    border-top:1px solid rgba(255,255,255,.1);

}


.mobile-nav button{

    background:none;

    border:none;

    color:white;

    font-size:12px;

}


.profile-box{

    flex-direction:column;

    text-align:center;

}


.subject-input,
.task-input{

    flex-direction:column;

}


.subject-input button,
.task-input button{

    width:100%;

}


}
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>BabyStudy Groups</title>

<link rel="stylesheet" href="groups.css">

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">

<script defer src="firebase.js"></script>
<script defer src="groups.js"></script>

</head>


<body>


<div class="background"></div>


<!-- Header -->

<header class="header">

<h1>
👥 BabyStudy Groups
</h1>


<button onclick="location.href='dashboard.html'">
← Dashboard
</button>


</header>



<main class="container">


<!-- Create Group -->


<section class="group-card">


<h2>
🚀 Create Study Group
</h2>


<input 
id="groupName"
placeholder="Group Name">


<input 
id="groupGoal"
placeholder="Group Goal (Example: JEE 2027)">


<select id="memberLimit">

<option value="10">
10 Members
</option>

<option value="20">
20 Members
</option>

<option value="50">
50 Members
</option>

</select>


<button id="createGroup">

Create Group

</button>


</section>




<!-- Join Group -->


<section class="group-card">


<h2>
🔑 Join Group
</h2>


<input
id="inviteCode"
placeholder="Enter Invite Code">


<button id="requestJoin">

Send Join Request

</button>


<p id="joinStatus">

</p>


</section>




<!-- My Group -->


<section class="group-card">


<h2>
🏠 My Group
</h2>


<div id="myGroup">


<p>
No group joined yet.
</p>


</div>


</section>




<!-- Owner Panel -->


<section class="group-card owner-panel">


<h2>
👑 Owner Dashboard
</h2>


<div id="requests">


<h3>
Join Requests
</h3>


</div>



<div id="members">


<h3>
Members
</h3>


</div>



</section>





<!-- Group Leaderboard -->


<section class="group-card">


<h2>
🏆 Group Ranking
</h2>


<div id="groupLeaderboard">


<div class="rank">

🥇 QuantumJEE - 15h

</div>


<div class="rank">

🥈 PhysicsMaster - 12h

</div>


<div class="rank">

🥉 MathWizard - 10h

</div>


</div>


</section>




<!-- Challenge -->


<section class="group-card">


<h2>
🔥 Group Challenge
</h2>


<h3 id="challengeTitle">

No Active Challenge

</h3>


<p id="challengeInfo">

Owner can create study challenges.

</p>


<button id="createChallenge">

Create Challenge

</button>


</section>



</main>


</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   groups.css
   Module 3B
================================== */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}


:root{

    --primary:#38bdf8;
    --secondary:#8b5cf6;
    --bg:#020617;
    --card:rgba(15,23,42,.75);
    --text:#ffffff;
    --muted:#94a3b8;

}


body{

    font-family:'Poppins',sans-serif;

    min-height:100vh;

    background:var(--bg);

    color:white;

}



/* Background */

.background{

    position:fixed;

    inset:0;

    z-index:-1;

    background:

    radial-gradient(circle at top left,#2563eb,transparent 35%),

    radial-gradient(circle at bottom right,#7c3aed,transparent 35%),

    #020617;

}



/* Header */

.header{

    display:flex;

    justify-content:space-between;

    align-items:center;

    padding:30px 8%;

}



.header h1{

    font-size:35px;

}


.header button{

    padding:12px 22px;

    border:none;

    border-radius:12px;

    background:var(--primary);

    color:white;

    cursor:pointer;

    font-weight:600;

}



/* Container */

.container{

    width:90%;

    max-width:1100px;

    margin:auto;

}



/* Cards */

.group-card{

    background:var(--card);

    backdrop-filter:blur(20px);

    border-radius:25px;

    padding:30px;

    margin:25px 0;

    border:1px solid rgba(255,255,255,.08);

    box-shadow:0 20px 40px rgba(0,0,0,.3);

}


.group-card h2{

    margin-bottom:25px;

}



/* Inputs */

.group-card input,
.group-card select{

    width:100%;

    padding:15px;

    margin:10px 0;

    border:none;

    border-radius:14px;

    background:#0f172a;

    color:white;

    font-size:16px;

}


.group-card input:focus{

    outline:2px solid var(--primary);

}



/* Buttons */

.group-card button{

    padding:14px 25px;

    border:none;

    border-radius:14px;

    background:linear-gradient(

    135deg,

    var(--primary),

    var(--secondary)

    );

    color:white;

    cursor:pointer;

    font-weight:600;

    margin-top:10px;

    transition:.3s;

}


.group-card button:hover{

    transform:translateY(-3px);

}



/* Group Info */

#myGroup{

    background:#0f172a;

    padding:20px;

    border-radius:18px;

}



#myGroup h3{

    color:var(--primary);

}



/* Owner Panel */

.owner-panel{

    border:1px solid #eab308;

}



.owner-panel h2{

    color:#facc15;

}



/* Requests & Members */

#requests,
#members{

    background:#0f172a;

    padding:20px;

    border-radius:18px;

    margin-top:15px;

}



.member{

    display:flex;

    justify-content:space-between;

    align-items:center;

    padding:15px;

    background:#1e293b;

    border-radius:12px;

    margin-top:10px;

}



.member button{

    padding:8px 15px;

    margin:0 5px;

}



/* Leaderboard */


.rank{

    display:flex;

    justify-content:space-between;

    padding:18px;

    background:#0f172a;

    border-radius:15px;

    margin-top:12px;

    font-weight:600;

}


.rank:first-child{

    border:1px solid #eab308;

    background:rgba(234,179,8,.15);

}



/* Challenge */

#challengeTitle{

    color:var(--primary);

    margin-bottom:10px;

}


#challengeInfo{

    color:var(--muted);

}



/* Responsive */


@media(max-width:700px){

.header{

    flex-direction:column;

    gap:20px;

    text-align:center;

}


.header h1{

    font-size:28px;

}


.group-card{

    padding:20px;

}


.member{

    flex-direction:column;

    gap:10px;

}

}
/* ==================================
   BABY STUDY PROJECT
   groups.js
   Module 3C
================================== */


const groupCreateBtn =
document.getElementById("createGroup");


const joinBtn =
document.getElementById("requestJoin");



let currentUser = null;



// -----------------------------
// Load User
// -----------------------------

firebase.auth().onAuthStateChanged(async(user)=>{

    if(!user){

        window.location.href="index.html";

        return;

    }


    currentUser=user;


    loadMyGroup();

});




// -----------------------------
// Generate Invite Code
// -----------------------------

function generateCode(){

    return "BS-" +

    Math.random()
    .toString(36)
    .substring(2,8)
    .toUpperCase();

}




// -----------------------------
// Create Group
// -----------------------------

groupCreateBtn.addEventListener("click",async()=>{


const name =
document.getElementById("groupName").value.trim();


const goal =
document.getElementById("groupGoal").value.trim();


const limit =
document.getElementById("memberLimit").value;



if(name.length < 3){

    alert("Group name too short");

    return;

}



const userDoc =
await db.collection("users")
.doc(currentUser.uid)
.get();


const user =
userDoc.data();



const groupCode =
generateCode();



await db.collection("groups")
.doc(groupCode)
.set({

    groupName:name,

    goal:goal,

    inviteCode:groupCode,

    ownerUID:currentUser.uid,


    ownerName:user.username,


    maxMembers:Number(limit),


    members:[{

        uid:currentUser.uid,

        username:user.username,

        babyID:user.babyID,

        role:"owner",

        hours:0,

        streak:0

    }],


    requests:[],


    createdAt:
    firebase.firestore.FieldValue.serverTimestamp()


});



await db.collection("users")
.doc(currentUser.uid)
.update({

    group:groupCode

});



alert(
"Group Created!\nInvite Code: "
+groupCode
);


loadMyGroup();


});




// -----------------------------
// Join Request
// -----------------------------

joinBtn.addEventListener("click",async()=>{


const code =
document.getElementById("inviteCode")
.value
.trim()
.toUpperCase();



if(!code){

    alert("Enter invite code");

    return;

}



const groupRef =
db.collection("groups").doc(code);



const group =
await groupRef.get();



if(!group.exists){

    alert("Group not found");

    return;

}



const userDoc =
await db.collection("users")
.doc(currentUser.uid)
.get();


const user=userDoc.data();



await groupRef.update({

requests:
firebase.firestore.FieldValue.arrayUnion({

    uid:currentUser.uid,

    username:user.username,

    babyID:user.babyID

})

});



document.getElementById("joinStatus")
.innerHTML =
"✅ Request sent to owner";


});




// -----------------------------
// Load My Group
// -----------------------------

async function loadMyGroup(){


const userDoc =
await db.collection("users")
.doc(currentUser.uid)
.get();



const user=userDoc.data();



if(!user.group){

    return;

}



const groupDoc =
await db.collection("groups")
.doc(user.group)
.get();



if(!groupDoc.exists)
return;



const group=groupDoc.data();



document.getElementById("myGroup")
.innerHTML=`

<h3>
${group.groupName}
</h3>

<p>
Code: ${group.inviteCode}
</p>

<p>
Members:
${group.members.length}
/
${group.maxMembers}
</p>

`;



loadMembers(group);


}




// -----------------------------
// Owner Member View
// -----------------------------

function loadMembers(group){


const box =
document.getElementById("members");



box.innerHTML =
"<h3>Members</h3>";



group.members.forEach(member=>{


box.innerHTML +=`

<div class="member">

<span>
${member.username}
<br>
${member.babyID}
</span>


<span>
${member.role}
</span>


</div>

`;


});


}




// -----------------------------
// Owner Approve Request
// -----------------------------

async function approveMember(
groupID,
request
){



const ref =
db.collection("groups")
.doc(groupID);



await ref.update({


members:
firebase.firestore.FieldValue
.arrayUnion({

uid:request.uid,

username:request.username,

babyID:request.babyID,

role:"member",

hours:0,

streak:0

}),


requests:
firebase.firestore.FieldValue
.arrayRemove(request)


});



alert("Member Approved");


}




// -----------------------------
// Reject Request
// -----------------------------

async function rejectMember(
groupID,
request
){


await db.collection("groups")
.doc(groupID)
.update({


requests:
firebase.firestore.FieldValue
.arrayRemove(request)


});


}
rules_version = '2';

service cloud.firestore {

  match /databases/{database}/documents {


    // ==========================
    // USER PROFILE
    // ==========================

    match /users/{userId} {


      // User can create own profile
      allow create:
      if request.auth != null
      && request.auth.uid == userId;


      // User can read own profile
      allow read:
      if request.auth != null
      && request.auth.uid == userId;


      // User can update only own study data
      allow update:
      if request.auth != null
      && request.auth.uid == userId;


      // No deletion from client
      allow delete:
      if false;

    }




    // ==========================
    // GROUP SYSTEM
    // ==========================

    match /groups/{groupId} {


      // Anyone logged in can view group info
      // (Only public group data)
      allow read:
      if request.auth != null;



      // Create group
      // Creator becomes owner
      allow create:
      if request.auth != null
      &&
      request.resource.data.ownerUID
      ==
      request.auth.uid;



      // Group owner controls group settings
      allow update:
      if request.auth != null
      &&
      resource.data.ownerUID
      ==
      request.auth.uid;



      // Prevent deleting groups
      allow delete:
      if false;


    }




    // ==========================
    // LEADERBOARD
    // ==========================

    match /leaderboard/{entryId} {


      allow read:

      if request.auth != null;



      allow create,update:

      if request.auth != null
      &&
      request.resource.data.uid
      ==
      request.auth.uid;



      allow delete:

      if false;

    }




    // ==========================
    // CHALLENGES
    // ==========================

    match /challenges/{challengeId} {


      allow read:

      if request.auth != null;


      allow create:

      if request.auth != null;



      allow update:

      if request.auth != null;



      allow delete:

      if false;


    }

  }

}
/* ==================================
   BABY STUDY PROJECT
   timer.js
   Module 4A
================================== */


let seconds = 0;

let timerRunning = false;

let interval = null;



const timerDisplay =
document.getElementById("timer");


const startBtn =
document.getElementById("startTimer");


const pauseBtn =
document.getElementById("pauseTimer");


const resetBtn =
document.getElementById("resetTimer");



const subjectSelect =
document.getElementById("subjectSelect");




// Load saved timer

if(localStorage.getItem("babyTimer")){

    seconds =
    Number(localStorage.getItem("babyTimer"));

    updateTimer();

}




// --------------------------
// Start Timer
// --------------------------

startBtn?.addEventListener("click",()=>{


if(timerRunning)
return;


timerRunning=true;



interval=setInterval(()=>{


seconds++;


updateTimer();


saveTimer();



if(seconds % 60 === 0){

    saveStudyMinute();

}


},1000);



});




// --------------------------
// Pause Timer
// --------------------------

pauseBtn?.addEventListener("click",()=>{


timerRunning=false;


clearInterval(interval);


});




// --------------------------
// Reset Timer
// --------------------------

resetBtn?.addEventListener("click",()=>{


clearInterval(interval);


timerRunning=false;


seconds=0;


updateTimer();


saveTimer();


});





// --------------------------
// Timer Display
// --------------------------

function updateTimer(){


if(!timerDisplay)
return;



let h =
Math.floor(seconds/3600);


let m =
Math.floor((seconds%3600)/60);


let s =
seconds%60;



timerDisplay.innerHTML =

`${String(h).padStart(2,"0")}:
${String(m).padStart(2,"0")}:
${String(s).padStart(2,"0")}`;


}





// --------------------------
// Save Timer
// --------------------------

function saveTimer(){


localStorage.setItem(

"babyTimer",

seconds

);


}





// --------------------------
// Save Study Minute
// --------------------------

async function saveStudyMinute(){



const user =
firebase.auth().currentUser;



if(!user)
return;



const subject =
subjectSelect.value;



const userRef =
db.collection("users")
.doc(user.uid);



const data =
await userRef.get();



let profile =
data.data();



let subjects =
profile.subjects || {};



if(!subjects[subject]){

subjects[subject]=0;

}



subjects[subject]+=1;



await userRef.update({

    subjects:subjects,


    totalHours:
    firebase.firestore.FieldValue.increment(
    1/60
    ),


    todayHours:
    firebase.firestore.FieldValue.increment(
    1/60
    ),


    xp:
    firebase.firestore.FieldValue.increment(
    10
    )

});



}




// --------------------------
// Daily Reset Check
// --------------------------

function checkDailyReset(){


let lastDate =
localStorage.getItem(
"babyLastDate"
);



let today =
new Date()
.toDateString();



if(lastDate !== today){


localStorage.setItem(
"babyLastDate",
today
);



seconds=0;


updateTimer();


}


}



checkDailyReset();
/* ==================================
   BABY STUDY PROJECT
   studyTracker.js
   Module 4B
================================== */


let studyData = {

    Physics:{
        hours:0,
        problems:0
    },

    Chemistry:{
        hours:0,
        problems:0
    },

    Mathematics:{
        hours:0,
        problems:0
    },

    Revision:{
        hours:0,
        problems:0
    }

};



const problemInput =
document.getElementById("problemCount");

const addProblemBtn =
document.getElementById("addProblem");




// Load Study Data

async function loadStudyData(){


const user =
firebase.auth().currentUser;


if(!user)
return;



const snap =
await db.collection("users")
.doc(user.uid)
.get();



if(snap.exists){


const data=snap.data();


studyData =
data.studyData ||
studyData;



updateStudyUI();


}


}




// Add Problems Solved

addProblemBtn?.addEventListener(
"click",
async()=>{


let count =
Number(problemInput.value);



if(!count || count<1)
return;



let subject =
document.getElementById(
"subjectSelect"
).value;



if(!studyData[subject]){


studyData[subject]={

hours:0,

problems:0

};


}



studyData[subject].problems += count;



await saveStudyData();



problemInput.value="";



});






// Save Data

async function saveStudyData(){



const user =
firebase.auth().currentUser;


if(!user)
return;



await db.collection("users")
.doc(user.uid)
.update({

studyData:studyData


});



updateStudyUI();


}




// Update UI

function updateStudyUI(){



for(let sub in studyData){



let element =
document.getElementById(
sub+"Stats"
);



if(element){


element.innerHTML=`

${studyData[sub].hours.toFixed(1)}
Hours

<br>

${studyData[sub].problems}
Problems

`;

}


}



}





// Calculate Daily Progress

function calculateProgress(
todayHours,
target
){


if(target<=0)
return 0;



let percent =
(todayHours/target)*100;



if(percent>100)
percent=100;



return Math.round(percent);


}





// Goal Update

async function updateDailyGoal(
goal
){



const user =
firebase.auth().currentUser;



if(!user)
return;



await db.collection("users")
.doc(user.uid)
.update({

dailyGoal:Number(goal)

});


}




// Start

firebase.auth()
.onAuthStateChanged(()=>{

loadStudyData();

});
/* ==================================
   BABY STUDY PROJECT
   streakSystem.js
   Module 4C
================================== */


// Check user streak

async function updateStreak(){


const user =
firebase.auth().currentUser;


if(!user)
return;



const ref =
db.collection("users")
.doc(user.uid);



const snap =
await ref.get();



if(!snap.exists)
return;



let data =
snap.data();



let today =
new Date()
.toISOString()
.split("T")[0];



let lastStudy =
data.lastStudyDate || "";



let streak =
data.streak || 0;



// Already counted today

if(lastStudy === today){

    return;

}




let yesterday =
new Date();


yesterday.setDate(
yesterday.getDate()-1
);



let yesterdayDate =
yesterday
.toISOString()
.split("T")[0];



if(lastStudy === yesterdayDate){

    streak++;

}

else{

    streak=1;

}




await ref.update({

    streak:streak,

    lastStudyDate:today

});



checkAchievements(data,streak);


}





// -----------------------------
// Achievement System
// -----------------------------


async function checkAchievements(
data,
streak
){


const user =
firebase.auth().currentUser;


if(!user)
return;



let achievements =
data.achievements || [];




let newAchievements=[];




if(streak>=7 &&
!achievements.includes("7 Day Warrior")){


newAchievements.push(
"7 Day Warrior"
);


}



if(streak>=30 &&
!achievements.includes("30 Day Legend")){


newAchievements.push(
"30 Day Legend"
);


}




let hours =
data.totalHours || 0;



if(hours>=100 &&
!achievements.includes("100 Hour Club")){


newAchievements.push(
"100 Hour Club"
);


}




if(newAchievements.length){



await db.collection("users")
.doc(user.uid)
.update({

achievements:
firebase.firestore.FieldValue
.arrayUnion(
...newAchievements
),


xp:
firebase.firestore.FieldValue
.increment(
newAchievements.length*100
)

});



alert(
"🏆 Achievement Unlocked:\n"+
newAchievements.join("\n")
);


}



}





// -----------------------------
// XP Level System
// -----------------------------


function calculateLevel(xp){


return Math.floor(
xp/500
)+1;


}




async function updateLevel(){


const user =
firebase.auth().currentUser;


if(!user)
return;



const ref =
db.collection("users")
.doc(user.uid);



const snap =
await ref.get();



let data =
snap.data();



let level =
calculateLevel(
data.xp || 0
);



if(level !== data.level){


await ref.update({

level:level

});


}


}





// -----------------------------
// Study Day Log
// -----------------------------


async function saveStudyDay(){


const user =
firebase.auth().currentUser;


if(!user)
return;



let today =
new Date()
.toISOString()
.split("T")[0];



await db.collection("users")
.doc(user.uid)
.update({

studyCalendar:

firebase.firestore.FieldValue
.arrayUnion(today)

});


}





firebase.auth()
.onAuthStateChanged(
(user)=>{

if(user){

updateStreak();

updateLevel();

saveStudyDay();

}

});
/* ==================================
   BABY STUDY PROJECT
   analytics.js
   Module 4D
================================== */


let studyHistory = [];



// -----------------------------
// Load Analytics Data
// -----------------------------

async function loadAnalytics(){


const user =
firebase.auth().currentUser;


if(!user)
return;



const snap =
await db.collection("users")
.doc(user.uid)
.get();



if(!snap.exists)
return;



const data =
snap.data();



studyHistory =
data.studyHistory || [];



updateAnalytics(data);


}




// -----------------------------
// Save Daily Study History
// -----------------------------

async function saveHistory(hours){


const user =
firebase.auth().currentUser;


if(!user)
return;



let today =
new Date()
.toISOString()
.split("T")[0];



const entry={

date:today,

hours:Number(hours)

};



await db.collection("users")
.doc(user.uid)
.update({


studyHistory:

firebase.firestore.FieldValue
.arrayUnion(entry)


});


}





// -----------------------------
// Weekly Hours
// -----------------------------

function weeklyHours(history){


let total=0;



let now =
new Date();



history.forEach(item=>{


let date =
new Date(item.date);



let diff =
(now-date)
/
(1000*60*60*24);



if(diff<=7){

total+=item.hours;

}


});


return total.toFixed(1);


}





// -----------------------------
// Monthly Hours
// -----------------------------

function monthlyHours(history){


let total=0;


let month =
new Date()
.getMonth();



history.forEach(item=>{


let date =
new Date(item.date);



if(date.getMonth()===month){

total+=item.hours;

}


});


return total.toFixed(1);


}





// -----------------------------
// Heatmap Generator
// -----------------------------

function generateHeatmap(history){


let map={};



history.forEach(item=>{


map[item.date]=item.hours;


});



return map;


}




// -----------------------------
// Subject Analysis
// -----------------------------

function subjectPerformance(
subjects
){


let result=[];



for(let sub in subjects){


result.push({

subject:sub,

hours:
subjects[sub].hours || 0,


problems:
subjects[sub].problems || 0


});


}



return result;


}





// -----------------------------
// Update Dashboard
// -----------------------------

function updateAnalytics(data){



const weekly =
document.getElementById(
"weeklyHours"
);



const monthly =
document.getElementById(
"monthlyHours"
);



if(weekly){

weekly.innerText =
weeklyHours(
data.studyHistory || []
)
+"h";

}



if(monthly){

monthly.innerText =
monthlyHours(
data.studyHistory || []
)
+"h";

}


}





// Auto Load

firebase.auth()
.onAuthStateChanged(
(user)=>{

if(user){

loadAnalytics();

}

});
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>BabyStudy Leaderboard</title>

<link rel="stylesheet" href="leaderboard.css">

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">

<script defer src="firebase.js"></script>
<script defer src="leaderboard.js"></script>

</head>


<body>


<div class="background"></div>



<header class="header">

<h1>
🏆 BabyStudy Leaderboard
</h1>


<button onclick="location.href='dashboard.html'">
← Dashboard
</button>


</header>



<main class="container">



<!-- Ranking Filter -->

<section class="filter-card">


<button class="filter active" data-type="daily">

Daily

</button>


<button class="filter" data-type="weekly">

Weekly

</button>


<button class="filter" data-type="monthly">

Monthly

</button>


</section>





<!-- User Position -->

<section class="card my-position">


<h2>
🎯 Your Position
</h2>


<div id="myRank">

Calculating Rank...

</div>


</section>





<!-- Top Ranking -->

<section class="card">


<h2>
🔥 Top Warriors
</h2>


<div id="leaderboardList">


<!-- Dynamic Data -->


</div>


</section>





<!-- Group Ranking -->

<section class="card">


<h2>
👥 Group Ranking
</h2>


<div id="groupLeaderboard">


Loading Group Ranking...


</div>


</section>






<!-- Rewards -->

<section class="card">


<h2>
🏅 Ranking Rewards
</h2>


<div class="reward-grid">


<div>

🥇

<br>

Top 1

<br>

+500 XP

</div>



<div>

🥈

<br>

Top 2

<br>

+300 XP

</div>



<div>

🥉

<br>

Top 3

<br>

+200 XP

</div>



</div>


</section>





<!-- Challenge -->

<section class="card">


<h2>
🔥 Current Competition
</h2>


<div id="competition">


<h3>
10 Day Focus War
</h3>


<p>
Study more, earn XP, climb ranking.
</p>


<div class="competition-bar">

<div id="competitionProgress">

</div>

</div>


</div>


</section>



</main>



</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   leaderboard.css
   Module 5B
================================== */


*{

margin:0;
padding:0;
box-sizing:border-box;

}


:root{

--primary:#38bdf8;
--secondary:#8b5cf6;
--bg:#020617;
--card:rgba(15,23,42,.75);

}



body{

font-family:'Poppins',sans-serif;

background:var(--bg);

color:white;

min-height:100vh;

}




/* Background */


.background{

position:fixed;

inset:0;

z-index:-1;

background:

radial-gradient(circle at top left,#2563eb,transparent 35%),

radial-gradient(circle at bottom right,#7c3aed,transparent 35%),

#020617;

}





/* Header */


.header{

display:flex;

justify-content:space-between;

align-items:center;

padding:30px 8%;

}


.header h1{

font-size:35px;

}



.header button{

padding:13px 22px;

border:none;

border-radius:12px;

background:var(--primary);

color:white;

cursor:pointer;

}





/* Container */


.container{

width:90%;

max-width:1100px;

margin:auto;

}





/* Cards */


.card,
.filter-card{


background:var(--card);

backdrop-filter:blur(20px);

border-radius:25px;

padding:30px;

margin:25px 0;

border:1px solid rgba(255,255,255,.08);

}





/* Filter */


.filter-card{

display:flex;

justify-content:center;

gap:15px;

}



.filter{

padding:13px 25px;

border:none;

border-radius:15px;

background:#0f172a;

color:white;

cursor:pointer;

}



.filter.active{

background:linear-gradient(

135deg,

var(--primary),

var(--secondary)

);

}





/* Ranking */


.rank-item{

display:flex;

justify-content:space-between;

align-items:center;

padding:20px;

margin-top:12px;

background:#0f172a;

border-radius:18px;

transition:.3s;

}



.rank-item:hover{

transform:translateX(5px);

}





/* Top Three */


.rank-item.first{

border:2px solid #eab308;

background:rgba(234,179,8,.15);

}



.rank-item.second{

border:2px solid #94a3b8;

}



.rank-item.third{

border:2px solid #cd7f32;

}





/* Rank Number */


.rank-number{

font-size:25px;

font-weight:700;

}



.username{

font-weight:600;

}



.hours{

color:var(--primary);

font-weight:700;

}





/* My Rank */


#myRank{

text-align:center;

font-size:24px;

color:var(--primary);

}





/* Group Ranking */


.group-user{

display:flex;

justify-content:space-between;

padding:15px;

background:#0f172a;

border-radius:14px;

margin-top:10px;

}





/* Rewards */


.reward-grid{

display:grid;

grid-template-columns:

repeat(auto-fit,minmax(180px,1fr));

gap:20px;

}



.reward-grid div{

background:#0f172a;

padding:25px;

border-radius:18px;

text-align:center;

font-size:18px;

}





/* Competition */


.competition-bar{

height:18px;

background:#1e293b;

border-radius:20px;

overflow:hidden;

margin-top:20px;

}



#competitionProgress{

height:100%;

width:40%;

background:linear-gradient(

90deg,

#22c55e,

var(--primary)

);

}





/* Mobile */


@media(max-width:600px){


.header{

flex-direction:column;

gap:20px;

text-align:center;

}



.header h1{

font-size:28px;

}



.filter-card{

flex-wrap:wrap;

}



.rank-item{

flex-direction:column;

gap:10px;

text-align:center;

}



}
/* ==================================
   BABY STUDY PROJECT
   leaderboard.js
   Module 5C
================================== */


let rankingType = "daily";

let currentUser = null;



const leaderboardList =
document.getElementById("leaderboardList");


const myRank =
document.getElementById("myRank");



const filters =
document.querySelectorAll(".filter");




// -----------------------------
// Auth Check
// -----------------------------

firebase.auth()
.onAuthStateChanged((user)=>{


if(!user){

location.href="index.html";

return;

}


currentUser=user;


loadLeaderboard();


});




// -----------------------------
// Filter Buttons
// -----------------------------

filters.forEach(btn=>{


btn.addEventListener("click",()=>{


filters.forEach(b=>
b.classList.remove("active")
);


btn.classList.add("active");


rankingType =
btn.dataset.type;



loadLeaderboard();


});


});




// -----------------------------
// Load Ranking
// -----------------------------

async function loadLeaderboard(){



const snapshot =
await db.collection("users")
.get();



let users=[];



snapshot.forEach(doc=>{


let data=doc.data();


users.push({

id:doc.id,

username:data.username,

babyID:data.babyID,

todayHours:data.todayHours || 0,

weeklyHours:data.weeklyHours || 0,

monthlyHours:data.monthlyHours || 0,

xp:data.xp || 0

});


});



users.sort((a,b)=>{


let aScore;
let bScore;



if(rankingType==="daily"){


aScore=a.todayHours;

bScore=b.todayHours;


}

else if(rankingType==="weekly"){


aScore=a.weeklyHours;

bScore=b.weeklyHours;


}

else{


aScore=a.monthlyHours;

bScore=b.monthlyHours;


}



return bScore-aScore;


});



displayLeaderboard(users);


calculateMyRank(users);



}






// -----------------------------
// Display Leaderboard
// -----------------------------

function displayLeaderboard(users){



leaderboardList.innerHTML="";



users.slice(0,50)
.forEach((user,index)=>{


let div =
document.createElement("div");



let medal="";

if(index===0)
medal="🥇";

else if(index===1)
medal="🥈";

else if(index===2)
medal="🥉";

else
medal="#"+(index+1);



let hours;



if(rankingType==="daily")
hours=user.todayHours;

else if(rankingType==="weekly")
hours=user.weeklyHours;

else
hours=user.monthlyHours;



div.className =
"rank-item ";


if(index===0)
div.classList.add("first");


if(index===1)
div.classList.add("second");


if(index===2)
div.classList.add("third");



div.innerHTML=`

<span class="rank-number">
${medal}
</span>


<span class="username">

${user.username}

<br>

<small>
${user.babyID}
</small>

</span>


<span class="hours">

${hours.toFixed(1)}h

</span>

`;



leaderboardList.appendChild(div);



});



}





// -----------------------------
// Calculate My Rank
// -----------------------------

function calculateMyRank(users){



let position =
users.findIndex(
u=>u.id===currentUser.uid
);



if(position!==-1){


myRank.innerHTML=

`
You are ranked
<br>

🏆 #${position+1}

`;

}

else{


myRank.innerHTML=
"No ranking yet";


}



}






// -----------------------------
// Group Leaderboard
// -----------------------------


async function loadGroupRanking(){



const box =
document.getElementById(
"groupLeaderboard"
);



if(!box)
return;



const snapshot =
await db.collection("groups")
.get();



box.innerHTML="";



snapshot.forEach(doc=>{


let group=doc.data();



box.innerHTML += `

<div class="group-user">

<span>
${group.groupName}
</span>

<span>
${group.members.length}
Members
</span>

</div>

`;



});



}



loadGroupRanking();
/* ==================================
   BABY STUDY PROJECT
   rankingSystem.js
   Module 5D
================================== */


// -----------------------------
// Calculate Ranking Score
// -----------------------------

function calculateScore(user, type){


let hours=0;



if(type==="daily"){

hours=user.todayHours || 0;

}


else if(type==="weekly"){

hours=user.weeklyHours || 0;

}


else{

hours=user.monthlyHours || 0;

}



let xp =
user.xp || 0;



// 80% study + 20% XP

return (

hours * 80

+

xp * 0.2

);


}




// -----------------------------
// Reset Daily Stats
// -----------------------------

async function dailyReset(){


const users =
await db.collection("users")
.get();



let batch =
db.batch();



users.forEach(doc=>{


batch.update(

doc.ref,

{

todayHours:0,

lastReset:
new Date()

}

);


});



await batch.commit();



console.log(
"Daily ranking reset complete"
);


}





// -----------------------------
// Weekly Reset
// -----------------------------

async function weeklyReset(){


const users =
await db.collection("users")
.get();



let batch =
db.batch();



users.forEach(doc=>{


let data =
doc.data();



batch.update(

doc.ref,

{


weeklyHours:0,


}

);


});



await batch.commit();


}





// -----------------------------
// Monthly Reset
// -----------------------------

async function monthlyReset(){



const users =
await db.collection("users")
.get();



let batch =
db.batch();



users.forEach(doc=>{


batch.update(

doc.ref,

{


monthlyHours:0


}

);


});



await batch.commit();


}





// -----------------------------
// Reward Top Players
// -----------------------------

async function giveRewards(){



const snapshot =
await db.collection("users")
.get();



let users=[];



snapshot.forEach(doc=>{


users.push({

id:doc.id,

...doc.data()

});


});



users.sort(
(a,b)=>
calculateScore(b,"daily")
-
calculateScore(a,"daily")
);



let rewards=[500,300,200];



for(
let i=0;
i<3;
i++
){



if(users[i]){


await db.collection("users")
.doc(users[i].id)
.update({

xp:
firebase.firestore.FieldValue
.increment(
rewards[i]
)


});


}


}



}





// -----------------------------
// Automatic Time Check
// -----------------------------

function checkResetTime(){


let now =
new Date();



let hour =
now.getHours();


let minute =
now.getMinutes();



if(hour===0 && minute===0){


dailyReset();


if(now.getDay()===1){

weeklyReset();

}


if(now.getDate()===1){

monthlyReset();

}


}


}




setInterval(
checkResetTime,
60000
);
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>BabyStudy Admin Panel</title>

<link rel="stylesheet" href="admin.css">

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">

<script defer src="firebase.js"></script>
<script defer src="admin.js"></script>

</head>


<body>


<div class="background"></div>



<header class="admin-header">


<h1>
👑 BabyStudy Owner Panel
</h1>


<button onclick="location.href='dashboard.html'">
← Dashboard
</button>


</header>




<main class="container">



<!-- Admin Verification -->


<section id="adminLogin" class="card">


<h2>
🔐 Owner Verification
</h2>


<input 
id="adminCode"
type="password"
placeholder="Enter Admin Code">


<button id="verifyAdmin">

Verify

</button>


<p id="loginStatus">

</p>


</section>





<!-- Dashboard -->


<section id="adminDashboard" style="display:none;">



<!-- Stats -->


<div class="stats-grid">


<div class="card">

<h3>
Total Users
</h3>

<h1 id="totalUsers">
0
</h1>

</div>



<div class="card">

<h3>
Total Groups
</h3>

<h1 id="totalGroups">
0
</h1>

</div>



<div class="card">

<h3>
Total Study Hours
</h3>

<h1 id="totalHours">
0h
</h1>

</div>



<div class="card">

<h3>
Active Today
</h3>

<h1 id="activeUsers">
0
</h1>

</div>


</div>





<!-- User Management -->


<section class="card">


<h2>
👥 User Management
</h2>


<input 
id="userSearch"
placeholder="Search username">


<div id="userList">


</div>


</section>






<!-- Group Management -->


<section class="card">


<h2>
🏠 Group Management
</h2>


<div id="groupList">


</div>


</section>







<!-- Announcement -->


<section class="card">


<h2>
📢 Send Announcement
</h2>


<textarea 
id="announcement"
placeholder="Write announcement">

</textarea>


<button id="sendAnnouncement">

Send

</button>


</section>






<!-- System Controls -->


<section class="card danger-zone">


<h2>
⚠ System Controls
</h2>


<button id="resetStats">

Reset Daily Stats

</button>



<button id="maintenance">

Maintenance Mode

</button>



</section>




</section>


</main>


</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   admin.css
   Module 6B
================================== */


*{

margin:0;
padding:0;
box-sizing:border-box;

}



:root{

--primary:#38bdf8;
--secondary:#8b5cf6;
--danger:#ef4444;
--bg:#020617;
--card:rgba(15,23,42,.75);

}



body{

font-family:'Poppins',sans-serif;

background:var(--bg);

color:white;

min-height:100vh;

}





/* Background */


.background{

position:fixed;

inset:0;

z-index:-1;

background:

radial-gradient(circle at top left,#2563eb,transparent 35%),

radial-gradient(circle at bottom right,#7c3aed,transparent 35%),

#020617;

}





/* Header */


.admin-header{

display:flex;

justify-content:space-between;

align-items:center;

padding:30px 8%;

}



.admin-header h1{

font-size:35px;

}



.admin-header button{

padding:13px 22px;

border:none;

border-radius:12px;

background:var(--primary);

color:white;

cursor:pointer;

font-weight:600;

}





/* Container */


.container{

width:90%;

max-width:1200px;

margin:auto;

}





/* Card */


.card{

background:var(--card);

backdrop-filter:blur(20px);

border-radius:25px;

padding:30px;

margin:25px 0;

border:1px solid rgba(255,255,255,.08);

}





.card h2{

margin-bottom:20px;

}





/* Inputs */


input,
textarea{

width:100%;

padding:15px;

margin:10px 0;

border:none;

border-radius:14px;

background:#0f172a;

color:white;

font-size:16px;

}



textarea{

height:120px;

resize:none;

}





/* Buttons */


button{

padding:13px 22px;

border:none;

border-radius:12px;

background:linear-gradient(

135deg,

var(--primary),

var(--secondary)

);

color:white;

cursor:pointer;

font-weight:600;

transition:.3s;

}



button:hover{

transform:translateY(-3px);

}





/* Stats */


.stats-grid{

display:grid;

grid-template-columns:

repeat(auto-fit,minmax(220px,1fr));

gap:20px;

}



.stats-grid .card{

text-align:center;

}



.stats-grid h3{

color:#94a3b8;

margin-bottom:15px;

}



.stats-grid h1{

font-size:35px;

color:var(--primary);

}





/* User List */


.user-item,
.group-item{

display:flex;

justify-content:space-between;

align-items:center;

background:#0f172a;

padding:18px;

border-radius:15px;

margin-top:12px;

}





.user-item span,
.group-item span{

color:#cbd5e1;

}





/* Action Buttons */


.user-item button,
.group-item button{

padding:8px 15px;

margin-left:8px;

font-size:13px;

}





/* Danger Zone */


.danger-zone{

border:1px solid var(--danger);

}



.danger-zone h2{

color:#f87171;

}



#resetStats{

background:var(--danger);

margin-right:10px;

}



#maintenance{

background:#f59e0b;

}





/* Mobile */


@media(max-width:700px){


.admin-header{

flex-direction:column;

gap:20px;

text-align:center;

}



.admin-header h1{

font-size:28px;

}



.user-item,
.group-item{

flex-direction:column;

gap:15px;

text-align:center;

}



}
/* ==================================
   BABY STUDY PROJECT
   admin.js
   Module 6C
================================== */


const ADMIN_CODE = "ADMIN2026";


let adminVerified = false;




const verifyBtn =
document.getElementById("verifyAdmin");




// -----------------------------
// Admin Login
// -----------------------------

verifyBtn?.addEventListener(
"click",
()=>{


const code =
document.getElementById("adminCode")
.value;



const status =
document.getElementById("loginStatus");



if(code===ADMIN_CODE){


adminVerified=true;


document.getElementById(
"adminLogin"
).style.display="none";



document.getElementById(
"adminDashboard"
).style.display="block";



status.innerHTML =
"✅ Access Granted";


loadAdminData();



}

else{


status.innerHTML =
"❌ Wrong Admin Code";


}



});






// -----------------------------
// Load Admin Data
// -----------------------------

async function loadAdminData(){


if(!adminVerified)
return;



loadUsers();

loadGroups();

loadStats();


}





// -----------------------------
// Load Users
// -----------------------------

async function loadUsers(){



const box =
document.getElementById(
"userList"
);



box.innerHTML="";



const snapshot =
await db.collection("users")
.get();



snapshot.forEach(doc=>{


let user =
doc.data();



box.innerHTML +=`

<div class="user-item">


<span>

${user.username}

<br>

${user.babyID}

<br>

⭐ XP:
${user.xp || 0}

</span>



<div>

<button onclick="editGoal('${doc.id}')">

Edit Goal

</button>


<button onclick="resetUser('${doc.id}')">

Reset

</button>


</div>


</div>


`;


});


}




// -----------------------------
// Load Groups
// -----------------------------

async function loadGroups(){


const box =
document.getElementById(
"groupList"
);



box.innerHTML="";



const snapshot =
await db.collection("groups")
.get();



snapshot.forEach(doc=>{


let group =
doc.data();



box.innerHTML +=`

<div class="group-item">


<span>

${group.groupName}

<br>

Owner:
${group.ownerName}

<br>

Members:
${group.members.length}

</span>



<button onclick="deleteGroup('${doc.id}')">

Delete

</button>


</div>


`;



});



}




// -----------------------------
// Platform Stats
// -----------------------------

async function loadStats(){



let users =
await db.collection("users")
.get();



let groups =
await db.collection("groups")
.get();



let hours=0;



let active=0;



users.forEach(doc=>{


let data=doc.data();


hours +=
data.totalHours || 0;


if((data.todayHours || 0)>0)

active++;


});



document.getElementById(
"totalUsers"
).innerText =
users.size;



document.getElementById(
"totalGroups"
).innerText =
groups.size;



document.getElementById(
"totalHours"
).innerText =
hours.toFixed(1)+"h";



document.getElementById(
"activeUsers"
).innerText =
active;


}





// -----------------------------
// Edit User Goal
// -----------------------------

async function editGoal(uid){


let goal =
prompt(
"Enter new daily goal hours:"
);



if(!goal)
return;



await db.collection("users")
.doc(uid)
.update({

dailyGoal:Number(goal)

});



alert(
"Goal Updated"
);


}






// -----------------------------
// Reset User
// -----------------------------

async function resetUser(uid){


if(!confirm(
"Reset this user stats?"
))

return;



await db.collection("users")
.doc(uid)
.update({

todayHours:0,

weeklyHours:0,

monthlyHours:0,

xp:0,

streak:0

});



alert(
"User Reset"
);



loadUsers();


}






// -----------------------------
// Delete Group
// -----------------------------

async function deleteGroup(id){



if(!confirm(
"Delete this group?"
))

return;



await db.collection("groups")
.doc(id)
.delete();



loadGroups();


}





// -----------------------------
// Announcement
// -----------------------------

document
.getElementById("sendAnnouncement")
?.addEventListener(
"click",
async()=>{


let text =
document.getElementById(
"announcement"
).value;



if(!text)
return;



await db.collection(
"announcements"
)
.add({

message:text,

time:
firebase.firestore.FieldValue
.serverTimestamp()

});



alert(
"Announcement Sent"
);



});






// -----------------------------
// Reset All Daily Stats
// -----------------------------

document
.getElementById("resetStats")
?.addEventListener(
"click",
async()=>{


if(!confirm(
"Reset everyone's daily stats?"
))

return;



const users =
await db.collection("users")
.get();



let batch =
db.batch();



users.forEach(doc=>{


batch.update(
doc.ref,
{

todayHours:0

}

);


});



await batch.commit();



alert(
"Daily stats reset"
);



});
/* ==================================
   BABY STUDY PROJECT
   admin.js v2
   Secure Owner Panel
================================== */


let isOwner = false;


// Replace with your Firebase Auth UID
const OWNER_UID = "YOUR_OWNER_UID";



// -----------------------------
// Check Owner
// -----------------------------

firebase.auth()
.onAuthStateChanged(async(user)=>{


if(!user){

location.href="index.html";

return;

}



if(user.uid === OWNER_UID){


isOwner=true;


document
.getElementById("adminDashboard")
.style.display="block";


document
.getElementById("adminLogin")
.style.display="none";


loadAdmin();


}

else{


alert(
"Access denied. Owner only."
);


location.href="dashboard.html";


}



});




// -----------------------------
// Load Admin Dashboard
// -----------------------------

async function loadAdmin(){


if(!isOwner)
return;


loadStats();

loadUsers();

loadGroups();


}




// -----------------------------
// Statistics
// -----------------------------

async function loadStats(){


let users =
await db.collection("users")
.get();



let groups =
await db.collection("groups")
.get();



let hours=0;



users.forEach(doc=>{


hours +=
doc.data().totalHours || 0;


});



totalUsers.innerText =
users.size;


totalGroups.innerText =
groups.size;


totalHours.innerText =
hours.toFixed(1)+"h";


}




// -----------------------------
// Users
// -----------------------------

async function loadUsers(){


let box =
document.getElementById(
"userList"
);


box.innerHTML="";



let snap =
await db.collection("users")
.get();



snap.forEach(doc=>{


let u=doc.data();



box.innerHTML +=`

<div class="user-item">

<span>

${u.username}

<br>

ID:
${u.babyID}

<br>

XP:
${u.xp || 0}

</span>


<button onclick="changeGoal('${doc.id}')">

Edit Goal

</button>


</div>

`;



});


}




// -----------------------------
// Edit Goal
// -----------------------------

async function changeGoal(uid){


let goal =
prompt(
"New daily goal:"
);



if(!goal)
return;



await db.collection("users")
.doc(uid)
.update({

dailyGoal:
Number(goal)

});


alert(
"Goal Updated"
);


}




// -----------------------------
// Groups
// -----------------------------

async function loadGroups(){


let box =
document.getElementById(
"groupList"
);



box.innerHTML="";



let snap =
await db.collection("groups")
.get();



snap.forEach(doc=>{


let g=doc.data();



box.innerHTML +=`

<div class="group-item">


<span>

${g.groupName}

<br>

Owner:
${g.ownerName}

<br>

Members:
${g.members.length}

</span>


</div>

`;


});


}




// -----------------------------
// Announcement
// -----------------------------

async function sendNotice(){


let msg =
document.getElementById(
"announcement"
).value;



if(!msg)
return;



await db.collection(
"announcements"
)
.add({

message:msg,

created:
firebase.firestore.FieldValue
.serverTimestamp()

});



alert(
"Announcement published"
);


}
rules_version = '2';

service cloud.firestore {

match /databases/{database}/documents {



/* ==========================
   USER DATA
========================== */


match /users/{uid} {


allow create:

if request.auth != null
&& request.auth.uid == uid;



allow read:

if request.auth != null;



// User can update own data only
allow update:

if request.auth != null
&& request.auth.uid == uid;



// Owner can manage all users
allow update, delete:

if request.auth != null
&& request.auth.uid == "YOUR_OWNER_UID";



}




/* ==========================
   GROUP SYSTEM
========================== */


match /groups/{groupId} {



allow read:

if request.auth != null;



// Anyone logged in can create group
allow create:

if request.auth != null
&& request.resource.data.ownerUID
==
request.auth.uid;



// Only group owner can edit

allow update:

if request.auth != null
&& resource.data.ownerUID
==
request.auth.uid;



// Only platform owner can delete groups

allow delete:

if request.auth != null
&& request.auth.uid ==
"YOUR_OWNER_UID";



}





/* ==========================
   ANNOUNCEMENTS
========================== */


match /announcements/{id} {


allow read:

if request.auth != null;



// Only owner can create

allow create:

if request.auth != null
&& request.auth.uid ==
"YOUR_OWNER_UID";



allow delete:

if request.auth != null
&& request.auth.uid ==
"YOUR_OWNER_UID";



}




/* ==========================
   LEADERBOARD
========================== */


match /leaderboard/{id} {



allow read:

if request.auth != null;



allow write:

if request.auth != null
&& request.auth.uid ==
resource.data.uid;



}





/* ==========================
   CHALLENGES
========================== */


match /challenges/{id} {



allow read:

if request.auth != null;



allow create,update:

if request.auth != null
&& request.auth.uid ==
"YOUR_OWNER_UID";



allow delete:

if request.auth != null
&& request.auth.uid ==
"YOUR_OWNER_UID";



}



}

}
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>BabyStudy Challenges</title>

<link rel="stylesheet" href="challenge.css">

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">

<script defer src="firebase.js"></script>
<script defer src="challenge.js"></script>

</head>


<body>


<div class="background"></div>



<header class="header">


<h1>
🔥 BabyStudy Challenges
</h1>


<button onclick="location.href='dashboard.html'">

← Dashboard

</button>


</header>




<main class="container">





<!-- Create Challenge (Owner) -->


<section class="card owner-section">


<h2>
👑 Create Challenge
</h2>


<input 
id="challengeName"
placeholder="Challenge name">


<input 
id="challengeDays"
type="number"
placeholder="Duration (Days)">



<input 
id="challengeTarget"
type="number"
placeholder="Daily Target Hours">



<button id="createChallenge">

Create Challenge

</button>


</section>







<!-- Active Challenges -->


<section class="card">


<h2>
🔥 Active Challenges
</h2>



<div id="challengeList">


<div class="challenge-card">


<h3>
10 Day Focus War
</h3>


<p>
Duration: 10 Days
</p>


<p>
Target: 10 Hours/day
</p>


<button>

Join Challenge

</button>


</div>



</div>


</section>








<!-- My Challenges -->


<section class="card">


<h2>
🎯 My Challenges
</h2>


<div id="myChallenges">

No active challenge

</div>


</section>







<!-- Challenge Ranking -->


<section class="card">


<h2>
🏆 Challenge Leaderboard
</h2>


<div id="challengeRanking">


Loading...


</div>


</section>







<!-- Rules -->


<section class="card">


<h2>
📜 Rules
</h2>


<ul>


<li>
Complete daily target
</li>


<li>
Maintain consistency
</li>


<li>
Missing target may remove participant
</li>


<li>
Highest hours wins
</li>


</ul>


</section>





</main>



</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   challenge.css
   Module 7B
================================== */


*{

margin:0;
padding:0;
box-sizing:border-box;

}



:root{

--primary:#38bdf8;
--purple:#8b5cf6;
--green:#22c55e;
--danger:#ef4444;

}



body{

font-family:'Poppins',sans-serif;

background:#020617;

color:white;

min-height:100vh;

}




.background{

position:fixed;

inset:0;

z-index:-1;

background:

radial-gradient(circle at top left,#2563eb,transparent 35%),

radial-gradient(circle at bottom right,#7c3aed,transparent 35%),

#020617;

}





/* Header */


.header{

display:flex;

justify-content:space-between;

align-items:center;

padding:30px 8%;

}



.header h1{

font-size:35px;

}



.header button{

padding:13px 22px;

border:none;

border-radius:12px;

background:var(--primary);

color:white;

cursor:pointer;

}





/* Container */


.container{

width:90%;

max-width:1100px;

margin:auto;

}





/* Cards */


.card{

background:

rgba(15,23,42,.75);

backdrop-filter:blur(20px);

padding:30px;

border-radius:25px;

margin:25px 0;

border:1px solid rgba(255,255,255,.08);

}





/* Inputs */


input{

width:100%;

padding:15px;

margin:10px 0;

background:#0f172a;

border:none;

border-radius:14px;

color:white;

font-size:16px;

}





/* Buttons */


button{

padding:13px 22px;

border:none;

border-radius:14px;

background:

linear-gradient(

135deg,

var(--primary),

var(--purple)

);

color:white;

font-weight:600;

cursor:pointer;

transition:.3s;

}



button:hover{

transform:translateY(-3px);

}





/* Challenge Card */


.challenge-card{

background:#0f172a;

padding:25px;

border-radius:20px;

margin-top:15px;

border:1px solid rgba(255,255,255,.1);

}



.challenge-card h3{

color:var(--primary);

font-size:24px;

margin-bottom:10px;

}



.challenge-card p{

color:#cbd5e1;

margin:8px 0;

}





/* Progress Bar */


.progress{

height:15px;

background:#1e293b;

border-radius:20px;

overflow:hidden;

margin:15px 0;

}



.progress span{

display:block;

height:100%;

width:60%;

background:

linear-gradient(

90deg,

var(--green),

var(--primary)

);

}





/* Ranking */


.rank-card{

display:flex;

justify-content:space-between;

align-items:center;

padding:18px;

background:#0f172a;

border-radius:15px;

margin-top:12px;

}



.rank-card.first{

border:2px solid #eab308;

background:rgba(234,179,8,.15);

}



.rank-card.second{

border:2px solid #94a3b8;

}



.rank-card.third{

border:2px solid #cd7f32;

}





/* Rules */


ul{

padding-left:25px;

}



li{

margin:10px 0;

color:#cbd5e1;

}





/* Winner Badge */


.badge{

display:inline-block;

padding:7px 15px;

border-radius:20px;

background:#eab308;

color:black;

font-weight:700;

}





/* Mobile */


@media(max-width:700px){


.header{

flex-direction:column;

gap:20px;

text-align:center;

}



.header h1{

font-size:28px;

}



.rank-card{

flex-direction:column;

gap:10px;

}



}
/* ==================================
   BABY STUDY PROJECT
   challenge.js
   Module 7C
================================== */


const OWNER_UID = "YOUR_OWNER_UID";


let currentUser = null;



firebase.auth()
.onAuthStateChanged(user=>{


if(!user)
return;


currentUser=user;


loadChallenges();


});




// ================================
// CREATE CHALLENGE (OWNER)
// ================================


async function createChallenge(){


if(currentUser.uid !== OWNER_UID){

alert("Owner only");

return;

}



let name =
document.getElementById(
"challengeName"
).value;


let days =
Number(document.getElementById(
"challengeDays"
).value);



let target =
Number(document.getElementById(
"challengeTarget"
).value);



if(!name || !days || !target){

alert("Fill all details");

return;

}



await db.collection("challenges")
.add({

name:name,

duration:days,

dailyTarget:target,


participants:[],


status:"active",


createdAt:
firebase.firestore.FieldValue
.serverTimestamp()


});



alert(
"Challenge Created 🔥"
);


loadChallenges();


}




document
.getElementById("createChallenge")
?.addEventListener(
"click",
createChallenge
);







// ================================
// LOAD CHALLENGES
// ================================


async function loadChallenges(){


let box =
document.getElementById(
"challengeList"
);



box.innerHTML="";



let snap =
await db.collection("challenges")
.orderBy("createdAt","desc")
.get();



snap.forEach(doc=>{


let c=doc.data();



box.innerHTML +=`

<div class="challenge-card">


<h3>

${c.name}

</h3>


<p>
Duration:
${c.duration} Days
</p>


<p>
Target:
${c.dailyTarget} Hours/day
</p>



<button onclick="joinChallenge('${doc.id}')">

Join

</button>



${
currentUser.uid===OWNER_UID

?

`

<button onclick="editChallenge('${doc.id}')">

Edit

</button>


<button onclick="deleteChallenge('${doc.id}')">

Delete

</button>

`

:

""

}



</div>


`;



});


}








// ================================
// JOIN CHALLENGE
// ================================


async function joinChallenge(id){


let user =
await db.collection("users")
.doc(currentUser.uid)
.get();



let data=user.data();



await db.collection("challenges")
.doc(id)
.update({

participants:

firebase.firestore.FieldValue
.arrayUnion({

uid:currentUser.uid,

username:data.username,

babyID:data.babyID,

hours:0,

status:"active"

})

});



alert(
"Joined Challenge 🔥"
);


}







// ================================
// OWNER EDIT
// ================================


async function editChallenge(id){



let newName =
prompt(
"New Challenge Name"
);



let newTarget =
prompt(
"New Daily Target Hours"
);



if(!newName || !newTarget)
return;



await db.collection("challenges")
.doc(id)
.update({

name:newName,

dailyTarget:Number(newTarget)

});



alert(
"Challenge Updated"
);



loadChallenges();


}








// ================================
// OWNER DELETE
// ================================


async function deleteChallenge(id){



if(currentUser.uid !== OWNER_UID){

return;

}



let confirmDelete =
confirm(
"Delete this challenge?"
);



if(!confirmDelete)
return;



await db.collection("challenges")
.doc(id)
.delete();



alert(
"Challenge Deleted"
);



loadChallenges();


}








// ================================
// CHALLENGE LEADERBOARD
// ================================


async function loadChallengeRanking(id){


let snap =
await db.collection("challenges")
.doc(id)
.get();



let challenge =
snap.data();



let users =
challenge.participants;



users.sort(
(a,b)=>
b.hours-a.hours
);



return users;


}
/* ==================================
   BABY STUDY PROJECT
   challengeRules.js
   Module 7D
================================== */


const OWNER_UID =
"YOUR_OWNER_UID";



// ================================
// CHECK CHALLENGE STATUS
// ================================


async function checkChallengeStatus(
challengeId
){


const ref =
db.collection("challenges")
.doc(challengeId);



const snap =
await ref.get();



if(!snap.exists)
return;



let challenge =
snap.data();



let today =
new Date();



let start =
new Date(
challenge.startDate
);



let end =
new Date(
challenge.endDate
);



if(today < start){


await ref.update({

status:"upcoming"

});


}



else if(today > end){


await ref.update({

status:"completed"

});


calculateWinner(challengeId);


}



else{


await ref.update({

status:"active"

});


}


}





// ================================
// DAILY TARGET CHECK
// ================================


async function checkDailyProgress(
challengeId
){



const ref =
db.collection("challenges")
.doc(challengeId);



const snap =
await ref.get();



let challenge =
snap.data();



let updatedParticipants=[];



challenge.participants
.forEach(member=>{



if(
member.todayHours <
challenge.dailyTarget
){


member.warning =
(member.warning || 0)+1;



}



// 3 warnings = eliminated

if(member.warning >=3){


member.status =
"eliminated";


}



updatedParticipants.push(member);



});





await ref.update({

participants:
updatedParticipants


});



}







// ================================
// WINNER CALCULATION
// ================================


async function calculateWinner(
challengeId
){



const ref =
db.collection("challenges")
.doc(challengeId);



const snap =
await ref.get();



let challenge =
snap.data();



let players =
challenge.participants
.filter(
p=>p.status!=="eliminated"
);



players.sort(
(a,b)=>
b.hours-a.hours
);



let winners =
players.slice(0,3);





await ref.update({

winners:winners


});



giveRewards(winners);



}








// ================================
// GIVE REWARDS
// ================================


async function giveRewards(
winners
){



let rewards=[500,300,200];



for(
let i=0;
i<winners.length;
i++
){


await db.collection("users")
.doc(winners[i].uid)
.update({

xp:

firebase.firestore.FieldValue
.increment(
rewards[i]
),


badges:

firebase.firestore.FieldValue
.arrayUnion(

"Challenge Winner"

)

});


}



}





// ================================
// DAILY AUTO CHECK
// ================================


setInterval(()=>{


db.collection("challenges")
.where(
"status",
"==",
"active"
)
.get()
.then(snapshot=>{


snapshot.forEach(doc=>{


checkDailyProgress(
doc.id
);


});


});


},


86400000
);
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>BabyStudy Profile</title>


<link rel="stylesheet" href="profile.css">


<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">


<script defer src="firebase.js"></script>

<script defer src="profile.js"></script>


</head>



<body>


<div class="background"></div>




<header class="header">


<h1>
👤 My Profile
</h1>


<button onclick="location.href='dashboard.html'">

← Dashboard

</button>


</header>






<main class="container">






<!-- Profile Card -->


<section class="card profile-card">



<div class="avatar">

👤

</div>



<h2 id="username">

Loading...

</h2>


<p id="babyID">

Baby ID

</p>



<div class="level-box">


⭐ Level

<span id="level">

1

</span>



</div>



</section>









<!-- Stats -->


<section class="card">


<h2>
📊 Study Statistics
</h2>



<div class="stats-grid">


<div>

🔥

<h3 id="streak">

0

</h3>

<p>
Day Streak
</p>

</div>




<div>

⏱

<h3 id="totalHours">

0

</h3>

<p>
Study Hours
</p>

</div>





<div>

⭐

<h3 id="xp">

0

</h3>

<p>
XP

</p>

</div>



</div>


</section>








<!-- Subjects -->


<section class="card">


<h2>
📚 Subjects
</h2>



<div id="subjects">


<p>
Physics: 0h
</p>


<p>
Chemistry: 0h
</p>


<p>
Mathematics: 0h
</p>


</div>


</section>








<!-- Goal -->


<section class="card">


<h2>
🎯 Daily Goal
</h2>


<input 
id="dailyGoal"
type="number"
placeholder="Hours">


<button id="saveGoal">

Save Goal

</button>


</section>









<!-- Achievements -->


<section class="card">


<h2>
🏅 Achievements
</h2>


<div id="badges"
class="badge-grid">


<p>
No badges yet
</p>


</div>


</section>








<!-- Edit Profile -->


<section class="card">


<h2>
✏️ Edit Profile
</h2>


<input 
id="newUsername"
placeholder="New username">


<button id="updateProfile">

Update

</button>


</section>





</main>


</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   profile.css
   Module 8B
================================== */


*{

margin:0;
padding:0;
box-sizing:border-box;

}



:root{

--primary:#38bdf8;

--purple:#8b5cf6;

--gold:#facc15;

--card:rgba(15,23,42,.75);

}



body{

font-family:'Poppins',sans-serif;

background:#020617;

color:white;

min-height:100vh;

}





.background{

position:fixed;

inset:0;

z-index:-1;

background:

radial-gradient(circle at top left,#2563eb,transparent 35%),

radial-gradient(circle at bottom right,#7c3aed,transparent 35%),

#020617;

}





/* Header */


.header{

display:flex;

justify-content:space-between;

align-items:center;

padding:30px 8%;

}



.header h1{

font-size:35px;

}



.header button{

padding:13px 22px;

border:none;

border-radius:12px;

background:var(--primary);

color:white;

cursor:pointer;

font-weight:600;

}





/* Container */


.container{

width:90%;

max-width:1000px;

margin:auto;

}





/* Cards */


.card{

background:var(--card);

backdrop-filter:blur(20px);

border-radius:25px;

padding:30px;

margin:25px 0;

border:1px solid rgba(255,255,255,.08);

box-shadow:0 20px 40px rgba(0,0,0,.3);

}





/* Profile */


.profile-card{

text-align:center;

}



.avatar{

height:100px;

width:100px;

margin:auto;

border-radius:50%;

background:

linear-gradient(

135deg,

var(--primary),

var(--purple)

);

display:flex;

align-items:center;

justify-content:center;

font-size:50px;

}



#username{

margin-top:20px;

font-size:30px;

}



#babyID{

color:#94a3b8;

}





.level-box{

display:inline-block;

margin-top:15px;

padding:12px 25px;

border-radius:20px;

background:#0f172a;

color:var(--gold);

font-weight:700;

}





/* Stats */


.stats-grid{

display:grid;

grid-template-columns:

repeat(auto-fit,minmax(180px,1fr));

gap:20px;

}



.stats-grid div{

background:#0f172a;

padding:25px;

border-radius:20px;

text-align:center;

}



.stats-grid h3{

font-size:30px;

color:var(--primary);

}



.stats-grid p{

color:#94a3b8;

}





/* Subjects */


#subjects p{

background:#0f172a;

padding:15px;

border-radius:15px;

margin:10px 0;

}





/* Inputs */


input{

width:100%;

padding:15px;

margin:10px 0;

background:#0f172a;

border:none;

border-radius:14px;

color:white;

font-size:16px;

}





/* Buttons */


button{

padding:13px 22px;

border:none;

border-radius:14px;

background:

linear-gradient(

135deg,

var(--primary),

var(--purple)

);

color:white;

font-weight:600;

cursor:pointer;

}





/* Badges */


.badge-grid{

display:grid;

grid-template-columns:

repeat(auto-fit,minmax(150px,1fr));

gap:15px;

}



.badge-grid p,
.badge{

background:#0f172a;

padding:20px;

border-radius:18px;

text-align:center;

border:1px solid var(--gold);

color:var(--gold);

}





/* XP Bar */


.xp-bar{

height:15px;

background:#1e293b;

border-radius:20px;

overflow:hidden;

margin-top:15px;

}



.xp-progress{

height:100%;

width:70%;

background:

linear-gradient(

90deg,

var(--primary),

var(--purple)

);

}





/* Mobile */


@media(max-width:700px){


.header{

flex-direction:column;

gap:20px;

text-align:center;

}



.header h1{

font-size:28px;

}



.stats-grid{

grid-template-columns:1fr;

}



}
/* ==================================
   BABY STUDY PROJECT
   profile.js
   Module 8C
================================== */


let currentUser = null;




// -----------------------------
// Authentication
// -----------------------------

firebase.auth()
.onAuthStateChanged(user=>{


if(!user){

location.href="index.html";

return;

}


currentUser=user;


loadProfile();


});






// -----------------------------
// Load Profile
// -----------------------------

async function loadProfile(){



const snap =
await db.collection("users")
.doc(currentUser.uid)
.get();



if(!snap.exists)
return;



const data =
snap.data();




document.getElementById(
"username"
).innerText =
data.username || "Student";



document.getElementById(
"babyID"
).innerText =
"ID: " + 
(data.babyID || "BS00000");



document.getElementById(
"streak"
).innerText =
data.streak || 0;



document.getElementById(
"totalHours"
).innerText =
(data.totalHours || 0)
.toFixed(1);



document.getElementById(
"xp"
).innerText =
data.xp || 0;



document.getElementById(
"level"
).innerText =
calculateLevel(
data.xp || 0
);



document.getElementById(
"dailyGoal"
).value =
data.dailyGoal || 15;



loadSubjects(
data.studyData
);



loadBadges(
data.achievements
);



}








// -----------------------------
// Level System
// -----------------------------

function calculateLevel(xp){


return Math.floor(
xp / 500
)+1;


}







// -----------------------------
// Subjects
// -----------------------------

function loadSubjects(subjects){


const box =
document.getElementById(
"subjects"
);



box.innerHTML="";



if(!subjects)
return;



for(let sub in subjects){


box.innerHTML +=`

<p>

📚 ${sub}

<br>

${subjects[sub].hours || 0}
Hours

<br>

${subjects[sub].problems || 0}
Problems

</p>

`;


}


}








// -----------------------------
// Badges
// -----------------------------

function loadBadges(badges){


const box =
document.getElementById(
"badges"
);



box.innerHTML="";



if(!badges ||
badges.length===0){


box.innerHTML=
"No badges yet";


return;


}



badges.forEach(
badge=>{


box.innerHTML +=`

<div class="badge">

🏅

<br>

${badge}

</div>

`;


});


}








// -----------------------------
// Save Goal
// -----------------------------


document
.getElementById("saveGoal")
?.addEventListener(
"click",
async()=>{


let goal =
Number(
document.getElementById(
"dailyGoal"
).value
);



await db.collection("users")
.doc(currentUser.uid)
.update({

dailyGoal:goal

});



alert(
"Daily goal updated 🎯"
);


});








// -----------------------------
// Update Username
// -----------------------------


document
.getElementById("updateProfile")
?.addEventListener(
"click",
async()=>{


let name =
document.getElementById(
"newUsername"
).value.trim();



if(name.length < 3){

alert(
"Name too short"
);

return;

}




await db.collection("users")
.doc(currentUser.uid)
.update({

username:name

});



alert(
"Profile Updated"
);



loadProfile();


});
<!-- Settings -->

<section class="card">

<h2>
⚙️ Privacy & Settings
</h2>


<label>

<input type="checkbox" id="publicProfile">

Show profile on leaderboard

</label>


<br><br>


<label>

<input type="checkbox" id="showStats">

Show study stats publicly

</label>


<br><br>


<button id="saveSettings">

Save Settings

</button>



<button id="logout">

Logout

</button>


<button id="deleteAccount">

Delete Account Request

</button>


</section>
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">


<title>BabyStudy Notifications</title>


<link rel="stylesheet" href="notification.css">


<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">


<script defer src="firebase.js"></script>

<script defer src="notification.js"></script>


</head>



<body>


<div class="background"></div>




<header class="header">


<h1>
🔔 Notifications
</h1>


<button onclick="location.href='dashboard.html'">

← Dashboard

</button>


</header>







<main class="container">





<!-- Notification Stats -->


<section class="card notification-header">


<h2>

📢 Notification Center

</h2>



<div class="notification-count">


Unread:

<span id="unreadCount">

0

</span>


</div>


</section>









<!-- Owner Announcement -->


<section class="card">


<h2>

👑 Owner Announcements

</h2>



<div id="announcementList">


Loading announcements...

</div>



</section>








<!-- Personal Notifications -->


<section class="card">


<h2>

🔔 My Notifications

</h2>



<div id="notificationList">


Loading notifications...

</div>



</section>








<!-- Achievement Alerts -->


<section class="card">


<h2>

🏆 Achievement Updates

</h2>



<div id="achievementList">


No new achievements

</div>



</section>









<!-- Actions -->


<section class="card actions">


<button id="markAllRead">

Mark All Read

</button>



<button id="clearNotifications">

Clear Notifications

</button>



</section>






</main>


</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   notification.css
   Module 9B
================================== */


*{

margin:0;
padding:0;
box-sizing:border-box;

}



:root{

--primary:#38bdf8;

--purple:#8b5cf6;

--green:#22c55e;

--danger:#ef4444;

}



body{

font-family:'Poppins',sans-serif;

background:#020617;

color:white;

min-height:100vh;

}




.background{

position:fixed;

inset:0;

z-index:-1;

background:

radial-gradient(circle at top left,#2563eb,transparent 35%),

radial-gradient(circle at bottom right,#7c3aed,transparent 35%),

#020617;

}





/* Header */


.header{

display:flex;

justify-content:space-between;

align-items:center;

padding:30px 8%;

}



.header h1{

font-size:35px;

}



.header button{

padding:13px 22px;

border:none;

border-radius:12px;

background:var(--primary);

color:white;

cursor:pointer;

font-weight:600;

}





/* Container */


.container{

width:90%;

max-width:1000px;

margin:auto;

}





/* Cards */


.card{

background:

rgba(15,23,42,.75);

backdrop-filter:blur(20px);

border-radius:25px;

padding:30px;

margin:25px 0;

border:1px solid rgba(255,255,255,.08);

}





/* Count */


.notification-count{

margin-top:15px;

color:#cbd5e1;

font-size:18px;

}



#unreadCount{

color:var(--primary);

font-weight:700;

}





/* Notification Item */


.notification-item{

display:flex;

justify-content:space-between;

align-items:center;

background:#0f172a;

padding:18px;

border-radius:18px;

margin-top:12px;

border:1px solid transparent;

transition:.3s;

}



.notification-item:hover{

transform:translateY(-3px);

}





/* Unread */


.notification-item.unread{

border-color:var(--primary);

background:

rgba(56,189,248,.1);

}





.notification-title{

font-weight:700;

font-size:18px;

}



.notification-message{

color:#cbd5e1;

margin-top:5px;

}



.notification-time{

font-size:12px;

color:#64748b;

}





/* Announcement */


.announcement{

background:

linear-gradient(

135deg,

rgba(56,189,248,.2),

rgba(139,92,246,.2)

);

padding:20px;

border-radius:20px;

margin-top:15px;

border-left:5px solid var(--primary);

}





/* Achievement */


.achievement{

display:flex;

align-items:center;

gap:15px;

background:#0f172a;

padding:20px;

border-radius:18px;

margin-top:12px;

}



.achievement-icon{

font-size:35px;

}



.achievement h3{

color:#facc15;

}





/* Buttons */


button{

padding:13px 22px;

border:none;

border-radius:14px;

background:

linear-gradient(

135deg,

var(--primary),

var(--purple)

);

color:white;

font-weight:600;

cursor:pointer;

transition:.3s;

}



button:hover{

transform:translateY(-3px);

}





.actions{

display:flex;

gap:15px;

flex-wrap:wrap;

}





#clearNotifications{

background:var(--danger);

}





/* Mobile */


@media(max-width:700px){


.header{

flex-direction:column;

gap:20px;

text-align:center;

}



.header h1{

font-size:28px;

}



.notification-item{

flex-direction:column;

align-items:flex-start;

gap:10px;

}



}
/* ==================================
   BABY STUDY PROJECT
   notification.js
   Module 9C
================================== */


let currentUser = null;



firebase.auth()
.onAuthStateChanged(user=>{


if(!user){

location.href="index.html";

return;

}



currentUser=user;


loadNotifications();

loadAnnouncements();

loadAchievements();


});







// ================================
// LOAD USER NOTIFICATIONS
// ================================


function loadNotifications(){



db.collection("notifications")

.where(
"userID",
"==",
currentUser.uid
)

.orderBy(
"timestamp",
"desc"
)

.onSnapshot(snapshot=>{



let box =
document.getElementById(
"notificationList"
);



box.innerHTML="";



let unread=0;



snapshot.forEach(doc=>{


let n=doc.data();



if(!n.read)

unread++;



box.innerHTML +=`

<div class="notification-item
${n.read ? "" : "unread"}"

onclick="markRead('${doc.id}')">


<div>


<div class="notification-title">

${n.title}

</div>


<div class="notification-message">

${n.message}

</div>



<div class="notification-time">

${formatDate(n.timestamp)}

</div>


</div>


</div>

`;


});



document.getElementById(
"unreadCount"
).innerText =
unread;



});



}








// ================================
// OWNER ANNOUNCEMENTS
// ================================


function loadAnnouncements(){



db.collection("announcements")

.orderBy(
"time",
"desc"
)

.limit(20)

.onSnapshot(snapshot=>{


let box =
document.getElementById(
"announcementList"
);



box.innerHTML="";



snapshot.forEach(doc=>{


let a=doc.data();



box.innerHTML +=`

<div class="announcement">


<h3>

📢 ${a.title || "Owner Message"}

</h3>


<p>

${a.message}

</p>


</div>


`;



});



});



}









// ================================
// MARK AS READ
// ================================


async function markRead(id){


await db.collection(
"notifications"
)

.doc(id)

.update({

read:true

});


}








// ================================
// MARK ALL READ
// ================================


document
.getElementById("markAllRead")
?.addEventListener(
"click",
async()=>{


let snap =
await db.collection(
"notifications"
)

.where(
"userID",
"==",
currentUser.uid
)

.get();



let batch =
db.batch();



snap.forEach(doc=>{


batch.update(

doc.ref,

{

read:true

}

);


});



await batch.commit();



});








// ================================
// CLEAR NOTIFICATIONS
// ================================


document
.getElementById("clearNotifications")
?.addEventListener(
"click",
async()=>{


if(!confirm(
"Clear all notifications?"
))

return;



let snap =
await db.collection(
"notifications"
)

.where(
"userID",
"==",
currentUser.uid
)

.get();



let batch =
db.batch();



snap.forEach(doc=>{


batch.delete(doc.ref);


});



await batch.commit();


});








// ================================
// ACHIEVEMENTS
// ================================


async function loadAchievements(){



let snap =
await db.collection("users")
.doc(currentUser.uid)
.get();



let data =
snap.data();



let badges =
data.achievements || [];



let box =
document.getElementById(
"achievementList"
);



box.innerHTML="";



if(badges.length===0){


box.innerHTML =
"No achievements yet";


return;

}



badges.forEach(b=>{


box.innerHTML +=`

<div class="achievement">


<div class="achievement-icon">

🏆

</div>


<h3>

${b}

</h3>


</div>


`;


});



}







// ================================
// DATE FORMAT
// ================================


function formatDate(time){


if(!time)
return "";



return new Date(
time.seconds*1000
)
.toLocaleString();


}
<section class="card">

<h2>
📢 Owner Announcement Center
</h2>


<input id="announcementTitle"
placeholder="Title">


<textarea id="announcementMessage"
placeholder="Write announcement...">
</textarea>


<select id="announcementType">

<option value="all">
All Members
</option>

<option value="group">
Specific Group
</option>

<option value="challenge">
Challenge Alert
</option>

</select>


<input id="targetGroup"
placeholder="Group ID (optional)">


<button id="sendAnnouncement">

Send Announcement

</button>


</section>
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">


<title>BabyStudy Focus Timer</title>


<link rel="stylesheet" href="timer.css">


<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">


<script defer src="firebase.js"></script>

<script defer src="timer.js"></script>


</head>


<body>


<div class="background"></div>




<header class="header">


<h1>
⏱ BabyStudy Focus Timer
</h1>


<button onclick="location.href='dashboard.html'">

← Dashboard

</button>


</header>







<main class="container">





<!-- Timer Card -->


<section class="card timer-card">


<h2>

🧠 Focus Session

</h2>




<select id="subject">


<option value="Physics">

Physics ⚛️

</option>


<option value="Chemistry">

Chemistry 🧪

</option>


<option value="Mathematics">

Mathematics 📐

</option>


<option value="Revision">

Revision 📖

</option>


</select>






<div id="timer">

00:00:00

</div>





<div class="buttons">


<button id="start">

▶ Start

</button>


<button id="pause">

⏸ Pause

</button>


<button id="reset">

🔄 Reset

</button>


</div>



</section>








<!-- Goal Progress -->


<section class="card">


<h2>

🎯 Daily Goal

</h2>



<div class="progress">

<span id="goalProgress"></span>

</div>



<p id="goalText">

0 / 15 Hours

</p>



</section>








<!-- Quick Modes -->


<section class="card">


<h2>

🔥 Focus Modes

</h2>



<div class="mode-grid">


<button id="normalMode">

Normal

</button>


<button id="pomodoroMode">

🍅 Pomodoro

</button>


<button id="focusMode">

🧠 Deep Focus

</button>


</div>



</section>









<!-- Today's Stats -->


<section class="card">


<h2>

📊 Today's Study

</h2>




<div class="stats-grid">


<div>

<h3 id="physics">

0h

</h3>

<p>

Physics

</p>

</div>



<div>

<h3 id="chemistry">

0h

</h3>

<p>

Chemistry

</p>

</div>



<div>

<h3 id="math">

0h

</h3>

<p>

Maths

</p>

</div>



</div>



</section>







<!-- Session History -->


<section class="card">


<h2>

📚 Session History

</h2>



<div id="history">

No sessions yet

</div>


</section>





</main>



</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   timer.css
   Module 10B
================================== */


*{

margin:0;
padding:0;
box-sizing:border-box;

}



:root{

--primary:#38bdf8;

--purple:#8b5cf6;

--green:#22c55e;

--orange:#f59e0b;

}



body{

font-family:'Poppins',sans-serif;

background:#020617;

color:white;

min-height:100vh;

}





.background{

position:fixed;

inset:0;

z-index:-1;

background:

radial-gradient(circle at top left,#2563eb,transparent 35%),

radial-gradient(circle at bottom right,#7c3aed,transparent 35%),

#020617;

}






/* Header */


.header{

display:flex;

justify-content:space-between;

align-items:center;

padding:30px 8%;

}



.header h1{

font-size:35px;

}



.header button{

padding:13px 22px;

border:none;

border-radius:12px;

background:var(--primary);

color:white;

cursor:pointer;

font-weight:600;

}





/* Container */


.container{

width:90%;

max-width:1000px;

margin:auto;

}






/* Cards */


.card{

background:

rgba(15,23,42,.75);

backdrop-filter:blur(20px);

padding:30px;

border-radius:25px;

margin:25px 0;

border:1px solid rgba(255,255,255,.08);

box-shadow:0 20px 40px rgba(0,0,0,.3);

}






/* Timer */


.timer-card{

text-align:center;

}



select{

width:100%;

padding:15px;

background:#0f172a;

color:white;

border:none;

border-radius:15px;

margin:20px 0;

font-size:16px;

}





#timer{

font-size:70px;

font-weight:700;

letter-spacing:5px;

color:var(--primary);

margin:30px 0;

text-shadow:

0 0 25px rgba(56,189,248,.5);

}







/* Buttons */


.buttons{

display:flex;

gap:15px;

justify-content:center;

flex-wrap:wrap;

}



button{

padding:14px 25px;

border:none;

border-radius:15px;

background:

linear-gradient(

135deg,

var(--primary),

var(--purple)

);

color:white;

font-weight:700;

cursor:pointer;

transition:.3s;

}



button:hover{

transform:translateY(-3px);

}






#start{

background:var(--green);

}



#pause{

background:var(--orange);

}



#reset{

background:#ef4444;

}







/* Progress */


.progress{

height:18px;

background:#1e293b;

border-radius:20px;

overflow:hidden;

}



.progress span{

display:block;

height:100%;

width:0%;

background:

linear-gradient(

90deg,

var(--green),

var(--primary)

);

transition:.5s;

}





#goalText{

text-align:center;

margin-top:15px;

color:#cbd5e1;

}








/* Modes */


.mode-grid{

display:grid;

grid-template-columns:

repeat(auto-fit,minmax(200px,1fr));

gap:15px;

}



#pomodoroMode{

background:#ef4444;

}



#focusMode{

background:#8b5cf6;

}








/* Stats */


.stats-grid{

display:grid;

grid-template-columns:

repeat(auto-fit,minmax(180px,1fr));

gap:20px;

}



.stats-grid div{

background:#0f172a;

padding:25px;

border-radius:20px;

text-align:center;

}



.stats-grid h3{

font-size:30px;

color:var(--primary);

}







/* History */


.history-item{

background:#0f172a;

padding:15px;

border-radius:15px;

margin-top:10px;

display:flex;

justify-content:space-between;

}








/* Focus Mode */


.focus-active{

background:#000;

}



.focus-active #timer{

font-size:90px;

color:#22c55e;

}








/* Mobile */


@media(max-width:700px){


.header{

flex-direction:column;

gap:20px;

text-align:center;

}



.header h1{

font-size:28px;

}



#timer{

font-size:45px;

}



}
/* ==================================
   BABY STUDY PROJECT
   timer.js
   Module 10C
================================== */


let currentUser = null;

let seconds = 0;

let interval = null;

let selectedSubject = "Physics";

let sessionStart = null;



// -----------------------------
// Authentication
// -----------------------------

firebase.auth()
.onAuthStateChanged(user=>{


if(!user){

location.href="index.html";

return;

}


currentUser=user;


loadUserData();


});







// -----------------------------
// Timer Elements
// -----------------------------

const timer =
document.getElementById("timer");



const subject =
document.getElementById("subject");



subject?.addEventListener(
"change",
()=>{

selectedSubject =
subject.value;

});






// -----------------------------
// Start Timer
// -----------------------------


document
.getElementById("start")
?.addEventListener(
"click",
()=>{


if(interval)
return;



sessionStart =
Date.now();



interval =
setInterval(()=>{


seconds++;


timer.innerText =
formatTime(seconds);



},1000);



});







// -----------------------------
// Pause Timer
// -----------------------------


document
.getElementById("pause")
?.addEventListener(
"click",
()=>{


clearInterval(interval);

interval=null;



saveSession();


});







// -----------------------------
// Reset Timer
// -----------------------------


document
.getElementById("reset")
?.addEventListener(
"click",
()=>{


clearInterval(interval);

interval=null;


seconds=0;


timer.innerText=
"00:00:00";


});








// -----------------------------
// Save Study Session
// -----------------------------


async function saveSession(){


if(seconds<60)
return;



let hours =
seconds/3600;



let userRef =
db.collection("users")
.doc(currentUser.uid);



let snap =
await userRef.get();



let data =
snap.data();





let studyData =
data.studyData || {};



if(!studyData[selectedSubject]){


studyData[selectedSubject]={

hours:0,

sessions:0

};


}



studyData[selectedSubject].hours += hours;



studyData[selectedSubject].sessions++;





await userRef.update({


totalHours:
(firebase.firestore.FieldValue.increment(hours)),


xp:

firebase.firestore.FieldValue.increment(

Math.floor(hours*100)

),



studyData:studyData,


todayHours:

firebase.firestore.FieldValue.increment(hours)


});



seconds=0;


timer.innerText=
"00:00:00";


loadUserData();


}








// -----------------------------
// Load User Stats
// -----------------------------


async function loadUserData(){


let snap =
await db.collection("users")
.doc(currentUser.uid)
.get();



let data =
snap.data();



let today =
data.studyData || {};



document.getElementById(
"physics"
).innerText =

(today.Physics?.hours || 0)
.toFixed(1)+"h";



document.getElementById(
"chemistry"
).innerText =

(today.Chemistry?.hours || 0)
.toFixed(1)+"h";



document.getElementById(
"math"
).innerText =

(today.Mathematics?.hours || 0)
.toFixed(1)+"h";



let goal =
data.dailyGoal || 15;



let done =
data.todayHours || 0;



document.getElementById(
"goalText"
).innerText =

`${done.toFixed(1)} / ${goal} Hours`;



document.getElementById(
"goalProgress"
).style.width =

Math.min(
(done/goal)*100,
100
)+"%";



}







// -----------------------------
// Format Time
// -----------------------------


function formatTime(s){


let h =
Math.floor(s/3600)
.toString()
.padStart(2,"0");



let m =
Math.floor((s%3600)/60)
.toString()
.padStart(2,"0");



let sec =
(s%60)
.toString()
.padStart(2,"0");



return `${h}:${m}:${sec}`;


}
/* ==================================
   BABY STUDY PROJECT
   focusEngine.js
   Module 10D
================================== */


let focusMode = "normal";

let focusSeconds = 0;

let focusInterval = null;

let isBreak = false;




// Default Pomodoro

const POMODORO_FOCUS = 25 * 60;

const POMODORO_BREAK = 5 * 60;





// ================================
// Normal Mode
// ================================

document
.getElementById("normalMode")
?.addEventListener(
"click",
()=>{


focusMode="normal";


resetFocus();


alert(
"Normal Mode Activated"
);


});





// ================================
// Pomodoro Mode
// ================================

document
.getElementById("pomodoroMode")
?.addEventListener(
"click",
()=>{


focusMode="pomodoro";


focusSeconds =
POMODORO_FOCUS;


startFocus();



});






// ================================
// Deep Focus Mode
// ================================


document
.getElementById("focusMode")
?.addEventListener(
"click",
()=>{


focusMode="deep";


focusSeconds =
60*60;



startFocus();


});






// ================================
// Start Focus
// ================================


function startFocus(){


clearInterval(
focusInterval
);



focusInterval =
setInterval(()=>{


focusSeconds--;



updateFocusTimer();



if(focusSeconds<=0){


completeFocus();


}


},1000);



document.body
.classList.add(
"focus-active"
);


}







// ================================
// Update Display
// ================================


function updateFocusTimer(){


let h =
Math.floor(
focusSeconds/3600
);



let m =
Math.floor(
(focusSeconds%3600)/60
);



let s =
focusSeconds%60;



document.getElementById(
"timer"
).innerText =


`${

h.toString()
.padStart(2,"0")

}:

${

m.toString()
.padStart(2,"0")

}:

${

s.toString()
.padStart(2,"0")

}`;


}







// ================================
// Complete Session
// ================================


async function completeFocus(){


clearInterval(
focusInterval
);



focusInterval=null;



if(
focusMode==="pomodoro"
){



if(!isBreak){


isBreak=true;


focusSeconds =
POMODORO_BREAK;



alert(
"Focus complete! Take a break ☕"
);



startFocus();



}

else{


isBreak=false;


focusSeconds =
POMODORO_FOCUS;


alert(
"Break finished. Focus again 🔥"
);



startFocus();



}



}


else{


saveFocusStreak();


alert(
"Deep Focus Completed 🧠"
);


resetFocus();


}



}







// ================================
// Save Focus Streak
// ================================


async function saveFocusStreak(){



let user =
firebase.auth()
.currentUser;



if(!user)
return;



await db.collection("users")
.doc(user.uid)
.update({

focusSessions:

firebase.firestore.FieldValue
.increment(1),



xp:

firebase.firestore.FieldValue
.increment(50)


});



}







// ================================
// Reset
// ================================


function resetFocus(){


clearInterval(
focusInterval
);



focusInterval=null;


focusSeconds=0;


isBreak=false;


document.body
.classList.remove(
"focus-active"
);



}
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width,initial-scale=1.0">

<title>BabyStudy Analytics</title>

<link rel="stylesheet" href="analytics.css">

<script defer src="firebase.js"></script>
<script defer src="analytics.js"></script>

</head>


<body>

<div class="background"></div>


<header class="header">

<h1>📊 Study Analytics</h1>

<button onclick="location.href='dashboard.html'">
← Dashboard
</button>

</header>



<main class="container">



<section class="card">

<h2>🔥 Performance Overview</h2>


<div class="stats-grid">


<div>
<h3 id="totalHours">
0h
</h3>
<p>Total Hours</p>
</div>


<div>
<h3 id="weeklyHours">
0h
</h3>
<p>This Week</p>
</div>


<div>
<h3 id="bestStreak">
0
</h3>
<p>Best Streak</p>
</div>


<div>
<h3 id="sessions">
0
</h3>
<p>Sessions</p>
</div>


</div>

</section>





<section class="card">


<h2>📚 Subject Distribution</h2>


<div id="subjectStats">

Loading...

</div>


</section>





<section class="card">


<h2>🏆 Personal Records</h2>


<div id="records">

</div>


</section>





<section class="card">


<h2>📅 Weekly Progress</h2>


<div id="weeklyChart">

</div>


</section>




</main>


</body>

</html>
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">


<title>BabyStudy Groups</title>


<link rel="stylesheet" href="group.css">


<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">


<script defer src="firebase.js"></script>

<script defer src="group.js"></script>


</head>


<body>


<div class="background"></div>




<header class="header">


<h1>
🏠 Study Groups
</h1>


<button onclick="location.href='dashboard.html'">

← Dashboard

</button>


</header>







<main class="container">





<!-- Create / Join Group -->


<section class="card">


<h2>

🏠 Group Access

</h2>



<input 
id="groupName"
placeholder="New Group Name">



<button id="createGroup">

Create Group

</button>




<hr>




<input
id="groupID"
placeholder="Enter Group ID">



<button id="joinGroup">

Send Join Request

</button>



</section>









<!-- Current Group -->


<section class="card">


<h2>

👥 Current Group

</h2>



<div id="groupInfo">

No group joined

</div>


</section>









<!-- Members -->


<section class="card">


<h2>

🏆 Group Leaderboard

</h2>



<div id="memberList">

Loading...

</div>


</section>









<!-- Rules -->


<section class="card">


<h2>

📜 Group Rules

</h2>



<ul id="groupRules">

<li>
No rules added
</li>

</ul>


</section>









<!-- Owner Panel -->


<section class="card admin-panel">


<h2>

👑 Owner Control

</h2>



<div id="adminControls">


Owner controls will appear here

</div>



</section>






</main>



</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   group.css
   Module 11B
================================== */


*{

margin:0;
padding:0;
box-sizing:border-box;

}



:root{

--primary:#38bdf8;

--purple:#8b5cf6;

--gold:#facc15;

--green:#22c55e;

--danger:#ef4444;

}



body{

font-family:'Poppins',sans-serif;

background:#020617;

color:white;

min-height:100vh;

}





.background{

position:fixed;

inset:0;

z-index:-1;

background:

radial-gradient(circle at top left,#2563eb,transparent 35%),

radial-gradient(circle at bottom right,#7c3aed,transparent 35%),

#020617;

}





/* Header */


.header{

display:flex;

justify-content:space-between;

align-items:center;

padding:30px 8%;

}



.header h1{

font-size:35px;

}



.header button{

padding:13px 22px;

border:none;

border-radius:12px;

background:var(--primary);

color:white;

font-weight:600;

cursor:pointer;

}





/* Container */


.container{

width:90%;

max-width:1000px;

margin:auto;

}







/* Cards */


.card{

background:

rgba(15,23,42,.75);

backdrop-filter:blur(20px);

padding:30px;

border-radius:25px;

margin:25px 0;

border:1px solid rgba(255,255,255,.08);

box-shadow:0 20px 40px rgba(0,0,0,.3);

}



.card h2{

margin-bottom:20px;

color:var(--primary);

}







/* Inputs */


input{

width:100%;

padding:15px;

margin:10px 0;

background:#0f172a;

border:none;

border-radius:14px;

color:white;

font-size:16px;

}






/* Buttons */


button{

padding:13px 22px;

border:none;

border-radius:14px;

background:

linear-gradient(

135deg,

var(--primary),

var(--purple)

);

color:white;

font-weight:700;

cursor:pointer;

transition:.3s;

}



button:hover{

transform:translateY(-3px);

}





/* Group Info */


.group-box{

background:#0f172a;

padding:20px;

border-radius:20px;

}



.group-box h3{

color:var(--gold);

font-size:25px;

}







/* Leaderboard */


.member-card{

display:flex;

justify-content:space-between;

align-items:center;

background:#0f172a;

padding:18px;

border-radius:18px;

margin-top:12px;

}





.member-card:first-child{

border:2px solid var(--gold);

}



.member-name{

font-weight:700;

}



.member-hours{

color:var(--primary);

}





/* Owner Badge */


.owner-badge{

background:var(--gold);

color:black;

padding:6px 14px;

border-radius:20px;

font-weight:700;

}







/* Rules */


#groupRules li{

margin:12px;

color:#cbd5e1;

}







/* Admin Panel */


.admin-panel{

border:1px solid var(--gold);

}



.admin-btn{

background:var(--green);

margin:5px;

}



.delete-btn{

background:var(--danger);

}







/* Mobile */


@media(max-width:700px){


.header{

flex-direction:column;

gap:20px;

text-align:center;

}



.header h1{

font-size:28px;

}



.member-card{

flex-direction:column;

gap:10px;

}


}
/* ==================================
   BABY STUDY PROJECT
   group.js
   Module 11C
================================== */


let currentUser=null;

let currentGroup=null;



const OWNER_CODE_LENGTH=6;






// Authentication

firebase.auth()
.onAuthStateChanged(user=>{


if(!user){

location.href="index.html";

return;

}



currentUser=user;


loadMyGroup();


});









// ================================
// CREATE GROUP
// ================================


document
.getElementById("createGroup")
?.addEventListener(
"click",
async()=>{


let name =
document.getElementById(
"groupName"
).value.trim();



if(!name){

alert(
"Enter group name"
);

return;

}



let groupCode =
generateGroupID();





await db.collection(
"groups"
)
.doc(groupCode)
.set({

name:name,


ownerUID:
currentUser.uid,


adminUID:[currentUser.uid],



members:[{

uid:
currentUser.uid,

role:
"owner",

studyHours:0

}],



requests:[],



rules:[

"Complete daily target",

"Respect members"

],



createdAt:

firebase.firestore.FieldValue
.serverTimestamp()


});



await db.collection(
"users"
)
.doc(currentUser.uid)
.update({

groupID:
groupCode


});



alert(
"Group Created 🔥\nID: "+groupCode
);



loadMyGroup();


});









// ================================
// JOIN REQUEST
// ================================


document
.getElementById("joinGroup")
?.addEventListener(
"click",
async()=>{


let id =
document.getElementById(
"groupID"
).value.trim();



if(!id)
return;



await db.collection(
"groups"
)
.doc(id)
.update({

requests:

firebase.firestore.FieldValue
.arrayUnion({

uid:
currentUser.uid,

status:
"pending"

})

});



alert(
"Request Sent ✅"
);


});








// ================================
// LOAD GROUP
// ================================


async function loadMyGroup(){


let userSnap =
await db.collection(
"users"
)
.doc(currentUser.uid)
.get();



let data =
userSnap.data();



if(!data.groupID)
return;



let snap =
await db.collection(
"groups"
)
.doc(data.groupID)
.get();



if(!snap.exists)
return;



currentGroup=snap.data();



displayGroup();


}







function displayGroup(){



document.getElementById(
"groupInfo"
).innerHTML=`

<div class="group-box">

<h3>

${currentGroup.name}

</h3>


<p>

Group ID:
${currentGroup.id || "Hidden"}

</p>


<p>

Members:
${currentGroup.members.length}

</p>


</div>

`;



loadMembers();


}





// ================================
// MEMBERS LEADERBOARD
// ================================


function loadMembers(){



let box =
document.getElementById(
"memberList"
);



box.innerHTML="";



let members =
currentGroup.members || [];



members.sort(
(a,b)=>
b.studyHours-a.studyHours
);



members.forEach(
(member,index)=>{


box.innerHTML +=`

<div class="member-card">


<div>

${index+1}.
${member.username || "Student"}

</div>


<div class="member-hours">

${member.studyHours || 0}h

</div>


</div>

`;



});



}








// ================================
// GENERATE GROUP ID
// ================================


function generateGroupID(){


let chars =
"ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789";


let result="";



for(
let i=0;
i<OWNER_CODE_LENGTH;
i++
){


result +=

chars.charAt(

Math.floor(
Math.random()*chars.length
)

);


}



return result;


}
/* ==================================
   BABY STUDY PROJECT
   groupAdmin.js
   Module 11D
================================== */


let adminUser=null;

let activeGroupID=null;



firebase.auth()
.onAuthStateChanged(user=>{


if(!user)
return;


adminUser=user;


loadAdminGroup();


});







// ================================
// LOAD ADMIN GROUP
// ================================


async function loadAdminGroup(){



let userSnap =
await db.collection("users")
.doc(adminUser.uid)
.get();



let user =
userSnap.data();



activeGroupID =
user.groupID;



if(!activeGroupID)
return;



let groupSnap =
await db.collection("groups")
.doc(activeGroupID)
.get();



let group =
groupSnap.data();



if(

group.ownerUID !== adminUser.uid &&

!group.adminUID.includes(adminUser.uid)

){

return;

}



showRequests(group);



}








// ================================
// SHOW REQUESTS
// ================================


function showRequests(group){



let box =
document.getElementById(
"adminControls"
);



box.innerHTML="";



group.requests.forEach(
(req,index)=>{


box.innerHTML +=`

<div class="member-card">


<p>

Request:
${req.uid}

</p>


<button onclick="approveMember(${index})">

Accept

</button>



<button onclick="rejectMember(${index})">

Reject

</button>


</div>

`;



});



}








// ================================
// APPROVE MEMBER
// ================================


async function approveMember(index){


let ref =
db.collection("groups")
.doc(activeGroupID);



let snap =
await ref.get();



let group =
snap.data();



let request =
group.requests[index];



let userSnap =
await db.collection("users")
.doc(request.uid)
.get();



let user =
userSnap.data();



group.members.push({

uid:
request.uid,

username:
user.username,

babyID:
user.babyID,

role:
"member",

studyHours:0


});



group.requests.splice(index,1);



await ref.update({

members:
group.members,

requests:
group.requests


});



await db.collection("users")
.doc(request.uid)
.update({

groupID:
activeGroupID


});



alert(
"Member Added ✅"
);


loadAdminGroup();


}









// ================================
// REJECT REQUEST
// ================================


async function rejectMember(index){



let ref =
db.collection("groups")
.doc(activeGroupID);



let snap =
await ref.get();



let group =
snap.data();



group.requests.splice(index,1);



await ref.update({

requests:
group.requests

});



loadAdminGroup();


}








// ================================
// EDIT RULES
// ================================


async function editRules(){


let rule =
prompt(
"Enter new rule"
);



if(!rule)
return;



await db.collection("groups")
.doc(activeGroupID)
.update({

rules:

firebase.firestore.FieldValue
.arrayUnion(rule)

});



alert(
"Rule Added 📜"
);


}








// ================================
// PROMOTE ADMIN
// ================================


async function promoteAdmin(uid){



await db.collection("groups")
.doc(activeGroupID)
.update({

adminUID:

firebase.firestore.FieldValue
.arrayUnion(uid)

});



alert(
"Admin Promoted 👑"
);


}








// ================================
// DELETE GROUP
// ================================


async function deleteGroup(){



let confirmDelete =
confirm(
"Delete this group permanently?"
);



if(!confirmDelete)
return;



await db.collection("groups")
.doc(activeGroupID)
.delete();



alert(
"Group Deleted"
);



location.href=
"dashboard.html";


}
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">


<title>BabyStudy Leaderboard</title>


<link rel="stylesheet" href="leaderboard.css">


<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">


<script defer src="firebase.js"></script>

<script defer src="leaderboard.js"></script>


</head>


<body>


<div class="background"></div>





<header class="header">


<h1>
🏆 Leaderboard
</h1>


<button onclick="location.href='dashboard.html'">

← Dashboard

</button>


</header>







<main class="container">






<!-- Filters -->

<section class="card">


<h2>
📊 Ranking Category
</h2>



<div class="filter-grid">


<button id="hoursBtn">

⏱ Study Hours

</button>



<button id="xpBtn">

⭐ XP

</button>



<button id="streakBtn">

🔥 Streak

</button>



<button id="problemBtn">

📚 Problems

</button>


</div>



</section>








<!-- Time Filter -->


<section class="card">


<h2>
📅 Duration
</h2>



<select id="timeFilter">


<option value="daily">

Today

</option>


<option value="weekly">

This Week

</option>


<option value="monthly">

This Month

</option>


<option value="all">

All Time

</option>


</select>



</section>









<!-- Top 3 -->


<section class="card">


<h2>
👑 Top Performers
</h2>



<div id="topThree">


Loading...

</div>



</section>









<!-- Full Ranking -->


<section class="card">


<h2>
🏅 Rankings
</h2>



<div id="leaderboardList">


Loading...

</div>



</section>









<!-- My Rank -->


<section class="card">


<h2>
🎯 My Position
</h2>



<div id="myRank">


Calculating...

</div>



</section>






</main>



</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   leaderboard.css
   Module 12B
================================== */


*{

margin:0;

padding:0;

box-sizing:border-box;

}



:root{

--primary:#38bdf8;

--purple:#8b5cf6;

--gold:#facc15;

--silver:#cbd5e1;

--bronze:#cd7f32;

}



body{

font-family:'Poppins',sans-serif;

background:#020617;

color:white;

min-height:100vh;

}





.background{

position:fixed;

inset:0;

z-index:-1;

background:

radial-gradient(circle at top left,#2563eb,transparent 35%),

radial-gradient(circle at bottom right,#7c3aed,transparent 35%),

#020617;

}





/* Header */


.header{

display:flex;

justify-content:space-between;

align-items:center;

padding:30px 8%;

}



.header h1{

font-size:35px;

}



.header button{

padding:13px 22px;

border:none;

border-radius:12px;

background:var(--primary);

color:white;

font-weight:600;

cursor:pointer;

}





/* Container */


.container{

width:90%;

max-width:1000px;

margin:auto;

}






/* Cards */


.card{

background:

rgba(15,23,42,.75);

backdrop-filter:blur(20px);

padding:30px;

border-radius:25px;

margin:25px 0;

border:1px solid rgba(255,255,255,.08);

}





/* Filters */


.filter-grid{

display:grid;

grid-template-columns:

repeat(auto-fit,minmax(160px,1fr));

gap:15px;

}



button{

padding:14px 22px;

border:none;

border-radius:15px;

background:

linear-gradient(

135deg,

var(--primary),

var(--purple)

);

color:white;

font-weight:700;

cursor:pointer;

}





select{

width:100%;

padding:15px;

border:none;

border-radius:15px;

background:#0f172a;

color:white;

font-size:16px;

}





/* Top Three */


.top-card{

display:flex;

align-items:center;

justify-content:space-between;

padding:20px;

background:#0f172a;

border-radius:20px;

margin-top:15px;

}





.rank-1{

border:2px solid var(--gold);

transform:scale(1.03);

}



.rank-2{

border:2px solid var(--silver);

}



.rank-3{

border:2px solid var(--bronze);

}




.medal{

font-size:35px;

}





/* Leaderboard List */


.rank-item{

display:flex;

justify-content:space-between;

align-items:center;

background:#0f172a;

padding:18px;

border-radius:18px;

margin-top:12px;

}



.rank-number{

font-size:25px;

font-weight:700;

color:var(--primary);

}



.player-name{

font-weight:600;

}



.player-score{

color:#22c55e;

}





/* My Rank */


#myRank{

background:#0f172a;

padding:25px;

border-radius:20px;

font-size:22px;

text-align:center;

color:var(--gold);

}







/* Mobile */


@media(max-width:700px){


.header{

flex-direction:column;

gap:20px;

text-align:center;

}



.header h1{

font-size:28px;

}



.top-card,
.rank-item{

flex-direction:column;

gap:10px;

}



}
/* ==================================
   BABY STUDY PROJECT
   leaderboard.js
   Module 12C
================================== */


let currentUser=null;

let rankingType="hours";

let timeRange="all";

let users=[];





// Authentication

firebase.auth()
.onAuthStateChanged(user=>{


if(!user)
return;


currentUser=user;


loadLeaderboard();


});







// ================================
// Buttons
// ================================


document
.getElementById("hoursBtn")
?.addEventListener(
"click",
()=>{

rankingType="hours";

loadLeaderboard();

});



document
.getElementById("xpBtn")
?.addEventListener(
"click",
()=>{

rankingType="xp";

loadLeaderboard();

});



document
.getElementById("streakBtn")
?.addEventListener(
"click",
()=>{

rankingType="streak";

loadLeaderboard();

});



document
.getElementById("problemBtn")
?.addEventListener(
"click",
()=>{

rankingType="problems";

loadLeaderboard();

});





document
.getElementById("timeFilter")
?.addEventListener(
"change",
e=>{

timeRange=e.target.value;

loadLeaderboard();

});








// ================================
// Load Users
// ================================


async function loadLeaderboard(){



let snap =
await db.collection("users")
.get();



users=[];



snap.forEach(doc=>{


let data=doc.data();


users.push({

id:doc.id,

username:
data.username || "Student",


xp:
data.xp || 0,


hours:
data.totalHours || 0,


streak:
data.streak || 0,


problems:
data.problemsSolved || 0


});


});



sortUsers();


displayTopThree();


displayRanking();


showMyRank();



}









// ================================
// Sort Ranking
// ================================


function sortUsers(){



users.sort((a,b)=>{


return b[rankingType]-a[rankingType];


});


}








// ================================
// Top Three
// ================================


function displayTopThree(){


let box =
document.getElementById(
"topThree"
);



box.innerHTML="";



let medals=[
"🥇",
"🥈",
"🥉"
];



users.slice(0,3)
.forEach((user,index)=>{


box.innerHTML +=`

<div class="top-card rank-${index+1}">


<div class="medal">

${medals[index]}

</div>


<div>

<h3>

${user.username}

</h3>


<p>

${user[rankingType]}

</p>


</div>


</div>

`;


});


}








// ================================
// Full Ranking
// ================================


function displayRanking(){


let box =
document.getElementById(
"leaderboardList"
);



box.innerHTML="";



users.forEach(
(user,index)=>{


box.innerHTML +=`

<div class="rank-item">


<div>


<span class="rank-number">

#${index+1}

</span>


${user.username}


</div>



<div class="player-score">

${user[rankingType]}

</div>



</div>

`;


});


}








// ================================
// My Rank
// ================================


function showMyRank(){


let position =
users.findIndex(
u=>u.id===currentUser.uid
);



document.getElementById(
"myRank"
)
.innerHTML=


`

Your Rank:

🏆 #${position+1}

<br>

Score:

${users[position]?.[rankingType] || 0}

`;



}
/* ==================================
   BABY STUDY PROJECT
   rankingAutomation.js
   Module 12D
================================== */


const OWNER_UID =
"YOUR_OWNER_UID";





// ================================
// WEEKLY RESET CHECK
// ================================


async function weeklyReset(){


let today =
new Date();



let day =
today.getDay();



// Sunday reset

if(day !== 0)
return;



let snapshot =
await db.collection("users")
.orderBy(
"weeklyHours",
"desc"
)
.limit(3)
.get();



let winners=[];



snapshot.forEach(doc=>{


winners.push({

uid:doc.id,

username:
doc.data().username,

score:
doc.data().weeklyHours || 0


});


});



await saveRankHistory(
"weekly",
winners
);



giveRewards(
winners,
"Weekly Champion"
);



resetWeeklyStats();


}







// ================================
// MONTHLY CHAMPION
// ================================


async function monthlyChampion(){


let date =
new Date();



if(date.getDate() !== 1)
return;



let snapshot =
await db.collection("users")
.orderBy(
"totalHours",
"desc"
)
.limit(1)
.get();



let champion =
snapshot.docs[0];



if(!champion)
return;



await db.collection("users")
.doc(champion.id)
.update({

badges:

firebase.firestore.FieldValue
.arrayUnion(
"Monthly Champion 🏆"
)

});



}








// ================================
// SAVE RANK HISTORY
// ================================


async function saveRankHistory(
type,
winners
){



await db.collection(
"rankHistory"
)
.add({

type:type,

winners:winners,

date:

firebase.firestore.FieldValue
.serverTimestamp()


});



}








// ================================
// REWARDS
// ================================


async function giveRewards(
players,
badge
){



let rewards=[
500,
300,
200
];



for(
let i=0;
i<players.length;
i++
){


await db.collection("users")
.doc(players[i].uid)
.update({

xp:

firebase.firestore.FieldValue
.increment(
rewards[i]
),


badges:

firebase.firestore.FieldValue
.arrayUnion(
badge
)


});


}



}








// ================================
// RESET WEEKLY DATA
// ================================


async function resetWeeklyStats(){



let users =
await db.collection("users")
.get();



let batch =
db.batch();



users.forEach(doc=>{


batch.update(

doc.ref,

{

weeklyHours:0,

weeklyXP:0

}

);


});



await batch.commit();


}







// ================================
// AUTO RUN DAILY
// ================================


setInterval(()=>{


weeklyReset();

monthlyChampion();


},


86400000
);
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">


<title>BabyStudy AI Assistant</title>


<link rel="stylesheet" href="aiAssistant.css">


<script defer src="firebase.js"></script>

<script defer src="aiAssistant.js"></script>


</head>


<body>


<div class="background"></div>





<header class="header">


<h1>
🤖 AI Study Assistant
</h1>


<button onclick="location.href='dashboard.html'">

← Dashboard

</button>


</header>







<main class="container">





<!-- AI Profile -->

<section class="card ai-card">


<div class="ai-icon">

🤖

</div>


<h2>

Study Mentor AI

</h2>


<p>

Your personal JEE preparation assistant

</p>


</section>









<!-- Quick Actions -->

<section class="card">


<h2>
⚡ Quick Help
</h2>



<div class="action-grid">


<button id="planStudy">

📅 Make Study Plan

</button>


<button id="analyse">

📊 Analyse Progress

</button>


<button id="revision">

🔄 Revision Plan

</button>


<button id="motivation">

🔥 Motivation

</button>


</div>


</section>








<!-- Chat -->


<section class="card">


<h2>
💬 Ask AI
</h2>



<div id="chatBox">

<div class="ai-message">

Hello! How can I help with your studies?

</div>

</div>





<div class="input-area">


<input 
id="userInput"
placeholder="Ask your study question...">


<button id="sendMessage">

Send

</button>



</div>



</section>








<!-- Suggestions -->


<section class="card">


<h2>
🎯 AI Recommendations
</h2>


<div id="recommendations">

Loading...

</div>


</section>






</main>


</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   aiAssistant.css
   Module 13B
================================== */


*{

margin:0;
padding:0;
box-sizing:border-box;

}



:root{

--primary:#38bdf8;

--purple:#8b5cf6;

--green:#22c55e;

}



body{

font-family:'Poppins',sans-serif;

background:#020617;

color:white;

min-height:100vh;

}





.background{

position:fixed;

inset:0;

z-index:-1;

background:

radial-gradient(circle at top left,#2563eb,transparent 35%),

radial-gradient(circle at bottom right,#7c3aed,transparent 35%),

#020617;

}





/* Header */


.header{

display:flex;

justify-content:space-between;

align-items:center;

padding:30px 8%;

}



.header h1{

font-size:35px;

}



.header button{

padding:13px 22px;

border:none;

border-radius:12px;

background:var(--primary);

color:white;

font-weight:600;

cursor:pointer;

}







/* Container */


.container{

width:90%;

max-width:1000px;

margin:auto;

}





/* Cards */


.card{

background:

rgba(15,23,42,.75);

backdrop-filter:blur(20px);

padding:30px;

border-radius:25px;

margin:25px 0;

border:1px solid rgba(255,255,255,.08);

}





/* AI Profile */


.ai-card{

text-align:center;

}



.ai-icon{

height:100px;

width:100px;

margin:auto;

display:flex;

align-items:center;

justify-content:center;

font-size:55px;

border-radius:50%;

background:

linear-gradient(

135deg,

var(--primary),

var(--purple)

);

}








/* Actions */


.action-grid{

display:grid;

grid-template-columns:

repeat(auto-fit,minmax(200px,1fr));

gap:15px;

}



button{

padding:14px 22px;

border:none;

border-radius:15px;

background:

linear-gradient(

135deg,

var(--primary),

var(--purple)

);

color:white;

font-weight:700;

cursor:pointer;

transition:.3s;

}



button:hover{

transform:translateY(-3px);

}







/* Chat */


#chatBox{

height:350px;

overflow-y:auto;

background:#0f172a;

padding:20px;

border-radius:20px;

}





.ai-message,
.user-message{

max-width:80%;

padding:15px;

border-radius:18px;

margin:10px 0;

}



.ai-message{

background:#1e293b;

}



.user-message{

background:#2563eb;

margin-left:auto;

}







/* Input */


.input-area{

display:flex;

gap:10px;

margin-top:15px;

}



input{

flex:1;

padding:15px;

background:#0f172a;

border:none;

border-radius:15px;

color:white;

font-size:16px;

}






/* Recommendations */


.recommendation-card{

background:#0f172a;

padding:18px;

border-radius:18px;

margin-top:12px;

border-left:4px solid var(--green);

}







/* Mobile */


@media(max-width:700px){


.header{

flex-direction:column;

gap:20px;

text-align:center;

}



.header h1{

font-size:28px;

}



.input-area{

flex-direction:column;

}



}
/* ==================================
   BABY STUDY PROJECT
   aiAssistant.js
   Module 13C
================================== */


let currentUser=null;



firebase.auth()
.onAuthStateChanged(user=>{


if(!user)
return;


currentUser=user;


loadRecommendations();


});







// ================================
// Chat System
// ================================


document
.getElementById("sendMessage")
?.addEventListener(
"click",
()=>{


let input =
document.getElementById(
"userInput"
);



let message =
input.value.trim();



if(!message)
return;



addMessage(
message,
"user"
);



input.value="";



generateAIReply(
message
);


});








function addMessage(
text,
type
){


let box =
document.getElementById(
"chatBox"
);



let div =
document.createElement(
"div"
);



div.className =
type==="user"
?
"user-message"
:
"ai-message";



div.innerText=text;



box.appendChild(div);



box.scrollTop =
box.scrollHeight;


}







// ================================
// AI Reply Engine
// ================================


function generateAIReply(
message
){


let reply =
"";



message =
message.toLowerCase();





if(
message.includes("plan")
){


reply=
"Create a daily plan with lectures, revision and problem solving. Keep difficult topics in your peak focus hours.";

}


else if(
message.includes("revision")
){


reply=
"Use active recall + previous questions. Revise formulas daily and maintain short notes.";

}



else if(
message.includes("physics")
){


reply=
"Focus on concepts first, then solve HCV, Cengage and advanced problems.";

}



else if(
message.includes("chemistry")
){


reply=
"Maintain reaction notes for Organic Chemistry and revise mechanisms regularly.";

}



else if(
message.includes("math")
){


reply=
"Practice problems daily. Accuracy and speed improve through repeated solving.";

}



else{


reply=
"Stay consistent. Track your hours, complete daily targets and avoid distractions.";

}



setTimeout(()=>{


addMessage(
reply,
"ai"
);


},700);



}








// ================================
// Quick Actions
// ================================


document
.getElementById("planStudy")
?.addEventListener(
"click",
()=>{


addMessage(

"AI Plan: Complete lectures → DPP → Practice problems → Revision",

"ai"

);


});





document
.getElementById("analyse")
?.addEventListener(
"click",
()=>{


analyseProgress();


});






document
.getElementById("revision")
?.addEventListener(
"click",
()=>{


addMessage(

"Revision Strategy: Revise notes → Formula sheet → PYQ → Mistake analysis",

"ai"

);


});







document
.getElementById("motivation")
?.addEventListener(
"click",
()=>{


addMessage(

"Small daily progress creates extraordinary results. Focus on consistency 🔥",

"ai"

);


});







// ================================
// Progress Analysis
// ================================


async function analyseProgress(){



let snap =
await db.collection("users")
.doc(currentUser.uid)
.get();



let data =
snap.data();



let hours =
data.totalHours || 0;



let xp =
data.xp || 0;



addMessage(

`Your progress:
Study Hours: ${hours}
XP: ${xp}

Keep improving daily.`,

"ai"

);



}








// ================================
// Recommendations
// ================================


async function loadRecommendations(){


let box =
document.getElementById(
"recommendations"
);



box.innerHTML=`

<div class="recommendation-card">

📚 Complete pending lectures first

</div>


<div class="recommendation-card">

🔥 Maintain daily study streak

</div>


<div class="recommendation-card">

📝 Practice questions after every topic

</div>

`;



}
/* ==================================
   BABY STUDY PROJECT
   aiAdvanced.js
   Module 13D
================================== */


let aiUser=null;



firebase.auth()
.onAuthStateChanged(user=>{


if(!user)
return;


aiUser=user;


loadAIAnalysis();


});








// ================================
// SMART ANALYSIS
// ================================


async function loadAIAnalysis(){


let snap =
await db.collection("users")
.doc(aiUser.uid)
.get();



let data =
snap.data();



let analysis =
generateAnalysis(data);



showAIRecommendation(
analysis
);



}









// ================================
// AI RULE ENGINE
// ================================


function generateAnalysis(data){



let result=[];



let hours =
data.totalHours || 0;



let streak =
data.streak || 0;



let subjects =
data.studyData || {};






if(hours < 50){


result.push(

"Increase daily study consistency"

);


}



if(streak < 7){


result.push(

"Build a stronger study streak"

);


}



for(let sub in subjects){



if(
subjects[sub].hours < 10
){


result.push(

`Give more attention to ${sub}`

);


}


}





result.push(

"Practice previous year questions regularly"

);



return result;


}







// ================================
// DISPLAY AI TIPS
// ================================


function showAIRecommendation(
tips
){



let box =
document.getElementById(
"recommendations"
);



box.innerHTML="";



tips.forEach(
tip=>{


box.innerHTML +=`

<div class="recommendation-card">

🤖 ${tip}

</div>

`;


});


}









// ================================
// SMART TIMETABLE
// ================================


function generateTimetable(
hours
){



let plan=[];



if(hours>=12){


plan=[

"Physics Concept + Problems",

"Chemistry Revision",

"Maths Advanced Practice"

];


}

else{


plan=[

"Complete Lectures",

"Practice Questions",

"Revision"

];


}



return plan;


}








// ================================
// AI STUDY PLAN BUTTON
// ================================


document
.getElementById("planStudy")
?.addEventListener(
"click",
async()=>{


let snap =
await db.collection("users")
.doc(aiUser.uid)
.get();



let data =
snap.data();



let plan =
generateTimetable(
data.dailyGoal || 8
);



addMessage(

"AI Plan:\n\n"+
plan.join("\n"),

"ai"

);



});
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">


<title>Admin Security Panel</title>


<link rel="stylesheet" href="securityAdmin.css">


<script defer src="firebase.js"></script>

<script defer src="securityAdmin.js"></script>


</head>


<body>


<div class="background"></div>




<header class="header">


<h1>
👑 Admin Security Panel
</h1>


<button onclick="location.href='dashboard.html'">

← Dashboard

</button>


</header>







<main class="container">





<!-- Admin Profile -->


<section class="card">


<h2>
🛡️ Admin Access
</h2>



<div id="adminStatus">

Checking permissions...

</div>



</section>








<!-- User Management -->


<section class="card">


<h2>
👥 User Management
</h2>



<div class="action-grid">


<button id="viewUsers">

View Users

</button>


<button id="banUser">

Restrict User

</button>


<button id="removeUser">

Remove User

</button>


</div>



</section>








<!-- Permission Control -->


<section class="card">


<h2>
🔐 Permission Control
</h2>



<div id="permissionList">


Loading permissions...

</div>



</section>








<!-- Activity Logs -->


<section class="card">


<h2>
📋 Activity Logs
</h2>



<div id="activityLogs">

Loading logs...

</div>



</section>








<!-- System Controls -->


<section class="card">


<h2>
⚙️ System Controls
</h2>



<button id="maintenance">

Enable Maintenance Mode

</button>



<button id="backup">

Create Data Backup

</button>



</section>






</main>



</body>

</html>
/* ==================================
   BABY STUDY PROJECT
   securityAdmin.css
   Module 15B
================================== */


*{

margin:0;
padding:0;
box-sizing:border-box;

}



:root{

--primary:#38bdf8;

--purple:#8b5cf6;

--red:#ef4444;

--green:#22c55e;

--gold:#facc15;

}



body{

font-family:'Poppins',sans-serif;

background:#020617;

color:white;

min-height:100vh;

}





.background{

position:fixed;

inset:0;

z-index:-1;

background:

radial-gradient(circle at top left,#1d4ed8,transparent 35%),

radial-gradient(circle at bottom right,#7c3aed,transparent 35%),

#020617;

}







/* Header */


.header{

display:flex;

justify-content:space-between;

align-items:center;

padding:30px 8%;

}



.header h1{

font-size:34px;

}



.header button{

padding:13px 22px;

border:none;

border-radius:12px;

background:var(--primary);

color:white;

font-weight:700;

cursor:pointer;

}







/* Container */


.container{

width:90%;

max-width:1100px;

margin:auto;

}







/* Cards */


.card{

background:

rgba(15,23,42,.8);

backdrop-filter:blur(20px);

border-radius:25px;

padding:30px;

margin:25px 0;

border:1px solid rgba(255,255,255,.08);

box-shadow:

0 20px 40px rgba(0,0,0,.35);

}





.card h2{

color:var(--primary);

margin-bottom:20px;

}







/* Buttons */


button{

padding:14px 22px;

border:none;

border-radius:15px;

background:

linear-gradient(

135deg,

var(--primary),

var(--purple)

);

color:white;

font-weight:700;

cursor:pointer;

margin:5px;

transition:.3s;

}



button:hover{

transform:translateY(-3px);

}





#banUser,
#removeUser{

background:var(--red);

}



#maintenance{

background:var(--gold);

color:black;

}



#backup{

background:var(--green);

}








/* Action Grid */


.action-grid{

display:grid;

grid-template-columns:

repeat(auto-fit,minmax(200px,1fr));

gap:15px;

}








/* Admin Status */


.status-box{

padding:20px;

border-radius:20px;

background:#0f172a;

border-left:5px solid var(--green);

}



.status-danger{

border-left-color:var(--red);

}







/* Permission List */


.permission-item{

display:flex;

justify-content:space-between;

align-items:center;

background:#0f172a;

padding:18px;

border-radius:18px;

margin-top:12px;

}



.permission-on{

color:var(--green);

font-weight:700;

}



.permission-off{

color:var(--red);

font-weight:700;

}








/* Logs */


.log-item{

background:#0f172a;

padding:15px;

border-radius:15px;

margin-top:10px;

color:#cbd5e1;

border-left:4px solid var(--primary);

}








/* Warning */


.warning{

background:

rgba(239,68,68,.15);

border:1px solid var(--red);

padding:20px;

border-radius:20px;

}








/* Mobile */


@media(max-width:700px){


.header{

flex-direction:column;

gap:20px;

text-align:center;

}



.header h1{

font-size:27px;

}



.permission-item{

flex-direction:column;

gap:10px;

}



}
/* ==================================
   BABY STUDY PROJECT
   securityAdmin.js
   Module 15C
================================== */


let adminUser = null;

let adminRole = null;





const OWNER_UID =
"YOUR_OWNER_UID";







// ================================
// AUTH CHECK
// ================================


firebase.auth()
.onAuthStateChanged(async user=>{


if(!user){

location.href="index.html";

return;

}


adminUser=user;


checkAdminAccess();


});









// ================================
// VERIFY ROLE
// ================================


async function checkAdminAccess(){


let snap =
await db.collection("users")
.doc(adminUser.uid)
.get();



let data =
snap.data();



adminRole =
data.role || "user";




if(

adminUser.uid === OWNER_UID

){

adminRole="owner";

}





if(
adminRole==="owner" ||
adminRole==="admin"
){


document.getElementById(
"adminStatus"
).innerHTML=

`

<div class="status-box">

✅ Access Granted

<br>

Role:
${adminRole}

</div>

`;



loadLogs();


}

else{


document.getElementById(
"adminStatus"
).innerHTML=

`

<div class="warning">

❌ Access Denied

</div>

`;



}






}









// ================================
// VIEW USERS
// ================================


document
.getElementById("viewUsers")
?.addEventListener(
"click",
async()=>{


let snap =
await db.collection("users")
.get();



let box =
document.getElementById(
"permissionList"
);



box.innerHTML="";



snap.forEach(doc=>{


let user =
doc.data();



box.innerHTML +=`

<div class="permission-item">


<span>

${user.username || "Student"}

</span>


<span>

${user.role || "user"}

</span>


</div>

`;


});


});









// ================================
// RESTRICT USER
// ================================


document
.getElementById("banUser")
?.addEventListener(
"click",
async()=>{


let uid =
prompt(
"Enter User ID"
);



if(!uid)
return;



await db.collection("users")
.doc(uid)
.update({

status:"restricted"

});



createLog(
"Restricted user: "+uid
);



alert(
"User restricted"
);



});









// ================================
// REMOVE USER
// ================================


document
.getElementById("removeUser")
?.addEventListener(
"click",
async()=>{


let uid =
prompt(
"Enter User ID"
);



if(!uid)
return;



await db.collection("users")
.doc(uid)
.delete();



createLog(
"Removed user: "+uid
);



alert(
"User removed"
);



});








// ================================
// ACTIVITY LOG
// ================================


async function createLog(
action
){



await db.collection(
"activityLogs"
)
.add({

action:action,


admin:
adminUser.uid,


time:

firebase.firestore.FieldValue
.serverTimestamp()


});



}








async function loadLogs(){



let snap =
await db.collection(
"activityLogs"
)
.orderBy(
"time",
"desc"
)
.limit(20)
.get();



let box =
document.getElementById(
"activityLogs"
);



box.innerHTML="";



snap.forEach(doc=>{


let log =
doc.data();



box.innerHTML +=`

<div class="log-item">

${log.action}

</div>

`;



});


}








// ================================
// MAINTENANCE MODE
// ================================


document
.getElementById("maintenance")
?.addEventListener(
"click",
async()=>{


await db.collection(
"settings"
)
.doc("system")
.update({

maintenance:true

});



createLog(
"Enabled maintenance mode"
);



alert(
"Maintenance Enabled"
);


});









// ================================
// BACKUP REQUEST
// ================================


document
.getElementById("backup")
?.addEventListener(
"click",
()=>{


createLog(
"Backup requested"
);



alert(
"Backup process started"
);


});
rules_version = '2';

service cloud.firestore {

  match /databases/{database}/documents {


    // USER DATA
    match /users/{userId} {


      // User can read/write own profile
      allow read, write:
      if request.auth != null
      && request.auth.uid == userId;


      // Admin/Owner access
      allow read, write:
      if isAdmin();

    }





    // GROUP SYSTEM
    match /groups/{groupId} {


      allow read:
      if request.auth != null;



      allow create:
      if request.auth != null;



      // Owner/Admin can edit group
      allow update, delete:
      if isGroupAdmin(groupId);


    }








    // NOTIFICATIONS

    match /notifications/{notificationId} {


      allow read:
      if request.auth != null
      && resource.data.userID ==
      request.auth.uid;



      allow write:
      if isAdmin();


    }








    // ANNOUNCEMENTS


    match /announcements/{id} {


      allow read:
      if request.auth != null;



      allow write:
      if isAdmin();


    }








    // ACTIVITY LOGS


    match /activityLogs/{id} {


      allow read:
      if isAdmin();



      allow create:
      if isAdmin();


    }








    // SETTINGS


    match /settings/{id} {


      allow read:
      if request.auth != null;



      allow write:
      if isOwner();


    }







    // FUNCTIONS


    function isAdmin(){


      return request.auth != null
      &&
      (
      get(
      /databases/$(database)/documents/users/$(request.auth.uid)
      ).data.role == "admin"

      ||

      get(
      /databases/$(database)/documents/users/$(request.auth.uid)
      ).data.role == "owner"

      );

    }







    function isOwner(){


      return request.auth != null

      &&

      get(
      /databases/$(database)/documents/users/$(request.auth.uid)
      ).data.role == "owner";


    }







    function isGroupAdmin(groupId){


      return request.auth != null

      &&

      request.auth.uid in

      get(
      /databases/$(database)/documents/groups/$(groupId)
      ).data.adminUID;


    }


  }

}
