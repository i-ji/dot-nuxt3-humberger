<template>
  <div class="font-['Verdana']">
    <Header @openHumberger="openHumberger" />
    <Overlay :toggleMenu="toggleMenu" @closeHumberger="closeHumberger" />
    <Main />
  </div>
</template>
<style></style>
<script setup>
import { ref } from "vue";
const toggleMenu = ref(false);
const openHumberger = () => {
  toggleMenu.value = true;
};
const closeHumberger = () => {
  toggleMenu.value = false;
};
</script>
