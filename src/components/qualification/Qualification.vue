<template>
  <div>
    <hr />
    <div class="qualification_page">
      <QualificationTabs
        @education="tabs = 'education'"
        @work="tabs = 'work'"
      />
      <div v-if="tabs == 'education'"><EducationVue /></div>
      <div v-if="tabs == 'work'"><WorkVue /></div>
      <!-- <hr /> -->
    </div>
  </div>
</template>

<script setup>
import EducationVue from "./Education.vue";
import WorkVue from "./Work.vue";
import { ref } from "vue";
import QualificationTabs from "./QualificationTabs.vue";

const tabs = ref("education");
</script>

<style scoped>
.qualification_page {
  margin-top: 1.5rem;
}
hr {
  margin-top: 0.9em;
  /* background-color: #dbdbdb; */
  border: 1px solid #a79c9c;
  /* position: absolute; */
  width: 100%;
  height: 0px;
}
</style>
