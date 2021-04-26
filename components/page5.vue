<template>
  <div
    class="main"
    :class="{ passed: passingData > 5, upcoming: passingData < 5 }"
  >
    <h1>The Grown Up applying for the MSc. in</h1>
    <div class="pencil-wrapper">
      <img src="/pencil.svg" />
    </div>
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
.main .pencil-wrapper {
  position: absolute;
  height: fit-content;
  width: 100%;
  right: 0;
  bottom: 2rem;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.main .pencil-wrapper img {
  width: 500px;
}
.main.passed {
  top: -100vh;
}
.main.upcoming {
  top: 100vh;
}
</style>
