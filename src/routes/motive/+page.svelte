<script>
  import NavBar from "./../../Pages/NavBar.svelte";
  import Footer from "../../lib/footer.svelte";
  import MainImage from "../../Assets/MainImage.svg";
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
  <p class="headerContent" style="padding-top:2%">
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
    <button type="button" class="btn btn-outline-secondary" style="font-size:2vw;border-radius: 30px;">Join Us Today</button>
  </div>
</div>
<hr style="margin-bottom: 0; margin-top: 0; background-color: white;"/>
<div class="content4">
  <p class="header">
    Read Our Latest Articles
  </p>
  <div class="container">
    <div class="row row-cols-2 row-cols-lg-2 g-5 g-lg-3">
      <div class="col">
        <div class="user">
          <button type="button" class="btn btn-outline-secondary" style="border-radius: 30px;">
            <img
            class="avatar"
            src="https://randomuser.me/api/portraits/men/77.jpg"
            alt="user"
          /> @adam123 "ChatGpt Cross Near...."</button>
        </div>
      </div>
      <div class="col">
        <div class="user">
          <button type="button" class="btn btn-outline-secondary" style="border-radius: 30px;">
            <img
            class="avatar"
            src="https://randomuser.me/api/portraits/men/77.jpg"
            alt="user"
          /> @adam123 "ChatGpt Cross Near...."</button>
        </div>
      </div>
      <div class="col">
        <div class="user">
          <button type="button" class="btn btn-outline-secondary" style="border-radius: 30px;">
            <img
            class="avatar"
            src="https://randomuser.me/api/portraits/men/77.jpg"
            alt="user"
          /> @adam123 "ChatGpt Cross Near...."</button>
        </div>
      </div>
      <div class="col">
        <div class="user">
          <button type="button" class="btn btn-outline-secondary" style="border-radius: 30px;">
            <img
            class="avatar"
            src="https://randomuser.me/api/portraits/men/77.jpg"
            alt="user"
          /> @adam123 "ChatGpt Cross Near...."</button>
        </div>
      </div>
      <div class="col">
        <div class="user">
          <button type="button" class="btn btn-outline-secondary" style="border-radius: 30px;">
            <img
            class="avatar"
            src="https://randomuser.me/api/portraits/men/77.jpg"
            alt="user"
          /> @adam123 "ChatGpt Cross Near...."</button>
        </div>
      </div>
      <div class="col">
        <div class="user">
          <button type="button" class="btn btn-outline-secondary" style="border-radius: 30px;">
            <img
            class="avatar"
            src="https://randomuser.me/api/portraits/men/77.jpg"
            alt="user"
          /> @adam123 "ChatGpt Cross Near...."</button>
        </div>
        <br>
      </div>
    </div>
  </div>
</div>
<!-- Famous Articles -->



<!-- footer -->
<Footer/>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Newsreader:wght@200&display=swap");

  img.avatar {
    height: 35px;
    width: 35px;
    border-radius: 50%;
    vertical-align: middle;
  }
  
  .user .btn-outline-secondary{
    font-size: 1.4vw;
    color: black;
  }
  .user .btn-outline-secondary:hover{
    background-color: transparent;
  }

  .content4 .header{
    font-size: 4vw;
    font-weight: 900;
    font-family: "Newsreader", serif;
    padding-top: 2%;
  }

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
    font-weight: 900;
    font-family: "Newsreader", serif;
  }
  .content3{
    max-width: 100%;
    background-color: #000;
    color: white;
    justify-content: center;
    text-align: center;
  }

  .content4{
    max-width: 100%;
    background-color: #FFA559;
    color: #000;
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
  img{
    height:20vw;
    width:50vw;
  }
  .butt{
    font-family: "Newsreader", serif;
  }

  .btn-outline-secondary{
    color:white;
  }
  .btn-outline-secondary:hover {
    background-color: white;
    color: black;
  }

</style>
