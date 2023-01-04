<template>
  <div class="skill">
    <div class="skill-body">
      <div class="header">
        <div class="title">
          <p class="sk">skills</p>
          <p class="desc">my technical level</p>
        </div>
        <div class="details">
          <p class="job">frontend developer</p>
          <p class="desc">one year</p>
        </div>
      </div>
      <div class="skill-set">
        <div @mouseenter="hover" class="card html">
          <div class="waves">
            <div class="wave" id="wave1"></div>
            <div class="wave2" id="wave2"></div>
            <!-- <div class="wave" id="wave3"></div>
            <div class="wave" id="wave4"></div> -->
          </div>
          <div class="cont">
            <div class="icons">
              <ion-icon class="iconic" name="logo-html5"></ion-icon>
              <p class="icon-title">HTML</p>
            </div>
            <div class="percentage">
              <p>90%</p>
            </div>
          </div>
          <div class="bar"></div>
          <div class="bar2"></div>
        </div>
        <div @mouseenter="hoverTwo" class="card css">
          <div class="waves">
            <div class="wave" id="wave1"></div>
            <div class="wave2" id="wave2"></div>
            <!-- <div class="wave" id="wave3"></div>
            <div class="wave" id="wave4"></div> -->
          </div>
          <div class="cont">
            <div class="icons">
              <ion-icon class="iconic" name="logo-css3"></ion-icon>
              <!-- <ion-icon class="iconic" name="logo-html5"></ion-icon> -->
              <p class="icon-title">CSS</p>
            </div>
            <div class="percentage">
              <p>80%</p>
            </div>
          </div>
          <div class="bar"></div>
          <div class="bar2"></div>
        </div>
        <div @mouseenter="hoverThree" class="card js">
          <div class="waves">
            <div class="wave" id="wave1"></div>
            <div class="wave2" id="wave2"></div>
            <!-- <div class="wave" id="wave3"></div>
            <div class="wave" id="wave4"></div> -->
          </div>
          <div class="cont">
            <div class="icons">
              <ion-icon class="iconic" name="logo-nodejs"></ion-icon>
              <!-- <ion-icon class="iconic" name="logo-html5"></ion-icon> -->
              <p class="icon-title">JS</p>
            </div>
            <div class="percentage">
              <p>70%</p>
            </div>
          </div>
          <div class="bar"></div>
          <div class="bar2"></div>
        </div>
        <div @mouseenter="hoverFour" class="card vue">
          <div class="waves">
            <div class="wave" id="wave1"></div>
            <div class="wave2" id="wave2"></div>
            <!-- <div class="wave" id="wave3"></div>
            <div class="wave" id="wave4"></div> -->
          </div>
          <div class="cont">
            <div class="icons">
              <!-- <ion-icon class="iconic" name="logo-html5"></ion-icon> -->
              <ion-icon class="iconic" name="logo-vue"></ion-icon>
              <p class="icon-title">VUE</p>
            </div>
            <div class="percentage">
              <p>55%</p>
            </div>
          </div>
          <div class="bar"></div>
          <div class="bar2"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const hover = () => {
  // alert("hovered");
  const wave = document.querySelector(".wave");
  const wave2 = document.querySelector(".wave2");
  const icon = document.querySelector(".iconic");
  wave.classList.add("showwave");
  wave2.classList.add("showwave");
  icon.classList.add("html");
};
const hoverTwo = () => {
  // alert("hovered");
  const wave = document.querySelector(".css").querySelector(".wave");
  const wave2 = document.querySelector(".css").querySelector(".wave2");
  const icon = document.querySelector(".css").querySelector(".iconic");
  wave.classList.add("showwave");
  wave2.classList.add("showwave");
  icon.classList.add("css");
};
const hoverThree = () => {
  // alert("hovered");
  const wave = document.querySelector(".js").querySelector(".wave");
  const wave2 = document.querySelector(".js").querySelector(".wave2");
  const icon = document.querySelector(".js").querySelector(".iconic");
  wave.classList.add("showwave");
  wave2.classList.add("showwave");
  icon.classList.add("js");
};
const hoverFour = () => {
  // alert("hovered");
  const wave = document.querySelector(".vue").querySelector(".wave");
  const wave2 = document.querySelector(".vue").querySelector(".wave2");
  const icon = document.querySelector(".vue").querySelector(".iconic");
  wave.classList.add("showwave");
  wave2.classList.add("showwave");
  icon.classList.add("vue");
};
</script>

