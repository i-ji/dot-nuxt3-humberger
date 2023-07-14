<template>
  <header class="flex px-4">
    <div>
      <h1 class="text-[22px] leading-[64px] font-bold">LOGO</h1>
    </div>

    <div class="ml-auto sm:hidden">
      <i
        class="fa-solid fa-bars text-2xl leading-[64px] cursor-pointer"
        @click="openHumberger"
      ></i>
    </div>

    <nav class="hidden ml-auto sm:block">
      <ul class="flex text-center">
        <li>
          <a href="#" class="block w-20 leading-[64px] hover:bg-gray-100"
            >Menu</a
          >
        </li>
        <li>
          <a href="#" class="block w-20 leading-[64px] hover:bg-gray-100"
            >Menu</a
          >
        </li>
        <li>
          <a href="#" class="block w-20 leading-[64px] hover:bg-gray-100"
            >Menu</a
          >
        </li>
      </ul>
    </nav>
  </header>
</template>
<script setup>
const emit = defineEmits(["openHumberger"]);

const openHumberger = () => {
  emit("openHumberger");
};
</script>
