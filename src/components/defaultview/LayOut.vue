<!-- <template>
  <div class="main container-fluid">
    <NavBar />
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-4"><SideBar /></div>
        <div class="col-md-8"><RouterView /></div>
      </div>
    </div>
  </div>
</template> -->

<template>
  <div id="defaultLayout">
    <SideBar />
    <div class="main">
      <NavBar />
      <RouterView />
    </div>
  </div>
</template>

<script setup>
import NavBar from "./NavBar.vue";
import SideBar from "./SideBar.vue";
import { RouterView } from "vue-router";
</script>

<style scoped>
#defaultLayout {
  background-color: #f8fafb;
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
::-webkit-scrollbar {
  display: none;
}
</style>
