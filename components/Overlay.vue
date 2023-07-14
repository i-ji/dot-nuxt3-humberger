<template>
  <transition name="fade">
    <div
      :class="{ overlay: toggleMenu }"
      v-show="toggleMenu"
      class="fixed top-0 bottom-0 right-0 left-0 bg-white text-center"
    >
      <i
        class="fa-solid fa-xmark absolute top-4 right-4 text-2xl cursor-pointer"
        @click="closeHumberger"
      ></i>
      <nav class="mt-20">
        <ul>
          <transition name="show1">
            <li class="mt-6" v-show="toggleMenu">
              <a href="#">Menu</a>
            </li>
          </transition>
          <transition name="show2">
            <li class="mt-6" v-show="toggleMenu">
              <a href="#">Menu</a>
            </li>
          </transition>
          <transition name="show3">
            <li class="mt-6" v-show="toggleMenu">
              <a href="#">Menu</a>
            </li>
          </transition>
        </ul>
      </nav>
    </div>
  </transition>
</template>

<style>
.overlay {
  opacity: 0.95;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.4s;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.show1-enter-active,
.show1-leave-active {
  transition: all 0.3s;
  transition-delay: 0.1s;
}

.show1-enter-from,
.show1-leave-to {
  opacity: 0;
  transform: translateY(16px);
}

.show2-enter-active,
.show2-leave-active {
  transition: all 0.3s;
  transition-delay: 0.2s;
}

.show2-enter-from,
.show2-leave-to {
  opacity: 0;
  transform: translateY(16px);
}

.show3-enter-active,
.show3-leave-active {
  transition: all 0.3s;
  transition-delay: 0.3s;
}

.show3-enter-from,
.show3-leave-to {
  opacity: 0;
  transform: translateY(16px);
}
</style>

<script setup>
const props = defineProps(["toggleMenu"]);
const emit = defineEmits(["closeHumberger"]);
const closeHumberger = () => {
  emit("closeHumberger");
};
</script>
