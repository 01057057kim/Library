<script setup>
import { inject } from 'vue'
import Left from "../assets/Images/chevron-left.svg"
import Right from "../assets/Images/chevron-right.svg"
let AsideHidden = inject('AsideHidden')
let activeButton = inject('activeButton')
</script>

<template>
    <div class="flex justify-center w-[10vh] h-[50vh] bg-white py-5 rounded-full ">
        <div
            class="bg-blue-300 bg-opacity-80 rounded-full min-w-10 min-h-10 flex items-center justify-center absolute top-[45%] -right-6 hover:bg-blue-400">
            <button @click="AsideHidden = !AsideHidden" type="text"><img :src="AsideHidden ? Right : Left"
                    :alt="AsideHidden ? 'right' : 'left'"></button>
        </div>
        <div>
            <ul class="flex flex-col gap-4">
                <li><button @click="activeButton = 1"
                        class="bg-white rounded-full w-14 h-14 uppercase border-4 hover:border-red-500 font-bold"
                        type="text">Nav</button>
                </li>
                <li>
                    <button @click="activeButton = 2"
                        class="bg-white rounded-full w-14 h-14 uppercase border-4 hover:border-red-500 font-bold"
                        type="text">Div</button>
                </li>
            </ul>
        </div>
    </div>
</template>
