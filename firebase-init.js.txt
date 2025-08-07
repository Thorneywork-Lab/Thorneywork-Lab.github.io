// firebase-init.js
const firebaseConfig = {
    apiKey: "AIzaSyAIhJFHk4fOgVZRADo5giS5rh-XpoGGJ7o",
    authDomain: "lab-intranet.firebaseapp.com",
    projectId: "lab-intranet",
    storageBucket: "lab-intranet.firebasestorage.app",
    messagingSenderId: "1007272743653",
    appId: "1:1007272743653:web:ffedfb9232bf4758a17a0c"
  };

firebase.initializeApp(firebaseConfig);
const auth = firebase.auth();

auth.onAuthStateChanged(user => {
  if (user) {
    document.getElementById("loginBtn").style.display = "none";
    document.getElementById("logoutBtn").style.display = "inline";
  } else {
    document.getElementById("loginBtn").style.display = "inline";
    document.getElementById("logoutBtn").style.display = "none";
  }
});
