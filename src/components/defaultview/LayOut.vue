<template>
  <div id="defaultLayout">
    <SideBar />
    <div class="main">
      <NavBar />
      <router-view></router-view>
      <!-- <RouterView /> -->
    </div>
  </div>
</template>

<script setup>
import NavBar from "./NavBar.vue";
import SideBar from "./SideBar.vue";
// import { RouterView } from "vue-router";
</script>

<style scoped>
#defaultLayout {
  /* background-color: #f8fafb; */
  background: url(../../../public/images/bgtwo.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  height: 100%;
  width: 100%;
  display: flex;
  position: relative;
}
.main {
  height: 100vh;
  overflow-y: scroll;
  width: 100%;
  flex: 1;
  padding: 10px 25px;
}
/* ::-webkit-scrollbar {
  display: none;
} */
</style>
