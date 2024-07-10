<script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
<!--    <a href="">-->
<!--      <img :src= imagePath(imageVisible) class="logo vue" alt="Vue logo" />-->
<!--    </a>-->
<!--    <a href="">-->
<!--      <img :src= imagePath(imageNIR) class="logo vue" alt="Vue logo" />-->
<!--    </a>    -->
    <a href="">
      <img :src= imagePath(imageVisible) class="logo vue" alt="Vue logo" />
    </a>
    <a href="">
      <img src= "./assets/images/Лик Богородицы_NIR.jpg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  {{imagePath(imageVisible)}}
  <HelloWorld msg="Vite + Vue" />
</template>
<script>


export default {
  name: 'App',
  components: {},
  data() {
  return {
      baseURL: '/visible-nir/',
      prefixURL: './assets/images/',
      imageVisible: 'Лик Богородицы_Visible.jpg',
      imageNIR: 'Лик Богородицы_NIR.jpg'

    }
  },
  methods: {
    imagePath(v) {

      const raw = `./assets/images/${v}`;
      console.log('raw', raw);
      const result = raw;
      console.log('result', result);
      return result;
    },
  },
}

</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
