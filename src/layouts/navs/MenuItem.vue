<template>
     <div class="flex items-center space-x-4">
          <div class="bg-orange-500 p-2 rounded-lg">
               <component :is="icon" class="w-4 h-4" />
          </div>
          <span>
               <slot></slot>
          </span>
     </div>
</template>

<script setup lang="ts">
import HomeIcon from "../../components/icons/HomeIcon.vue";
// import { defineProps } from 'vue';

defineProps({
     icon: { default: null },
});
//import TrendingUpIcon from '../../components/icons/TrendingUpIcon.vue'
</script>
