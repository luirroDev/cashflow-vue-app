<template>
  <SplashScreen />
  <HomePage />
</template>

<script>
import HomePage from '@/components/HomePage.vue'
import { defineAsyncComponent } from 'vue'
export default {
  components: {
    HomePage,
    SplashScreen: defineAsyncComponent(
      () =>
        new Promise((resolve) => {
          setTimeout(() => {
            resolve(import('./components/SplashScreen.vue'))
          }, 1000)
        })
    )
  }
}
</script>

<style>
html,
body,
#app {
  min-height: 100vh;
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

* {
  --brand-green: #04b500;
  --brand-blue: #0689b0;
}
</style>
