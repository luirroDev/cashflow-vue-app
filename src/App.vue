<template>
  <SplashScreen></SplashScreen>
  <HomePage></HomePage>
</template>

<script setup>
import HomePage from './components/HomePage.vue'
import SplashScreen from './components/SplashScreen.vue'
</script>

<style>
html,
body,
#app {
  min-height: 100vh;
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  box-sizing: border-box;
}

* {
  --brand-green: #04b500;
  --brand-blue: #0689b0;
}
</style>
