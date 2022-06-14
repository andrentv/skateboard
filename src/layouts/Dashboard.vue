<template>
  <div class="bg-gray-800 flex text-white max-h-screen h-screen">
    <div class="w-64">
      <span class="font-semibold p-6 block opacity-90">Skateboard</span>

      <nav class="p-6">
        <h3 class="opacity-50 uppercase font-semibold tracking-wider mb-6 text-xs">Menu</h3>
        <div class="space-y-6">
          <MenuItem :icon="HomeIcon">Discover</MenuItem>
          <MenuItem :icon="HomeIcon">Discover</MenuItem>
          <MenuItem :icon="TrendingUpIcon">Trending</MenuItem>
          <MenuItem :icon="TrendingUpIcon">Trending</MenuItem>
          <MenuItem :icon="TrendingUpIcon">Trending</MenuItem>
          <MenuItem :icon="TrendingUpIcon">Trending</MenuItem>
        </div>
      </nav>
    </div>
    <div class="flex-1 h-screen relative overflow-y-auto">
      <header class="flex p-5 bg-gray-800 z-20 sticky top-0 items-center justify-between">
        <InputSearch class="w-96" />

        <div class="flex items-center">

          <div class="flex items-center space-x-3">

            <Avatar class="rounded-full overflow-hidden w-10 h-10" />

            <span>Thomas</span>
            <ChevronDownIcon class="w-4 h-4" />
          </div>

          <BellIcon class="w-5 h-5 ml-8 opacity-50 hover:opacity-100 cursor-pointer transition duration-100" />
        </div>
      </header>
      <div class="px-5 pb-5 content">
        <h1 class="font-bold text-4xl mt-6 mb-4">Discover</h1>

        <div class="grid gap-4 grid-cols-12">
          <div class="rounded-3xl col-span-8 h-96 overflow-hidden relative">
            <div class="flex w-full h-full">
              <img src="https://cdn.pixabay.com/photo/2021/06/04/15/50/skateboarding-6310245__340.jpg"
                class="w-full object-cover" />
            </div>
            <div class="z-10 absolute top-0 p-6 w-full bottom-0">
              <h3 class="text-2xl max-w-xs">How to do Basic Jumping and how to landing safety</h3>
              <div class="absolute right-6 bottom-6 px-2 py-1 rounded-lg bg-gray-800 bg-opacity-50 text-white-700">7
                minutes</div>
            </div>
          </div>


          <div class="rounded-3xl col-span-4 h-96 overflow-hidden relative">
            <div class="flex w-full h-full">
              <img src="https://cdn.pixabay.com/photo/2014/10/22/08/38/skateboard-497706__340.jpg"
                class="w-full object-cover" />
            </div>
            <div class="z-10 absolute top-0 p-6 w-full bottom-0">
              <h3 class="text-2xl max-w-xs">How to do Basic Jumping and how to landing safety</h3>
              <div class="absolute right-6 bottom-6 px-2 py-1 rounded-lg bg-gray-800 bg-opacity-50 text-white-700">7
                minutes</div>
            </div>
          </div>

        </div>
        <h1 class="font-semibold text-2xl mt-6 mb-4">Most Watched</h1>




        <div class="grid gap-4 grid-cols-4">
          <CardItem v-for="n of 10" />
          <CardItem />
          <CardItem />
          <CardItem />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import HomeIcon from '../components/icons/HomeIcon.vue'
import TrendingUpIcon from '../components/icons/TrendingUpIcon.vue'
import MenuItem from './navs/MenuItem.vue'
import InputSearch from '../components/inputs/InputSearch.vue'
import ChevronDownIcon from '../components/icons/ChevronDownIcon.vue'
import BellIcon from '../components/icons/BellIcon.vue'
import Avatar from '../components/Avatar.vue'
import CardItem from '../components/CardItem.vue'
</script>