<style scoped>
.skill {
  width: 100%;
  margin-top: 1rem;
}
.skill-body {
  display: grid;
  place-items: center;
  text-transform: capitalize;
}
.header {
  text-align: center;
}
.sk {
  font-weight: 600;
  font-size: 32px;
  line-height: 48px;
  color: #383838;
  text-align: center;
  /* margin-bottom: 0.5em; */
}
.desc {
  font-weight: 500;
  font-size: 14px;
  line-height: 21px;
  /* identical to box height */

  text-align: center;

  color: #616161;
}
.job {
  font-weight: 600;
  font-size: 16px;
  line-height: 24px;
  /* margin-bottom: -0.5em; */
  text-align: center;
  color: #383838;
}
.skill-set {
  display: grid;
  grid-template-columns: repeat(auto-fill, 250px);
  padding: 24px;
  gap: 20px;
  justify-content: center;
  width: 100%;
}
.card {
  position: relative;
  /* width: 170px; */
  height: 150px;
  /* border: 1px solid pink; */
  border-radius: 5px;
  /* padding: 10px; */
}
.cont {
  display: flex;
  justify-content: space-between;
  transform: translateY(5rem);
  padding: 0px 10px;
  z-index: 6000;
  position: relative;
}
.iconic {
  color: #383838;
  font-size: 30px;
  margin-bottom: 0.2em;
}
.icon-title {
  font-weight: 600;
  font-size: 16px;
  line-height: 24px;
  color: #383838;
  margin-bottom: -0.1em;
  /* trans */
}
.percentage {
  font-weight: 600;
  font-size: 16px;
  line-height: 24px;
  color: #616161;
  transform: translateY(2.6rem);
  /* margin-bottom: 0.2em; */
}
.bar {
  /* width: 170px; */
  height: 5px;
  background: #cc985b;
  transform: translateY(5.2rem);
  z-index: 1000;
  position: relative;
}
.bar2 {
  /* width: 170px; */
  height: 5px;
  background: #e89e9e;
  transform: translateY(4.9rem);
}
.wave {
  position: absolute;
  top: 9px;
  left: 0;
  width: 100%;
  height: 140px;
  background: url(../../public/images/Rectangle\ 8.png);
  background-size: 500px 191px;
  background-position-y: bottom;
  transform: scale(0);
  background-repeat: repeat-x;
  animation: animate 10s linear infinite;
  z-index: 999;
}
.wave2 {
  position: absolute;
  top: 7px;
  left: 0;
  width: 100%;
  height: 140px;
  background: url(../../public/images/anotherWave.png);
  background-size: 500px 191px;
  background-position-y: bottom;
  transform: scale(0);
  background-repeat: repeat-x;
  animation: animate 10s linear infinite;
}
/* .wave#wave1 {
  z-index: 1000;
  opacity: 1;
  bottom: 0;
  animation: animatewave 4s linear infinite;
}
.wave#wave2 {
  z-index: 999;
  opacity: 0.5;
  bottom: 15px;
  animation: animatewave_02 3s linear infinite;
}
.wave#wave3 {
  background: pink;
  z-index: 999;
  opacity: 0.7;
  bottom: 20px;
  animation: animatewave 3s linear infinite;
}
.wave#wave4 {
  z-index: 999;
  opacity: 0.5;
  bottom: 10px;
  animation: animatewave_02 4s linear infinite;
} */
@keyframes animatewave {
  0% {
    background-position-x: 1000px;
  }
  100% {
    background-position-x: 0px;
  }
}
@keyframes animatewave_02 {
  0% {
    background-position-x: 0px;
  }
  100% {
    background-position-x: 1000px;
  }
}
@keyframes animate {
  0% {
    background-position: 0 100px;
  }
  10% {
    background-position: 0 100px;
  }
  40% {
    background-position: 1000px 0;
  }
  80% {
    background-position: 2000px 0;
  }
  100% {
    background-position: 2500px 0;
  }
}
.showwave {
  transform: scale(1);
  /* color: #e44d26; */
}
.html {
  color: #e44d26;
}
.css {
  color: #2196f3;
}
.js {
  color: #f0db4f;
}
.vue {
  color: #41b883;
}
/* css animation */
.css .bar {
  /* width: 170px; */
  height: 5px;
  background: #84b1db;
  transform: translateY(5.2rem);
  z-index: 1000;
  position: relative;
}
.css .bar2 {
  /* width: 170px; */
  height: 5px;
  background: #84b1db;
  transform: translateY(4.9rem);
}
.css .wave {
  position: absolute;
  top: 24px;
  left: 0;
  width: 100%;
  height: 128px;
  background: url(../../public/images/css1.png);
  background-size: 500px 125px;
  background-position-y: bottom;
  /* transform: scale(0); */
  background-repeat: repeat-x;
  animation: animatewave2 10s linear infinite;
  z-index: 999;
}
.css .wave2 {
  position: absolute;
  top: 22px;
  left: 0;
  width: 100%;
  height: 128px;
  background: url(../../public/images/css2.png);
  background-size: 500px 125px;
  background-position-y: bottom;
  /* transform: scale(0); */
  background-repeat: repeat-x;
  animation: animatewave2 10s linear infinite;
}
@keyframes animatewave2 {
  0% {
    background-position: 0 100px;
  }
  10% {
    background-position: 0 100px;
  }
  40% {
    background-position: 1000px 0;
  }
  80% {
    background-position: 2000px 0;
  }
  100% {
    background-position: 2500px 0;
  }
}
/* js animation */
.js .bar {
  /* width: 170px; */
  height: 5px;
  background: #ede98b;
  transform: translateY(5.2rem);
  z-index: 1000;
  position: relative;
}
.js .bar2 {
  /* width: 170px; */
  height: 5px;
  background: #fffcb6;
  transform: translateY(4.9rem);
}
.js .wave {
  position: absolute;
  top: 40px;
  left: 0;
  width: 100%;
  height: 110px;
  background: url(../../public/images/js1.png);
  background-size: 500px 125px;
  background-position-y: bottom;
  /* transform: scale(0); */
  background-repeat: repeat-x;
  animation: animatewave3 10s linear infinite;
  z-index: 999;
}
.js .wave2 {
  position: absolute;
  top: 40px;
  left: 0;
  width: 100%;
  height: 110px;
  background: url(../../public/images/js2.png);
  background-size: 500px 128px;
  background-position-y: bottom;
  /* transform: scale(0); */
  background-repeat: repeat-x;
  animation: animatewave3 10s linear infinite;
}
@keyframes animatewave3 {
  0% {
    background-position: 0 100px;
  }
  10% {
    background-position: 0 100px;
  }
  40% {
    background-position: 1000px 0;
  }
  80% {
    background-position: 2000px 0;
  }
  100% {
    background-position: 2500px 0;
  }
}
/* vue animation */
.vue .bar {
  /* width: 170px; */
  height: 5px;
  background: #0ce87a;
  transform: translateY(5.2rem);
  z-index: 1000;
  position: relative;
}
.vue .bar2 {
  /* width: 170px; */
  height: 5px;
  background: #96ffca;
  transform: translateY(4.9rem);
}
.vue .wave {
  position: absolute;
  top: 69px;
  left: 0;
  width: 100%;
  height: 80px;
  background: url(../../public/images/vue1.png);
  background-size: 500px 125px;
  background-position-y: bottom;
  /* transform: scale(0); */
  background-repeat: repeat-x;
  animation: animatewave4 10s linear infinite;
  z-index: 999;
}
.vue .wave2 {
  position: absolute;
  top: 69px;
  left: 0;
  width: 100%;
  height: 80px;
  background: url(../../public/images/vue2.png);
  background-size: 500px 128px;
  background-position-y: bottom;
  /* transform: scale(0); */
  background-repeat: repeat-x;
  animation: animatewave4 10s linear infinite;
}
@keyframes animatewave4 {
  0% {
    background-position: 0 100px;
  }
  10% {
    background-position: 0 100px;
  }
  40% {
    background-position: 1000px 0;
  }
  80% {
    background-position: 2000px 0;
  }
  100% {
    background-position: 2500px 0;
  }
}
</style>
