<script setup>
import DesktopNav from "./components/Nav_Components/DesktopNav.vue"
import Snippets from "./components/Nav_Components/Snippets.vue"
import MobileNav from "./components/Nav_Components/MobileNav.vue"
import AsideButton from "./components/AsideButton.vue"
import DivComponent from "./components/Div_Component/DivComponent.vue"
import { ref, provide } from "vue"
let show = ref(false)
provide('show', show)
let AsideHidden = ref(false)
provide('AsideHidden', AsideHidden)
let activeButton = ref(1)
provide('activeButton', activeButton)
</script>

<template>
  <header class="bg-white">
    <DesktopNav v-if="activeButton === 1" class="hidden md:flex" />
    <MobileNav v-if="activeButton === 1" class="block md:hidden" />
  </header>
  <main class="grid place-content-center min-h-screen mx-5">
    <div>
      <Snippets v-if="activeButton === 1" />
    </div>
    <aside :class="{ 'AsideHidden': AsideHidden }" class="fixed left-0 top-[25%]">
      <AsideButton />
    </aside>
    <section>
      <DivComponent v-if="activeButton === 2" />
    </section>
  </main>
</template>

<style scoped>
.AsideHidden {
  left: -8vh;
}
</style>