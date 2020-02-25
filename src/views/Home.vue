<template>
  <div class="home">
    <ul class="nav navbar-nav">
      <li><router-link :to="{ name: 'Secure' }">Home</router-link></li>
      <li><router-link :to="{ name: 'Home' }">App</router-link></li>
      <li><router-link :to="{ name: 'About' }">About</router-link></li>
    </ul>
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
