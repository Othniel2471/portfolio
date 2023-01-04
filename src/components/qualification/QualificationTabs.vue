<template>
  <div class="tabs">
    <div
      class="tab_links"
      @click="education"
      :class="{ active_tab: tab == 'education' }"
    >
      <ion-icon class="icon" name="school-outline"></ion-icon>
      <p class="text">Education</p>
    </div>
    <div
      class="tab_links link"
      @click="work"
      :class="{ active_tab: tab == 'work' }"
    >
      <ion-icon class="icon" name="briefcase-outline"></ion-icon>
      <p class="text">Work</p>
    </div>
  </div>
</template>

<script setup>
import { defineEmits, ref } from "vue";

const tab = ref("education");
const emit = defineEmits(["education", "work"]);
const education = () => {
  tab.value = "education";
  emit("education");
};
const work = () => {
  tab.value = "work";
  emit("work");
};
</script>

<style scoped>
.tabs {
  display: flex;
}
.tab_links {
  margin-right: 8em;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: space-between;
  padding: 0px;
  gap: 3px;
  width: 100%;
  height: 24px;
  left: 20px;
  top: 20px;
  cursor: pointer;
}
.tab_links:hover {
  color: #5671a6;
}
.link {
  margin-left: 2em;
  transform: translateX(-2em);
}
.icon {
  width: 25.06px;
  height: 19px;
  /* margin-right: 0.5em; */
  /* transform: translateY(1em); */
}
</style>
