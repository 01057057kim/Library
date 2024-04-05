<script setup>
import DesktopNav from "./components/DesktopNav.vue"
import Snippets from "./components/Snippets.vue"
import MobileNav from "./components/MobileNav.vue"
import Left from "./assets/Images/chevron-left.svg"
import Right from "./assets/Images/chevron-right.svg"
import { ref } from "vue"
const show = ref(false)
const AsideHidden = ref(false)
</script>

<template>
  <header class="bg-white">
    <DesktopNav v-if="show" class="hidden md:flex" />
    <MobileNav v-if="show" class="block md:hidden" />
  </header>
  <main class="grid place-content-center min-h-screen mx-5">
    <div>
      <Snippets v-if="show" />
    </div>
    <aside :class="{ 'AsideHidden': AsideHidden }" class="absolute left-0 top-[25%]">
      <div class="flex justify-center w-[10vh] h-[50vh] bg-white py-5 rounded-full ">
        <div
          class="bg-blue-300 bg-opacity-80 rounded-full min-w-10 min-h-10 flex items-center justify-center absolute top-[45%] -right-6 hover:bg-blue-400">
          <button @click="AsideHidden = !AsideHidden" type="text"><img :src="AsideHidden ? Right : Left"
              :alt="AsideHidden ? 'right' : 'left'"></button>
        </div>
        <div>
          <button @click="show = !show"
            class="bg-white rounded-full p-2 uppercase border-4 hover:border-red-500 font-bold" type="text">Nav</button>
        </div>
      </div>
    </aside>
  </main>
</template>

<style scoped>
.AsideHidden {
  left: -8vh;
}
</style>