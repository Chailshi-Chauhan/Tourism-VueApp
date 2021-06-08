<template>
  <div>
    <div id="myPage" class="overlay">
      <main class="grid overlay-content">
        <article>
          <img src="../assets/shillong.jpeg" alt="Sample photo">
          <div class="text">
            <h3>SHILLONG</h3>
            <p>Shillong is a hill station in the northeastern part of India and the capital of Meghalaya, which means "The Abode of Clouds".</p>
            <a href="https://en.wikipedia.org/wiki/Shillong">Here's why</a>
          </div>
        </article>
        <article>
          <img src="../assets/bangalore.jpeg" alt="Sample photo">
          <div class="text">
            <h3>BANGALORE</h3>
            <p>The city is popularly known as "The Silicon Valley of India" and is the nation's leading IT employer and exporter.</p>
            <a href="https://en.wikipedia.org/wiki/Bangalore">Here's why</a>
          </div>
        </article>
        <article>
          <img src="../assets/gujarat.jpeg" alt="Sample photo">
          <div class="text">
            <h3>GUJARAT</h3>
            <p>Asiatic lions, Rann of Kutch (White Desert), colourful handicrafts, festival and culture are some of the things that make Gujarat famous.</p>
            <a href="https://en.wikipedia.org/wiki/Gujarat">Here's why</a>
          </div>
        </article>
        <button class="closebtn" @click="closeNav()">X</button>
        <article>
          <img src="../assets/Himachal.jpeg" alt="Sample photo">
          <div class="text">
            <h3>HIMACHAL</h3>
            <p>Largest glacier in Asia. The Manali – Leh National Highway is famed for being the highest motor able road in the world.</p>
            <a href="https://en.wikipedia.org/wiki/Himachal_Pradesh">Here's why</a>
          </div>
        </article>
        <article>
          <img src="../assets/goa.jpeg" alt="Sample photo">
          <div class="text">
            <h3>GOA</h3>
            <p>Overwhelming Beaches. Goa is one of the most favorite destination among Indian tourists due to its pristine beaches.</p>
            <a href="https://en.wikipedia.org/wiki/Goa">Here's why</a>
          </div>
        </article>
        <article>
          <img src="../assets/Kerala.jpeg" alt="Sample photo">
          <div class="text">
            <h3>KERALA</h3>
            <p>Kerala is well-known for its mesmerizing backwaters, ecotourism initiatives, scenic beauty, amazing beaches, and mouthwatering cuisine.</p>
            <a href="https://en.wikipedia.org/wiki/Kerala">Here's why</a>
          </div>
        </article>
      </main>
    </div>
    <div  id="home-page">
      <img src="../assets/india.jpeg" class="india"/>
      <h1 class="title" id="title"> WELCOME TO INDIAN TOURISM</h1>
      <br>
      <span id="open"  @click="openNav()">&#9776; open</span>
      <br>
      <img src="../assets/taj.jpeg" class="india"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    openNav () {
      document.getElementById("myPage").style.display = "block";
      document.getElementById("home-page").style.display = "none";
    },

    closeNav () {
      document.getElementById("myPage").style.display = "none";
      document.getElementById("home-page").style.display = "block";
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#home-page {
  background-color: rgb(194, 214, 214, 0.5);
}

#open {
  font-size:30px;
  cursor:pointer;
}
#open:hover {
  font-weight: bold;
  background-color: white;
}
.india {
  height: 320px;
  width: 700px;
}
.title {
  margin: 10px;
  font-weight: bold;
  font-size: 80px;  
  text-shadow: 5px 5px #ff0000;
  display: inline-block;
  animation: move 2s ease-in-out;
}
@keyframes move {
  0% {
    transform: translate(-10%, 0);
  }
  50% {
    text-shadow: 0 25px 50px #ff0000;
  }
  100% {
    transform: translate(0%, 0);
  }
}

.overlay{
  background-color:rgb(194, 214, 214, 0.5);
  height: 100%;
  display: none;
  width: 100%;
}

.overlay-content {
  position: relative;
}
.overlay .closebtn {
  cursor: pointer;
  background-color: yellow;
  width: 3%;
  position: absolute;
  top: 5px;
  right: 5px;
  font-size: 40px;
}
.overlay .closebtn:hover {
  color: blueviolet;
  background-color: white;
}
.grid { 
  display: grid;
  /* 1fr == 1 fraction space all the coloums will be of 1 fractional space, auto-fill FILLS the row with as many columns as it can fit */
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  grid-gap: 80px;
  align-items: stretch;
  /* align-items: stretch; The flexbox items will stretch across the whole cross axis */
  }
.grid > article {
  background-color: thistle;
  border: 1px solid #ccc;
  border-radius: 8%;
  box-shadow: 2px 2px 6px 0px  rgba(0,0,0,0.6);
}
.grid > article img {
  margin-top: 20px;
  max-width: 100%;
}
.text {
  padding: 10px 30px 20px ;
}
.text > a {
  margin-top: 100px;
  border-radius: 50% ;
  background: gray;
  border: 0;
  color: white;
  padding: 15px;
  }

  .text > a:hover {
    color: black;
  }
</style>
