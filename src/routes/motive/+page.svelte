<script>
  import NavBar from "./../../Pages/NavBar.svelte";
  import image1 from "../../Assets/1.jpg";
  import image2 from "../../Assets/2.jpg";
  import image3 from "../../Assets/3.jpg";
  import Footer from "../../lib/footer.svelte";
  import MainImage from "../../Assets/logo_svg.svg";
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
      <div class="image">
        <img src={MainImage} alt="Tetode">
      </div>
    </div>
  </div>
</div>
<hr style="margin-bottom: 0;margin-top: 0;background-color: white;" />
<div class="content3">
  <p class="headerContent">
    We Provide the space to Work And Collabrate 
  </p>
  <p class="headerContent2">
    Your IDEAS
  </p>
  <p class="quotes" style="padding-top: 3%;">
      The more an idea is developed, the more concise becomes its expression;
  </p>
  <p class="quotes">
      the more a tree is pruned, the better is the fruit.
  </p>
  <p class="author">
    - Alfred Bougeart
  </p>
  <div class="butt" style="padding-bottom: 5%;">
    <button type="button" class="btn btn-outline-secondary" style="color:white;font-size:2vw;border-radius: 30px;">Write Your Ideas</button>
  </div>Alfred Bougear
</div>

<!-- footer -->
<Footer/>

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
    border-width: 2px;
    border-top: none;
    border-color: grey;
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
  .content3{
    max-width: 100%;
    max-height: 30%;
    background-color: #000;
    color: white;
    justify-content: center;
    text-align: center;
  }
  .headerContent{
    font-family: "Newsreader", serif;
    font-weight: 200;
    font-size: 5vw;
  }
  .headerContent2{
    font-family: "Newsreader", serif;
    font-weight: bolder;
    font-size:4.5vw
  }
  .quotes{
    font-family: "Newsreader", serif;
    font-weight: 800;
    font-size:2vw;
  }
  .author{
    font-family: "Newsreader", serif;
    padding-left: 40%;
    padding-top: 1%;
    font-size: large;
    font-weight: bolder;
  }
  .image{
    height:20vw;
  }
</style>
