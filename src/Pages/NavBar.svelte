<script>
  import {
    GoogleAuthProvider,
    signInWithPopup,
    getAuth,
    onAuthStateChanged,
  } from "firebase/auth";
  import Logo from "../Assets/logo_tranparent.png";
  import { onMount } from "svelte";
  import { initializeApp } from "firebase/app";

  // firebase config

  let user = null;

  const firebaseConfig = {
    apiKey: "AIzaSyCBH-d34GR4q-qv3yWolY2yxc_rsUsyWcw",
    authDomain: "tetode-e3b08.firebaseapp.com",
    projectId: "tetode-e3b08",
    storageBucket: "tetode-e3b08.appspot.com",
    messagingSenderId: "972864826221",
    appId: "1:972864826221:web:74a2944c400f2121390864",
    measurementId: "G-H7PSVR6ZRH",
  };

  //initialize app

  const app = initializeApp(firebaseConfig);

  //login
  const login = () => {
    const auth = getAuth(app);
    signInWithPopup(auth, new GoogleAuthProvider());
  };
  //logout

  onMount(() => {
    const auth = getAuth(app);
    onAuthStateChanged(auth, (newuser) => {
      user = newuser;
    });
  });
  function on() {
    document.getElementById("overlay").style.display = "block";
  }

  function off() {
    document.getElementById("overlay").style.display = "none";
  }
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div id="overlay" on:click={off}>
  <div class="card">
    <div class="card-body">
      <h5 class="card-title text-center">Welcome Back</h5>
      <div
        class="loader"
        style="display: flex; justify-content: center;padding-top: 5%;"
      >
        <svg class="pl" width="240" height="240" viewBox="0 0 240 240">
          <circle
            class="pl__ring pl__ring--a"
            cx="120"
            cy="120"
            r="105"
            fill="none"
            stroke="#000"
            stroke-width="20"
            stroke-dasharray="0 660"
            stroke-dashoffset="-330"
            stroke-linecap="round"
          />
          <circle
            class="pl__ring pl__ring--b"
            cx="120"
            cy="120"
            r="35"
            fill="none"
            stroke="#000"
            stroke-width="20"
            stroke-dasharray="0 220"
            stroke-dashoffset="-110"
            stroke-linecap="round"
          />
          <circle
            class="pl__ring pl__ring--c"
            cx="85"
            cy="120"
            r="70"
            fill="none"
            stroke="#000"
            stroke-width="20"
            stroke-dasharray="0 440"
            stroke-linecap="round"
          />
          <circle
            class="pl__ring pl__ring--d"
            cx="155"
            cy="120"
            r="70"
            fill="none"
            stroke="#000"
            stroke-width="20"
            stroke-dasharray="0 440"
            stroke-linecap="round"
          />
        </svg>
      </div>
      <div style="padding-top: 2%%;display: flex;justify-content: center;">
        <a href="#ds" class="google btn" style="color:#FE6244" on:click={login}>
          <i class="fa fa-google fa-fw fs-4" /> Login with Google
        </a>
      </div>
      <a
        href="#er"
        class="forget"
        style="justify-content: center;display: flex;"
        >Having any TroubleShoot ? Don't Hesitate to Contact us</a
      >
      <div class="footer">
        <p
          style="font-size: 0.8em;  display: flex; justify-content: center;padding-top: 20%;color: gray;"
        >
          click signIn to agree the Tetode's <a class="tandc" href="#23"
            >Terms and Conditions</a
          >
        </p>
      </div>
    </div>
  </div>
</div>

<nav
  class="navbar navbar-expand-lg navbar-light border-bottom navbar-default fixed-top"
>
  <div class="container-fluid" style="padding-left: 5vw;">
    <a href="./" class="imge-link">
      <img
        src={Logo}
        alt="Logo"
        width="200"
        height="60"
        style="padding-bottom: 1%;"
      />
    </a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon" />
    </button>
  </div>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav ml-auto" style="width:max-content;">
      <li class="nav-item">
        <a class="nav-link fs-5" href="#header" style="color: black;">PUBLISH</a
        >
      </li>
      <li class="nav-item">
        <a class="nav-link fs-5" href="./motive" style="color: black;"
          >OUR MOTIVE</a
        >
      </li>
      <li class="nav-item">
        <a class=" nav-link fs-5" href="#testimonials" style="color: black;"
          >BE A MEMBER</a
        >
      </li>
      <li class="nav-item">
        <!-- svelte-ignore a11y-missing-attribute -->
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <a
          class="nav-link fs-5"
          on:click={on}
          style="color: black;padding-right:40px;">SIGN IN</a
        >
      </li>
    </ul>
  </div>
