<template>
  <div class="main" :class="{ inactive: passingData > 1 }">
    <h1>Pitch for the MSc. in</h1>
  </div>
</template>
<script>
export default {
  props: { passingData: Number },
}
</script>

<style scoped>
.main {
  height: 100vh;
  width: 100vw;
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: #1a1940;
  transition: ease all 1s;
  pointer-events: none;
}
.main.inactive {
  top: -100vh;
}
</style>
