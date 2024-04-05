<script setup>
import Snippets from './Snippets.vue';
</script>

<template>
    <section class="grid">
        <div class="flex gap-10">
            <div class="w-[400px]">
                <div class=" h-[400px] bg-white flex items-center justify-center">
                    <div class="w-[200px] h-[200px] bg-black flex items-center justify-center">
                        <p class="text-white">Flex</p>
                    </div>
                </div>
            </div>
            <div class="w-[400px]">
                <div class="h-[400px] bg-white">
                    <div class="h-[400px] bg-white grid place-content-center">
                        <div class="w-[200px] h-[200px] bg-black grid place-content-center">
                            <p class="text-white">Grid</p>
                        </div>
                    </div>
                </div>
            </div>
            <div>
                <div class="w-[400px] h-[400px] bg-white">
                    <div
                        class="w-[400px] h-[400px] bg-white relative top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2">
                        <div
                            class="w-[200px] h-[200px] bg-black relative top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 flex items-center justify-center">
                            <p class="text-white">Translate</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <Snippets />
    </section>
</template>
