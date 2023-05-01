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
<MainContent />

