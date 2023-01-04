<template>
  <div class="sidebar">
    <div class="profile-pic">
      <i class="person"
        ><img src="../../../public/images/profile.svg" alt=""
      /></i>
    </div>
    <div class="name-job">
      <h1 class="name">othniel omaidu</h1>
      <p class="job">frontend developer</p>
    </div>
    <div class="description">
      <p>High level experience in web design and development knowledge.</p>
    </div>
    <ul class="social_icon">
      <li>
        <a href="#"><ion-icon name="logo-instagram"></ion-icon></a>
      </li>
      <li>
        <a href="#"><ion-icon name="logo-twitter"></ion-icon></a>
      </li>
      <li>
        <a href="#"><ion-icon name="mail-outline"></ion-icon></a>
      </li>
      <li>
        <a href="#"><ion-icon name="logo-facebook"></ion-icon></a>
      </li>
      <li>
        <a href="#"><ion-icon name="logo-github"></ion-icon></a>
      </li>
    </ul>
    <button class="contact-btn">
      <p>contact me</p>
      <i><img src="../../../public/images/mail.svg" alt="" /></i>
    </button>
  </div>
</template>

<style scoped>
.sidebar {
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  padding: 50px 46px;
  gap: 30px;
  /* position: absolute; */
  width: 271px;
  height: 100vh;
  left: 0px;
  top: 75px;
  border: 1px solid #6d8093;
}
.profile-pic {
  box-sizing: border-box;
  position: absolute;
  width: 163px;
  height: 163px;
  left: 54px;
  top: 50px;
  border-radius: 100px;
  border: 5px solid var(--border-color);
  /* border-color: linear-gradient(143.91deg, #5671a6 1.93%, #b2cad8 111.65%); */
}
.name-job {
  display: grid;
  place-items: center;
  gap: 0;
  transform: translateY(10rem);
}
.name {
  width: 193px;
  height: 36px;
  font-family: "Poppins";
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 36px;
  background: linear-gradient(101.83deg, #5671a6 14.93%, #b2cad8 58.66%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-transform: capitalize;
  /* margin-bottom: -1rem; */
}
.job {
  width: 160px;
  height: 24px;
  font-family: "Poppins";
  font-style: normal;
  font-weight: 600;
  font-size: 16px;
  line-height: 24px;
  color: #383838;
  text-transform: capitalize;
}
.description {
  width: 179px;
  height: 84px;
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 20px;
  text-align: center;
  transform: translateY(92px);
  color: #616161;
}
.social_icon {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: -2.3rem;
  transform: translateY(50px);
}
.social_icon li {
  list-style: none;
}
.social_icon li a {
  font-size: 1.5em;
  color: #5671a6;
  margin: 0 10px;
  display: inline-block;
  transition: 0.2s;
}
.social_icon li a:hover {
  transform: translateY(-10px);
}
.contact-btn {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 10px 15px;
  gap: 10px;
  cursor: pointer;
  width: 164px;
  height: 44px;
  outline: none;
  border: none;
  background: #5671a6;
  border-radius: 100px;
  /* transition: 0.25s ease-in; */
}
.contact-btn p {
  width: 95px;
  height: 24px;
  font-weight: 600;
  font-size: 16px;
  line-height: 24px;
  color: #ffffff;
  margin-top: 12px;
}
.contact-btn i img {
  width: 27.83px;
  height: 15px;
  display: none;
  transition: 0.2s;
}
.contact-btn:hover {
  background: linear-gradient(104.82deg, #5671a6 11.88%, #b3cbd9 80.84%);
  border-radius: 100px;
  /* transition: transform 0.5s ease-out; */
  /* transition: 0.25; */
}
.contact-btn:hover > i img {
  display: block;
  /* transition: 0.25s ease-in; */
}
@media only screen and (max-width: 565px) {
  .sidebar {
    display: none;
  }
}
</style>
