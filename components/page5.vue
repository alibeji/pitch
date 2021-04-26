<template>
  <div
    class="main"
    :class="{ passed: passingData > 5, upcoming: passingData < 5 }"
  >
    <h1>Page 5</h1>
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
.main.passed {
  top: -100vh;
}
.main.upcoming {
  top: 100vh;
}
</style>
