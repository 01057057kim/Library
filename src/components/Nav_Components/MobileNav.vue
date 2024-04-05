<script setup>
import { ref } from 'vue'
const show = ref(false)
</script>

<template>
    <nav class="flex justify-between items-center w-full px-5 py-2 mx-auto text-nowrap">
        <div v-if="show" class="absolute w-full h-screen left-0 top-0 bg-black bg-opacity-50"></div>
        <div class="flex gap-[4vw]">
            <button @click="show = !show" type="text">
                <img src="../assets/Images/menu.svg" alt="hamburger">
            </button>
            <p class="text-2xl font-bold uppercase">logo</p>
        </div>
        <div v-if="show" class="absolute bg-white min-h-screen w-[25%] left-0 top-[0%] p-5">
            <ul class="flex flex-col items-start gap-[3vw]">
                <div>
                    <button @click="show = false" type="text">
                        <img src="../assets/Images/close.svg" alt="close">
                    </button>
                </div>
                <li>
                    <a class="hover:text-gray-500 font-semibold" href="#">Home</a>
                </li>
                <li>
                    <a class="hover:text-gray-500 font-semibold" href="#">Products</a>
                </li>
                <li>
                    <a class="hover:text-gray-500 font-semibold" href="#">Pricing</a>
                </li>
                <li>
                    <a class="hover:text-gray-500 font-semibold" href="#">About Us</a>
                </li>
            </ul>
        </div>
        <div>
            <button class="bg-red-500 text-white px-5 py-2 rounded-full hover:bg-opacity-80" type="text">
                Get Started</button>
        </div>
    </nav>
</template>
