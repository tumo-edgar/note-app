<template>
  <div v-for="pix in arr">
     <PixCounter v-if="pix.age <= 10" :name="pix.name" :age="pix.age" :count="pix.count" />
  </div>
 

  <RouterView />
</template>

<script setup>
import { RouterView } from 'vue-router'
import PixCounter from './components/PixCounter.vue'
import { ref } from 'vue';

const arr = ref([
  {
    name: 'Luna',
    age: 5,
    count: 2
  },
  {
    name: 'John',
    age: 12,
    count: 34
  },
  {
    name: 'Aaaa',
    age: 3,
    count: 5
  },

])

</script>

<style scoped></style>
