<template>
  <div class="skill">
    <div class="skill-name">
      {{ skill.name }}
    </div>
    <div class="skill-line" />
    <div class="skill-line-bar" :style="{ width: skill.value + '%' }" />
  </div>
</template>

<script>
export default {
  props: {
    skill: {
      type: Object,
      default: () => {
        return {}
      }
    }
  },
  data () {
    return {
      skillValueAccumulator: 0
    }
  },
  mounted () {
    this.moveBar(1000, this.skill.value, this.skillValueAccumulator)
  },
  methods: {
    moveBar (interval, originalVal, current) {
      this.skill.value = current
      if (this.skill.value === originalVal) {
        return
      }
      setInterval(() => {
        if (this.skill.value < originalVal) {
          this.skill.value++
          current++
        }
      }, interval)
      console.log(current, originalVal, this.skill.value)
      this.moveBar(interval -= 10, originalVal, current)
    }
  }
}
</script>

<style lang="scss">
@import '../../assets/scss/main.scss';
  .skill {
    display: grid;
    -webkit-display: grid;
    width: 100%;
    grid-template-columns: 80px 1fr 50px;
    // grid-gap: 10px;
    margin-top: -8px;
    align-items: center;
    &-line {
      grid-column: 2;
      width: 100%;
      height: 4px;
      // margin-top: 2px;
      background-color: $mid-gray;
      &-bar {
        // width: 70%;
        background-color: $highlight-text-color;
        height: 4px;
        transform: translateY(-14px);
        grid-column: 2;
      }
    }
    p {
      grid-column: 3;
      grid-row: 1;
    }
    &-name {
      grid-column: 1;
    }
  }
</style>
