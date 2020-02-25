<template>
    <div id="secure">
    <ul class="nav navbar-nav">
      <li><router-link :to="{ name: 'Secure' }">Home</router-link></li>
      <li><router-link :to="{ name: 'Home' }">App</router-link></li>
      <li><router-link :to="{ name: 'About' }">About</router-link></li>
    </ul>
        <h1>Login Area</h1>
        <p>
            You're Logged In
        </p>
    </div>
</template>


<script>
    export default {
        name: 'Secure',
    }
</script>

<style scoped>
    #secure {
        background-color: #FFFFFF;
        padding: 20px;
        margin-top: 10px;
    }
</style>