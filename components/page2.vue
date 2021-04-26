<template>
  <div
    class="main"
    :class="{ passed: passingData > 2, upcoming: passingData < 2 }"
  >
    <div class="illustration">
      <svg viewBox="0 0 229 133" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect
          width="229"
          height="127"
          transform="matrix(1 0 0 -1 0 127)"
          fill="#0A092E"
        />
        <rect
          x="3"
          y="-3"
          width="223"
          height="121"
          transform="matrix(1 0 0 -1 0 121)"
          stroke="#E4DABC"
          stroke-width="6"
        />
        <rect
          x="3"
          y="-3"
          width="223"
          height="9"
          transform="matrix(1 0 0 -1 0 127)"
          stroke="#E4DABC"
          stroke-width="6"
        />
      </svg>
    </div>
    <h2>The Kid with a Computer</h2>
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
  position: relative;
}
.main .illustration svg {
  width: 500px;
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
