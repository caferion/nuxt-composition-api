<template>
  <div class="  ">
<!--    <h3 class="text-2x">{{count}}</h3>-->
<!--    <button class="bg-blue-500 text-white font-bold w-20 rounded ml-2 hover:bg-blue-600"-->
<!--     @click="upCount">-->
<!--      +-->
<!--      </button>-->
<!--    <button class="bg-blue-500 text-white font-bold w-20 rounded ml-2" @click="downCount">-</button>-->
    <div class="flex items-start justify-center h-16 mt-4"><div class="relative"><input type="checkbox" class="w-12 border border-gray-300 rounded-full appearance-none cursor-pointer peer checked:border-gray-900 h-7"> <span class="absolute block w-5 h-5 transition-all duration-500 bg-gray-300 rounded-full pointer-events-none peer-checked:left-6 peer-checked:bg-gray-900 top-1 left-1"></span></div></div>
    <div class="relative">
      <input type="checkbox" v-model="temp" checked class="w-12 border border-gray-300 rounded-full appearance-none cursor-pointer peer checked:border-blue-900 h-7"/>
      <span class="absolute block w-5 h-5 transition-all duration-500 bg-gray-300 rounded-full pointer-events-none peer-checked:left-6 peer-checked:bg-gray-900 top-1 left-1">{{temp}}</span>
    </div>
    <div class="flex items-center mb-4">
      <input id="checkbox-1" aria-describedby="checkbox-1" type="checkbox" class="w-4 h-4 text-blue-600 bg-gray-100 rounded border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"" checked>
      <label for="checkbox-1" class="ml-3 text-sm font-medium text-gray-900 dark:text-gray-300">I agree to the <a href="#" class="text-blue-600 hover:underline dark:text-blue-500">terms and conditions</a></label>
    </div>
    <ul class="py-3 bg-gray-100 rounded-xl">
      <li>
        <span class="block px-5 py-1 text-xs text-gray-400 font-bold">Menu Title</span>
      </li>
      <li><a class="block px-5 py-3 rounded-lg text-gray-900 hover:bg-gray-200 focus:bg-indigo-500 focus:text-white outline-none cursor-pointer">First Menu Item</a></li>
      <li><a class="block px-5 py-3 rounded-lg text-gray-900 hover:bg-gray-200 focus:bg-indigo-500 focus:text-white outline-none cursor-pointer">Second Menu Item</a></li>
      <li><a class="block px-5 py-3 rounded-lg text-gray-900 hover:bg-gray-200 focus:bg-indigo-500 focus:text-white outline-none cursor-pointer">Third Menu Item</a></li>
    </ul>
    <div class="flex justify-center">
      <div class="form-check form-switch">
        <input class="form-check-input appearance-none w-9 -ml-10 rounded-full float-left h-5 align-top bg-white bg-no-repeat bg-contain bg-gray-300 focus:outline-none cursor-pointer shadow-sm" type="checkbox" role="switch" id="flexSwitchCheckDefault">
        <label class="form-check-label inline-block text-gray-800" for="flexSwitchCheckDefault">Default switch checkbox input</label>
      </div>
    </div>


  </div>
</template>

<script lang="ts">
import {defineComponent, ref} from '@nuxtjs/composition-api';

export default defineComponent({
  setup() {
    let count = ref(0)
    const temp = ref(true)

    const upCount = () => count.value++;
    const downCount = () => count.value--;

    return {
      temp,
      count,
      upCount,
      downCount
    }
  }
})
</script>
<style>

</style>
