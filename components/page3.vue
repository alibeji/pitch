<template>
  <div
    class="main"
    :class="{ passed: passingData > 3, upcoming: passingData < 3 }"
  >
    <div class="illustration">
      <svg viewBox="0 0 182 166" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect x="9" width="173" height="166" fill="#0497AF" />
        <circle cx="17" cy="11" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="23" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="35" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="47" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="59" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="71" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="83" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="95" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="107" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="119" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="131" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="143" r="4" fill="#FDF9EE" />
        <circle cx="17" cy="155" r="4" fill="#FDF9EE" />
        <rect y="9" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="21" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="33" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="45" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="57" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="69" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="81" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="93" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="105" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="117" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="129" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="141" width="18" height="4" rx="2" fill="#C4C4C4" />
        <rect y="153" width="18" height="4" rx="2" fill="#C4C4C4" />
      </svg>
    </div>
    <h2>The Kid with a Sketchbook</h2>
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
.main .illustration svg {
  width: 500px;
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
