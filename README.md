
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Abdullah Ola Tech Academy</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }body {
  scroll-behavior: smooth;
  background-color: #f4f8fc;
  color: #333;
}

header {
  background: #007BFF;
  color: white;
  padding: 2rem 1rem;
  text-align: center;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  background: #0056b3;
}

nav .logo {
  font-weight: bold;
  font-size: 1.5rem;
  color: white;
}

nav ul {
  list-style: none;
  display: flex;
  gap: 1rem;
}

nav ul li a {
  color: white;
  text-decoration: none;
}

section {
  padding: 3rem 1rem;
  text-align: center;
}

.auth-forms {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  max-width: 400px;
  margin: auto;
}

input {
  display: block;
  width: 100%;
  padding: 0.5rem;
  margin: 0.5rem 0;
}

button {
  padding: 0.6rem;
  background: #007BFF;
  border: none;
  color: white;
  cursor: pointer;
}

footer {
  background: #0056b3;
  color: white;
  text-align: center;
  padding: 1rem;
}

  </style>
  <script type="module">
    import { initializeApp } from 'https://www.gstatic.com/firebasejs/10.12.0/firebase-app.js';
    import { getAuth, createUserWithEmailAndPassword, signInWithEmailAndPassword } from 'https://www.gstatic.com/firebasejs/10.12.0/firebase-auth.js';const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};

const app = initializeApp(firebaseConfig);
const auth = getAuth(app);

window.signup = function () {
  const email = document.getElementById("signup-email").value;
  const password = document.getElementById("signup-password").value;

  createUserWithEmailAndPassword(auth, email, password)
    .then((userCredential) => {
      alert("Signup successful!");
    })
    .catch((error) => {
      alert("Signup failed: " + error.message);
    });
};

window.login = function () {
  const email = document.getElementById("login-email").value;
  const password = document.getElementById("login-password").value;

  signInWithEmailAndPassword(auth, email, password)
    .then((userCredential) => {
      alert("Login successful!");
    })
    .catch((error) => {
      alert("Login failed: " + error.message);
    });
};

  </script>
</head>
<body>
  <header>
    <nav>
      <div class="logo">Abdullah Ola Tech Academy</div>
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#auth">Login/Signup</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
    <div class="hero">
      <h1>Welcome to Abdullah Ola Tech Academy</h1>
      <p>Learn modern tech skills to transform your future!</p>
    </div>
  </header>  <section id="about">
    <h2>About Us</h2>
    <p>We are a premier academy teaching all tech skills including programming, cybersecurity, data science, and more.</p>
  </section>  <section id="skills">
    <h2>Tech Skills We Offer</h2>
    <ul>
      <li>Web Development</li>
      <li>Cybersecurity</li>
      <li>Data Science</li>
      <li>Mobile App Development</li>
      <li>UI/UX Design</li>
    </ul>
  </section>  <section id="auth">
    <h2>Login / Signup</h2>
    <div class="auth-forms">
      <div class="form">
        <h3>Login</h3>
        <input type="email" id="login-email" placeholder="Email" />
        <input type="password" id="login-password" placeholder="Password" />
        <button onclick="login()">Login</button>
      </div><div class="form">
    <h3>Signup</h3>
    <input type="email" id="signup-email" placeholder="Email" />
    <input type="password" id="signup-password" placeholder="Password" />
    <button onclick="signup()">Signup</button>
  </div>
</div>

  </section>  <section id="contact">
    <h2>Contact Us</h2>
    <p>📞 WhatsApp: <a href="https://wa.me/2348136311326">08136311326</a></p>
    <p>📧 Email: <a href="mailto:folabdullah8@gmail.com">folabdullah8@gmail.com</a></p>
  </section>  <footer>
    <p>&copy; 2025 Abdullah Ola Tech Academy</p>
  </footer>
</body>
</html>
