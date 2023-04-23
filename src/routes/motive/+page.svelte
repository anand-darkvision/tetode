<script>
  import NavBar from "./../../Pages/NavBar.svelte";
  import image1 from "../../Assets/1.jpg";
  import image2 from "../../Assets/2.jpg";
  import image3 from "../../Assets/3.jpg";
</script>

<NavBar />

<div class="content1">
  <p class="content-text">Build Your Ideas From Tetode</p>
</div>
<hr style="margin-top: 7%;margin-bottom: 0;" />
<div style="margin:0px">
  <div class="row">
    <div class="col-6 content2">
      <p>
        Tetode is a dynamic platform that fosters creativity, collaboration, and
        knowledge-sharing among a global community. It provides a space for
        individuals to bring their ideas to life, engage with like-minded peers,
        and receive valuable feedback to help them grow. Whether you're a
        professional seeking to expand your network, or an aspiring creator
        looking to explore new opportunities, Tetode offers a supportive and
        inclusive environment to help you thrive. Join us today and unlock your
        potential.
      </p>
    </div>
    <div class="col-6" style="padding: 0px;">
      <div id="carouselExampleRide" class="carousel slide" data-bs-ride="true">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src={image1} class="d-block w-100" alt="...">
          </div>
          <div class="carousel-item">
            <img src={image2} class="d-block w-100" alt="...">
          </div>
          <div class="carousel-item">
            <img src={image3} class="d-block w-100" alt="...">
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleRide" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleRide" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </div>
  </div>
</div>
<hr style="margin-bottom: 0;margin-top: 0;" />

<style>
  @import url("https://fonts.googleapis.com/css2?family=Newsreader:wght@200&display=swap");

  hr {
    height: 0px;
    border: none;
    border-top: 2px solid black;
  }
  .content-text {
    color: black;
    font-size: 4vw;
    font-weight: 100;
    font-family: "Newsreader", serif;
  }
  .content1 {
    text-align: center;
    align-items: center;
    margin: 10% 0 0;
  }
  .content2 {
    border-style: solid;
    border-top: none;
    border-color: black;
    border-bottom: none;
    padding: 0;
  }
  .content2 p {
    padding-left: 5%;
    font-size: 1.8vw;
    color: #3c4048;
    font-weight: 300;
    font-family: "Newsreader", serif;
  }
  .carousel > .carousel-inner > .carousel-item > img {
    width: 200px; /* Yeap you can change the width and height*/
    height: 380px;
  }
</style>
