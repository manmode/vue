<script setup>
import { ref } from 'vue';
let pageBackground = ref('#00000000');
let arrLetters = ref([
  'a','b','c'
]);
function changeColor() {
  pageBackground.value = '#' + Math.floor(Math.random() * 10000000).toString(16);
}
</script>

<template>
  <div id="app" class="app">
    {{ appName }}
    {{ pageBackground }}

    <button @click="changeColor()">Change Color</button>
    <div>
      <p>Message is: {{ pageBackground }}</p>
      <input v-model="pageBackground" placeholder="edit me" />
    </div>

    <div>
      arrLetters.map((item) => {
          {{ item }}  
        })
    </div>
</div>
</template>

<style scoped>
.app {
  font-size: 30px;
}
</style>
