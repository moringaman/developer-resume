<template>
  <div>
    <div
      ref="dot"
      class="dot"
      :class="{'dot-active': active}"
    />
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
    this.yPos = this.$refs.dot.offsetTop
    if (process.browser) {
      window.addEventListener('scroll', this.handleScroll)
    }
  },
  methods: {
    handleScroll () {
      const YPos = this.yPos
      const windowY = window.scrollY
      if ((YPos - windowY < 200) && (YPos - windowY > 15)) {
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
    .dot {
      width: 20px;
      height: 20px;
      border-radius: 50%;
      background-color: white;
      border: 4px solid $dark-text-color;
      transform: translate(-91px, 31px);
      display: inline-block;
      &-active {
        background-color: $highlight-text-color;
        border: 4px solid $highlight-text-color;
      }
    }
</style>
