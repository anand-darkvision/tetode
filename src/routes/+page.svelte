<script>
  import NewContent from "../Pages/NewContent.svelte";
  import Header from "../Pages/Header.svelte";
  import NavBar from "../Pages/NavBar.svelte";
  import MainContent from "../Pages/MainContent.svelte";

  function on() {
    document.getElementById("overlay").style.display = "block";
  }

  function off() {
    document.getElementById("overlay").style.display = "none";
  }
</script>

<NavBar />
<Header />
<NewContent />
<div class="main-content-container">
  <MainContent />
</div>

<style>
  .main-content-container {
    max-height: calc(98vh - 60px);
    overflow-y: auto;
    overflow-x: hidden;
  }
</style>
