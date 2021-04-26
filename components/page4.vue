<template>
  <div
    class="main"
    :class="{ passed: passingData > 4, upcoming: passingData < 4 }"
  >
    <div class="illustration">
      <img src="/canvas.svg" />
    </div>
    <h2>The Kid behind the Canvas</h2>
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
.main .illustration {
  width: 500px;
  height: fit-content;
  position: relative;
  z-index: 1;
}
.main .illustration img {
  width: 400px;
  position: relative;
}
.main h2 {
  position: absolute;
  bottom: 2rem;
}
.main.passed {
  top: -100vh;
}
.main.upcoming {
  top: 100vh;
}
</style>
