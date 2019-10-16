<template>
  <div>
    <div
      id="top-nav"
      class="container"
      :style="{top: yPos}"
    >
      <div
        class="tab"
        :class="{active: active}"
      >
        <a
          ref="icon"
          href="https://github.com/moringaman"
          target="_blank"
        >
          <img
            id="github"
            src="github-brands.svg"
            alt="github"
          >
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      active: false,
      yPos: undefined
    }
  },
  mounted () {
    this.yPos = this.$refs.icon.offsetTop
    if (process.browser) {
      window.addEventListener('scroll', this.handleScroll)
    }
  },
  methods: {
    handleScroll () {
      // const YPos = this.yPos
      const windowY = window.scrollY
      this.yPos = windowY
      console.log(windowY)
      if (windowY > 280) {
        console.log(this.active)
        this.active = true
      } else {
        this.active = false
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/main.scss';
#top-nav {
  margin-top: 0px;
  width: 100%;
  // max-width:1345px;
  position: fixed;
  z-index: 1000;
  top: 0;
  background-color: transparent !important;
  .tab {
    z-index: 3000;
    width: 55px;
    height: 68px;
    float: right;
    border-radius: 5px;
    margin-right: 20px;
    transform: translateY(-5px);
  }
}
#github {
  position: relative;
  width: 40px;
  margin-top: 20px;
  // margin-left: 90%;
  cursor: pointer;
}

.active {
  background-color: $highlight-text-color;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.3);
}
</style>
