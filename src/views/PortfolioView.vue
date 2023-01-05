<template>
  <div class="portfolio">
    <div class="portfolio-body">
      <h1 class="header">portfolio</h1>
      <div class="wrapper">
        <div class="box">
          <h3>STICKY</h3>
          <div class="img">
            <img src="../../public/images/projects/sticky.png" alt="" />
          </div>
          <div class="content">
            <p>
              Sticky is a simple note app, that i developed with "vue". The
              users gets the chance to add new notes. The notes are generated
              and given random colors, the user also has the ability to delete
              notes and also change the theme of each note with the color
              choices provided
            </p>
            <br />
            <a
              href="https://othniel2471.github.io/stickyNotes/"
              class="btns"
              target="_blank"
              >Live Demo</a
            >
          </div>
        </div>

        <div class="box">
          <h3>MATCHAPP</h3>
          <div class="img">
            <img src="../../public/images/projects/matchapp.png" alt="" />
          </div>
          <div class="content">
            <p>
              The MatchApp is an app i developed when i wanted to make it
              possible to share christmas presents with my family, and we needed
              to get names randomly, so i built this simple app that takes in my
              family members names and also randomly picks two people and match
              them together.
            </p>
            <br />
            <a
              href="https://othniel2471.github.io/matchApp/"
              target="_blank"
              class="btns"
              >Live Demo</a
            >
          </div>
        </div>
        <div class="box">
          <h3>Intro Section</h3>
          <div class="img">
            <img src="../../public/images/projects/introsection.png" alt="" />
          </div>
          <div class="content">
            <p>
              This is the hero section of a home page for an app. I built it
              with vanilla js and tailwind css, it is fully responsive. I got
              the excercise from frontend mentor
            </p>
            <br />
            <a
              href="https://tailwindherosection.netlify.app/"
              class="btns"
              target="_blank"
              >Live Demo</a
            >
          </div>
        </div>
        <div class="box">
          <h3>OT - SAMA</h3>
          <div class="img">
            <img src="../../public/images/css1.png" alt="" />
          </div>
          <div class="content">
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Recusandae deleniti sint consequuntur quo amet! Esse
              exercitationem repellendus atque eos cupiditate doloremque, natus
              libero vitae quod officia consequatur assumenda cumque odit omnis
              fuga? Laboriosam accusantium eaque sit saepe alias aliquam!
            </p>
            <br />
            <a href="#" class="btns">Live Demo</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.portfolio {
  width: 100%;
  margin-top: 1rem;
}
.portfolio-body {
  display: grid;
  place-items: center;
  text-transform: capitalize;
}
.header {
  font-weight: 600;
  line-height: 36px;
  background: linear-gradient(101.83deg, #5671a6 14.93%, #b2cad8 58.66%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-transform: capitalize;
}
.wrapper {
  display: grid;
  grid-template-columns: repeat(auto-fill, 300px);
  padding: 24px;
  gap: 20px;
  justify-content: center;
  width: 100%;
}
.box {
  background: #fff;
  padding: 20px;
  border-radius: 2rem;
}
.box:hover {
  transform: translateY(-10px);
  transition: 0.5s;
  cursor: pointer;
}
.box .img {
  border-radius: 1rem;
  width: 100%;
}

.box h3 {
  font-size: 1rem;
  font-weight: 600;
  float: right;
}
.content {
  /* width: 20rem; */
  font-size: 13px;
  padding: 10px;
  margin-bottom: 0.5rem;
  text-align: justify;
  box-shadow: 0 10px 20px 3px #00968814;
  /* filter: blur(3px); */
}
.btns {
  background: #000;
  color: #fff;
  border-radius: 0.5rem;
  padding: 5px;
}
.btns:hover {
  background: #333;
}
</style>
