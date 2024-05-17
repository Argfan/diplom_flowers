<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue'

const date = ref('')

const selectedCity = ref();
const cities = ref([
    { name: 'New York', code: 'NY' },
    { name: 'Rome', code: 'RM' },
    { name: 'London', code: 'LDN' },
    { name: 'Istanbul', code: 'IST' },
    { name: 'Paris', code: 'PRS' }
]);


</script>



<template>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
  <Calendar v-model="date" />

  <div class="card flex justify-center">
        <Dropdown v-model="selectedCity" :options="cities" optionLabel="name" placeholder="Select a City" class="w-full md:w-[14rem]" />
    </div>
</template>

<style scoped>

</style>
