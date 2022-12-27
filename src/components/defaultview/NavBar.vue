<template>
  <div class="navigation">
    <nav>
      <div class="nav-header">
        <div class="menu-toggle"></div>
        <h1>othniel omaidu</h1>
      </div>
      <ul class="nav-links">
        <li class="link hover-underline-animation">
          <router-link class="hov" to="/">About</router-link>
        </li>
        <li class="link hover-underline-animation">
          <router-link class="hov" to="/skills">skills</router-link>
        </li>
        <li class="link hover-underline-animation">
          <router-link class="hov" to="/portfolio">portfolio</router-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.navigation {
  width: 100%;
}
nav {
  display: flex;
  justify-content: space-between;
  height: 76px;
  width: 100%;
  border: 1px solid #6d8093;
}
nav a {
  /* font-weight: bold; */
  color: #5671a6;
  text-decoration: none;
  list-style: none;
  transition: 0.2s;
}
.nav-header {
  display: flex;
  justify-content: space-between;
  text-transform: capitalize;
}

.nav-links {
  display: flex;
  justify-content: space-between;
  gap: 16px;
  list-style: none;
  transform: translate(-14px, 3px);
  height: 24px;
  width: 29%;
}
.nav-links :nth-child(3) {
  transform: translate(-96px, 20px);
}
.hover-underline-animation {
  display: inline-block;
  position: relative;
  color: #b3cbd9;
}

.hover-underline-animation:after {
  content: "";
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #b3cbd9;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.hover-underline-animation:hover:after {
  transform: scaleX(1);
  transform-origin: bottom left;
  background-color: #b3cbd9;
}
.hov:hover {
  color: #b3cbd9;
}

/* media query */
@media only screen and (min-width: 565px) {
  nav .nav-header h1 {
    position: absolute;
    width: 25%;
    height: 54px;
    left: 20px;
    top: 15px;
    font-weight: 600;
    font-size: 100%;
    max-height: fit-content;
    line-height: 54px;
    color: #5671a6;
    text-transform: capitalize;
  }
  .nav-links {
    position: absolute;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    padding: 0px;
    /* gap: 47px; */
    text-transform: uppercase;
    position: absolute;
    width: 250px;
    height: 27px;
    right: 144px;
    top: 28px;
    list-style: none;
    gap: 10px;
    transform: translate(80px, 0);
  }
  .nav-links :nth-child(3) {
    transform: translate(0px, 0px);
  }
  .menu-toggle {
    display: none;
  }
} ;
</style>
