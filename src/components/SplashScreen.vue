<template>
  <div :class="{ hiden: !isVisible, splashscreen: isVisible }">
    <img src="@/assets/cash-flow-app-icon.svg" alt="CashFlow Logo" />
    <h1><span>Cash</span>Flow</h1>
    <a class="get-started" @click="hideComponent()">Get Started</a>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const isVisible = ref(true)

const hideComponent = () => {
  isVisible.value = !isVisible.value
}
</script>

<style scoped>
.hiden {
  display: none;
}
.splashscreen {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  height: 100vh;
  animation: lazy-loading 1500ms linear;
  margin-top: 0px;
  opacity: 1;
}
@keyframes lazy-loading {
  0% {
    margin-top: 100px;
    opacity: 0.1;
  }
}

.get-started {
  padding: 8px 18px;
  border-radius: 8px;
  background-color: #b9efff;
  color: var(--brand-blue);
  cursor: pointer;
  font-weight: normal;
  transition: background-color 200ms ease;
}
.get-started:hover {
  background-color: #cbf3ff;
}
h1 {
  color: var(--brand-blue);
}
h1 span {
  color: var(--brand-green);
}
</style>
