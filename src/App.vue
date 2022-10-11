<template>
  <Navbar/>
  <div>
    Operation insde html: 2+2={{2+2}}<br>
    String from a function: {{helloWorld()}}
  </div>
  <hr>
    <div :class="{'red': show, 'blue':!show}">
      Dinamic CSS (Bonus 5) - Works with the button
    </div>
  <hr>
  <button @click="changeShow()">Change me</button>
  <div v-if="show">The if is true</div>
  <div v-else>The if is false</div>

  <div v-show="show">The same but with v-show</div>
  <hr>
  <DataInfo/>
  <hr>
  <Footer/>
</template>
<script setup>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
import { ref } from 'vue';
import DataInfo from './components/DataInfo.vue';

let show = ref(true);

const helloWorld = ()=>{
  return "Hello World"
}
const changeShow = ()=>  show.value = !show.value
</script>
<style scoped>
.red{
  background-color: red;
}
.blue{
  background-color: blue;
}
</style>