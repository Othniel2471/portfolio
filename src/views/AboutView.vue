<template>
  <div class="about">
    <p class="about-header">about</p>
    <p class="about-text">
      Web developer, with extensive knowledge and years of experience, working
      in web technologies and UI/UX design, delivering quality work.
    </p>
    <div class="abt-cards container">
      <div class="row">
        <div class="card col-md-4">
          <div class="icon">
            <i><img src="../../public/images/exp.svg" alt="" /></i>
          </div>
          <div class="content">
            <p class="exp">Years experience</p>
            <p class="no">1</p>
          </div>
        </div>

        <div class="card col-md-4">
          <div class="icon">
            <i><img src="../../public/images/exp.svg" alt="" /></i>
          </div>
          <div class="content">
            <p class="exp">Completed projects</p>
            <p class="no">5</p>
          </div>
        </div>

        <div class="card col-md-4">
          <div class="icon">
            <i><img src="../../public/images/exp.svg" alt="" /></i>
          </div>
          <div class="content">
            <p class="exp">Companies worked</p>
            <p class="no">2</p>
          </div>
        </div>
      </div>
    </div>
    <div class="qualification container">
      <div class="header">
        <p class="qual">Qualification</p>
        <p class="text">My personal journey</p>
      </div>
      <QualificationVue />
    </div>
  </div>
</template>

<script setup>
import QualificationVue from "@/components/qualification/Qualification.vue";
</script>
<style scoped>
.about {
  width: 100%;
  margin-top: 1rem;
}
.about-header {
  width: 99px;
  height: 48px;
  font-weight: 600;
  font-size: 32px;
  line-height: 48px;
  color: #5671a6;
  text-transform: capitalize;
}
.about-text p {
  width: 593px;
  height: 35px;
  font-weight: 500;
  font-size: 14px;
  line-height: 21px;
  color: #616161;
}
.about-text {
  width: 593px;
}
.abt-cards {
  display: flex;
  gap: 20px;
  margin-left: 0rem;
  /* margin-top: 10rem; */
  width: 100%;
}
.abt-cards .card {
  width: 150px;
  height: 150px;
  border-radius: 10px;
  padding: 5px;
  transition: 0.25s;
  margin-right: 2rem;
}
.abt-cards .card:hover {
  /* width: 150px;
  height: 150px; */
  overflow: hidden;
  background: rgba(255, 255, 255, 0.5);
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 10px;
}
.abt-cards .card .content {
  display: flex;
  justify-content: space-between;
  transform: translateY(60px);
}
.abt-cards .card .content .exp {
  width: 78px;
  height: 42px;
  font-weight: 500;
  font-size: 14px;
  line-height: 21px;
  color: #383838;
}
.abt-cards .card .content .no {
  width: 18px;
  height: 26px;
  font-weight: bolder;
  transform: translateY(13px);
  color: #383838;
  transition: 0.25s;
}
.abt-cards .card:hover > .content .no {
  position: absolute;
  font-size: 84.49px;
  color: rgb(120, 224, 234);
  transform: rotate(-18.57deg) translateY(-46px) translateX(100px);
}
.qualification {
  margin-top: 2rem;
}
.qualification .header {
  display: flex;
  justify-content: space-between;
  width: 40%;
}
.qualification .header .qual {
  /* position: absolute;
  width: 210px;
  height: 48px;
  left: 50px;
  top: 327px;
  font-family: "Poppins";
  font-style: normal; */
  font-weight: 600;
  font-size: 32px;
  line-height: 48px;
  color: #5671a6;
  margin-top: -0.3rem;
}
.qualification .header .text {
  width: 123px;
  height: 18px;
  margin-top: 1.1rem;
  font-weight: 500;
  font-size: 12px;
  line-height: 18px;
  color: #616161;
}

@media only screen and (max-width: 600px) {
  .about-text {
    width: 100%;
  }
  .abt-cards .card {
    width: 100%;
    margin-bottom: 1rem;
  }
  .qualification .header {
    width: 100%;
  }
  .qualification .header .text {
    width: 100%;
    font-size: 11px;
    transform: translate(0px, -5px);
  }
}
</style>
