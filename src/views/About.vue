<template>
  <div class="about">
    <ul class="nav navbar-nav">
      <li><router-link :to="{ name: 'Secure' }">Home</router-link></li>
      <li><router-link :to="{ name: 'Home' }">App</router-link></li>
      <li><router-link :to="{ name: 'About' }">About</router-link></li>
    </ul>
    <h1>This is an about page</h1>
  </div>
</template>
