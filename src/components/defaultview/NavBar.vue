<!-- <template>
  <div class="navigation">
    <nav>
      <div class="nav-header">
        <div class="menu-toggle"></div>
      </div>
      <ul class="nav-links links">
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
</template> -->

<style scoped>
/* .navigation {
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

@media only screen and (min-width: 565px) {
  nav .nav-header h1 {
    width: 25%;
    height: 54px;
    left: 20px;
    top: 15px;
    font-weight: 600;
    font-size: 24px;
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
} ; */
</style>

<template>
  <div>
    <nav>
      <div class="nav-center">
        <!-- nav header -->
        <div class="nav-header">
          <!-- <img src="./logo.svg" class="logo" alt="logo" /> -->
          <button class="nav-toggle" @click="toggleNav">
            <i class="fas fa-bars"></i>
          </button>
        </div>
        <!-- links -->
        <ul class="links" :class="{ show_links: isActive }">
          <ul class="nav-links links">
            <li
              class="hover-underline-animation"
              :class="{ linkz: showLinks, link1: linkPos1 }"
            >
              <router-link class="hov" to="/">About</router-link>
            </li>
            <li
              class="hover-underline-animation"
              :class="{ linkz: showLinks, link2: linkPos2 }"
            >
              <router-link class="hov" to="/skills">skills</router-link>
            </li>
            <li
              class="hover-underline-animation"
              :class="{ linkz: showLinks, link3: linkPos3 }"
            >
              <router-link class="hov" to="/portfolio">portfolio</router-link>
            </li>
          </ul>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const isActive = ref(null);
const showLinks = ref(null);
const linkPos1 = ref(null);
const linkPos2 = ref(null);
const linkPos3 = ref(null);

onMounted(() => {
  window.addEventListener("resize", checkScreen);
  checkScreen();
});

const toggleNav = () => {
  isActive.value = !isActive.value;
  showLinks.value = !showLinks.value;
  linkPos1.value = !linkPos1.value;
  linkPos2.value = !linkPos2.value;
  linkPos3.value = !linkPos3.value;
};

const checkScreen = () => {
  if (window.innerWidth > 600) {
    isActive.value = false;
    showLinks.value = false;
    linkPos1.value = false;
    linkPos2.value = false;
    linkPos3.value = false;
  }
};
</script>

<style scoped>
nav {
  background: var(--clr-white);
  box-shadow: var(--light-shadow);
  border: 1px solid #6d8093;
}
.nav-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem;
}
.nav-toggle {
  font-size: 1.5rem;
  color: var(--clr-primary-5);
  background: transparent;
  border-color: transparent;
  transition: var(--transition);
  cursor: pointer;
}
.nav-toggle:hover {
  color: var(--clr-primary-1);
  transform: rotate(90deg);
}

.links a {
  position: relative;
  color: var(--clr-grey-3);
  font-size: 1rem;
  text-transform: capitalize;
  letter-spacing: var(--spacing);
  display: block;
  padding: 0.5rem 1rem;
  transition: var(--transition);
  z-index: 200000;
}
.links a:hover {
  background: var(--clr-primary-8);
  color: var(--clr-primary-5);
  padding-left: 1.5rem;
}
.social-icons {
  display: none;
}
.links {
  height: 0;
  overflow: hidden;
  transition: var(--transition);
}
.show_links {
  height: 7rem;
  /* transform: translateX(-64px); */
  transform: translate(-64px, -38px);
}
.linkz {
  position: absolute;
}
.link1 {
  transform: translateY(1rem);
}
.link2 {
  transform: translateY(3rem);
}
.link3 {
  transform: translateY(5rem);
}
@media screen and (min-width: 800px) {
  .nav-center {
    max-width: 1170px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem;
  }
  .nav-header {
    padding: 0;
  }
  .nav-toggle {
    display: none;
  }
  .links {
    height: auto;
    display: flex;
  }
  .links a {
    padding: 0;
    margin: 0 0.5rem;
  }
  .links a:hover {
    padding: 0;
    background: transparent;
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
}
</style>
