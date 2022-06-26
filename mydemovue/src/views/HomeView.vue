<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <button @click="setClick()">点击</button>
    <HomeView v-if="click===2"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  data(){
    return {
      click: 1
    }
  },
  methods: {
    setClick(){
      this.click++;
    }
  },
  components: {
    HelloWorld,
  },
};
</script>
