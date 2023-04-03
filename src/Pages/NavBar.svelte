<script>
  import Logo from "../Assets/logo_tranparent.png";
  import { onMount } from "svelte";

  let navBar;

  function handleScroll() {
    if (window.scrollY > 530) {
      navBar.style.backgroundColor = "white";
    } else if (window.scrollY > 0) {
      navBar.style.backgroundColor = "#FE6244";
    } else {
      navBar.style.backgroundColor = "white";
    }
  }

  onMount(() => {
    window.addEventListener("scroll", handleScroll);
  });
</script>

<nav
  class="navbar navbar-expand-lg navbar-light border-bottom navbar-default fixed-top"
  bind:this={navBar}
>
  <div class="container-fluid " style="padding-left: 5vw;">
    <img
      src={Logo}
      alt="Logo"
      width="200"
      height="60"
      style="padding-bottom: 1%;"
    />
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
        <a class="nav-link fs-5" href="#product " style="color: black;"
          >OUR MOTIVE</a
        >
      </li>
      <li class="nav-item">
        <a class=" nav-link fs-5" href="#testimonials" style="color: black;"
          >BE A MEMBER</a
        >
      </li>
      <li class="nav-item">
        <a
          class="nav-link fs-5"
          href="#history"
          style="color: black;padding-right:40px;">SIGN IN</a
        >
      </li>
    </ul>
  </div>
</nav>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200&display=swap");
  a {
    font-family: "Poppins", sans-serif;
    font-weight: 800;
  }
  a:hover {
    color: gray !important;
  }
  .navbar {
    background-color: transparent;
    transition: background-color 0.3s ease-in-out;
  }
</style>