</nav>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200&display=swap");

  .card {
    width: 35%;
    height: 50%;
    border-radius: 20px;
  }
  /* Common styles for all screens */
  a {
    font-family: "Poppins", sans-serif;
    font-weight: 800;
  }

  a:hover {
    color: gray !important;
  }

  .navbar {
    background-color: white;
  }

  .google {
    font-size: 30px;
  }

  #overlay {
    position: fixed;
    display: none;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 2;
    cursor: pointer;
  }

  .card-title {
    font-family: "Poppins", sans-serif;
    padding-top: 6%;
    font-size: 22px;
  }

  .tandc {
    color: gray;
    padding-left: 1%;
  }

  .forget {
    text-decoration: none;
    color: gray;
    padding-top: 5%;
  }

  .forget:hover {
    text-decoration: underline;
  }

  .pl {
    width: 6em;
    height: 6em;
  }

  .pl__ring {
    animation: ringA 2s linear infinite;
  }

  .pl__ring--a {
    stroke: #f42f25;
  }

  .pl__ring--b {
    animation-name: ringB;
    stroke: #f49725;
  }

  .pl__ring--c {
    animation-name: ringC;
    stroke: #255ff4;
  }

  .pl__ring--d {
    animation-name: ringD;
    stroke: #f42582;
  }

  /* Common styles for screens with a width less than or equal to 600px */
  @media (max-width: 600px) {
    .card {
      position: absolute;
      top: 20%;
      left: 15%;
      width: 70% !important;
      height: 70% !important;
    }

    .card-title {
      font-size: 20px;
    }

    .pl {
      width: 3em;
      height: 3em;
    }

    .google {
      font-size: 20px;
    }
  }

  /* Styles for screens with a width between 601px and 1024px */
  @media (min-width: 601px) and (max-width: 1024px) {
    .card {
      position: absolute;
      top: 15%;
      left: 15%;
    }
  }

  /* Styles for screens with a width greater than 1024px */
  @media (min-width: 1025px) {
    .card {
      position: absolute;
      top: 22%;
      left: 32%;
    }
  }
  /* Animations */
  @keyframes ringA {
    from,
    4% {
      stroke-dasharray: 0 660;
      stroke-width: 20;
      stroke-dashoffset: -330;
    }

    12% {
      stroke-dasharray: 60 600;
      stroke-width: 30;
      stroke-dashoffset: -335;
    }

    32% {
      stroke-dasharray: 60 600;
      stroke-width: 30;
      stroke-dashoffset: -595;
    }

    40%,
    54% {
      stroke-dasharray: 0 660;
      stroke-width: 20;
      stroke-dashoffset: -660;
    }

    62% {
      stroke-dasharray: 60 600;
      stroke-width: 30;
      stroke-dashoffset: -665;
    }

    82% {
      stroke-dasharray: 60 600;
      stroke-width: 30;
      stroke-dashoffset: -925;
    }

    90%,
    to {
      stroke-dasharray: 0 660;
      stroke-width: 20;
      stroke-dashoffset: -990;
    }
  }

  @keyframes ringB {
    from,
    12% {
      stroke-dasharray: 0 220;
      stroke-width: 20;
      stroke-dashoffset: -110;
    }

    20% {
      stroke-dasharray: 20 200;
      stroke-width: 30;
      stroke-dashoffset: -115;
    }

    40% {
      stroke-dasharray: 20 200;
      stroke-width: 30;
      stroke-dashoffset: -195;
    }

    48%,
    62% {
      stroke-dasharray: 0 220;
      stroke-width: 20;
      stroke-dashoffset: -220;
    }

    70% {
      stroke-dasharray: 20 200;
      stroke-width: 30;
      stroke-dashoffset: -225;
    }

    90% {
      stroke-dasharray: 20 200;
      stroke-width: 30;
      stroke-dashoffset: -305;
    }

    98%,
    to {
      stroke-dasharray: 0 220;
      stroke-width: 20;
      stroke-dashoffset: -330;
    }
  }

  @keyframes ringC {
    from {
      stroke-dasharray: 0 440;
      stroke-width: 20;
      stroke-dashoffset: 0;
    }

    8% {
      stroke-dasharray: 40 400;
      stroke-width: 30;
      stroke-dashoffset: -5;
    }

    28% {
      stroke-dasharray: 40 400;
      stroke-width: 30;
      stroke-dashoffset: -175;
    }

    36%,
    58% {
      stroke-dasharray: 0 440;
      stroke-width: 20;
      stroke-dashoffset: -220;
    }

    66% {
      stroke-dasharray: 40 400;
      stroke-width: 30;
      stroke-dashoffset: -225;
    }

    86% {
      stroke-dasharray: 40 400;
      stroke-width: 30;
      stroke-dashoffset: -395;
    }

    94%,
    to {
      stroke-dasharray: 0 440;
      stroke-width: 20;
      stroke-dashoffset: -440;
    }
  }

  @keyframes ringD {
    from,
    8% {
      stroke-dasharray: 0 440;
      stroke-width: 20;
      stroke-dashoffset: 0;
    }

    16% {
      stroke-dasharray: 40 400;
      stroke-width: 30;
      stroke-dashoffset: -5;
    }

    36% {
      stroke-dasharray: 40 400;
      stroke-width: 30;
      stroke-dashoffset: -175;
    }

    44%,
    50% {
      stroke-dasharray: 0 440;
      stroke-width: 20;
      stroke-dashoffset: -220;
    }

    58% {
      stroke-dasharray: 40 400;
      stroke-width: 30;
      stroke-dashoffset: -225;
    }

    78% {
      stroke-dasharray: 40 400;
      stroke-width: 30;
      stroke-dashoffset: -395;
    }

    86%,
    to {
      stroke-dasharray: 0 440;
      stroke-width: 20;
      stroke-dashoffset: -440;
    }
  }
</style>
