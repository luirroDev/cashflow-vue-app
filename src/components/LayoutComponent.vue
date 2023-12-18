<template>
  <div class="header">
    <slot name="header"></slot>
  </div>
</template>

<style scoped>
.header,
.resume,
.movements {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 14px 0;
}
.header {
  position: fixed;
  width: 100vw;
}
</style>
