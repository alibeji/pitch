<template>
  <div class="container" @click="push">
    <page1 :passing-data="reality" />
    <itpd :passing-data="reality" />
    <page2 :passing-data="reality" />
    <page3 :passing-data="reality" />
    <page4 :passing-data="reality" />
    <page5 :passing-data="reality" />
  </div>
</template>

<script>
import page1 from './../components/page1.vue'
import page2 from './../components/page2.vue'
import page3 from './../components/page3.vue'
import page4 from './../components/page4.vue'
import page5 from './../components/page5.vue'
import itpd from './../components/itpd.vue'
export default {
  components: {
    page1,
    itpd,
    page2,
    page3,
    page4,
    page5,
  },
  data() {
    return {
      reality: 1,
    }
  },
  mounted() {
    this._keyListener = function (e) {
      if (e.key === ' ' || e.key === 'Enter' || e.key === 'ArrowDown') {
        // e.key.length > 0 for any key
        e.preventDefault()

        this.push()
        setTimeout(3000)
      }
    }

    document.addEventListener('keyup', this._keyListener.bind(this))
  },
  methods: {
    push() {
      if (this.reality === 1) {
        this.reality = 2
      } else if (this.reality === 2) {
        this.reality = 3
      } else if (this.reality === 3) {
        this.reality = 4
      } else {
        this.reality = 5
      }
    },
  },
}
</script>

<style scoped>
.container {
  overflow: hidden;
  display: flex;
  flex-direction: row;
  width: 100%;
  align-items: flex-start;
  height: 100vh;
  overflow-y: hidden;
}
</style>
