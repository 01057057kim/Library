<script setup>

</script>

<template>
    <div class="bg-black bg-opacity-60 rounded-xl p-5 grid grid-cols-2">
        <div class="col-span-1">
            <h1 class="font-bold text-xl text-white">Desktop Nav Code:</h1>
            <pre class="w-auto h-[500px] overflow-auto rounded-l-xl border-2 border-white">
            <code class="text-white font-semibold">
&lt;nav class="flex justify-between items-center w-full px-5 py-2 mx-auto text-nowrap"&gt;
    &lt;div&gt;
        &lt;p class="text-2xl font-bold uppercase"&gt;logo&lt;/p&gt;
    &lt;/div&gt;
    &lt;div&gt;
        &lt;ul class="flex items-center gap-[4vw]"&gt;
            &lt;li&gt;
                &lt;a class="hover:text-gray-500 font-semibold" href="#"&gt;Home&lt;/a&gt;
            &lt;/li&gt;
            &lt;li&gt;
                &lt;a class="hover:text-gray-500 font-semibold" href="#"&gt;Products&lt;/a&gt;
            &lt;/li&gt;
            &lt;li&gt;
                &lt;a class="hover:text-gray-500 font-semibold" href="#"&gt;Pricing&lt;/a&gt;
            &lt;/li&gt;
            &lt;li&gt;
                &lt;a class="hover:text-gray-500 font-semibold" href="#"&gt;About Us&lt;/a&gt;
            &lt;/li&gt;
        &lt;/ul&gt;
    &lt;/div&gt;
    &lt;div&gt;
        &lt;button class="bg-red-500 text-white px-5 py-2 rounded-full hover:bg-opacity-80" type="text"&gt;
            Get Started&lt;
        /button&gt;
    &lt;/div&gt;
&lt;/nav&gt;
            </code>
        </pre>
        </div>
        <div class="col-span-1">
            <h1 class="font-bold text-xl text-white">Mobile Nav Code:</h1>
            <pre class="w-auto h-[500px] overflow-auto rounded-r-xl border-2 border-white">
                    <code class="text-white font-semibold p-2">
&lt;script setup&gt;
import { ref } from 'vue'
const show = ref(false)
&lt;/script&gt;

&lt;nav class="flex justify-between items-center w-full px-5 py-2 mx-auto text-nowrap"&gt;
    &lt;div v-if="show" class="absolute w-full h-screen left-0 top-0 bg-black bg-opacity-50"&gt;&lt;/div&gt;
    &lt;div class="flex gap-[4vw]"&gt;
        &lt;button @click="show = !show" type="text"&gt;
            &lt;img src="../assets/Images/menu.svg" alt="hamburger"&gt;
        &lt;/button&gt;
        &lt;p class="text-2xl font-bold uppercase"&gt;logo&lt;/p&gt;
    &lt;/div&gt;
    &lt;div v-if="show" class="absolute bg-white min-h-screen w-[25%] left-0 top-[0%] p-5"&gt;
        &lt;ul class="flex flex-col items-start gap-[3vw]"&gt;
            &lt;div&gt;
                &lt;button @click="show = false" type="text"&gt;
                    &lt;img src="../assets/Images/close.svg" alt="close"&gt;
                &lt;/button&gt;
            &lt;/div&gt;
            &lt;li&gt;
                &lt;a class="hover:text-gray-500 font-semibold" href="#"&gt;Home&lt;/a&gt;
            &lt;/li&gt;
            &lt;li&gt;
                &lt;a class="hover:text-gray-500 font-semibold" href="#"&gt;Products&lt;/a&gt;
            &lt;/li&gt;
            &lt;li&gt;
                &lt;a class="hover:text-gray-500 font-semibold" href="#"&gt;Pricing&lt;/a&gt;
            &lt;/li&gt;
            &lt;li&gt;
                &lt;a class="hover:text-gray-500 font-semibold" href="#"&gt;About Us&lt;/a&gt;
            &lt;/li&gt;
        &lt;/ul&gt;
    &lt;/div&gt;
    &lt;div&gt;
        &lt;button class="bg-red-500 text-white px-5 py-2 rounded-full hover:bg-opacity-80" type="text"&gt;
            Get Started&lt;/button&gt;
    &lt;/div&gt;
&lt;/nav&gt; 
                    </code>
                </pre>
        </div>
    </div>
</template>
