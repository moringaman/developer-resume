<template>
  <div class="skill">
    <div class="skill-name">
      {{ skill.name }}
    </div>
    <div class="skill-line" />
    <div class="skill-line-bar" :style="{ width: skill.value + '%' }" />
    <p class="light">
      {{ skill.value }}%
    </p>
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
      skillValueAccumulator: 0,
      skillLevel: this.skill.value
    }
  },
  created () {
    this.skill.value = 0
    this.moveBar()
  },
  methods: {
    moveBar () {
      let interval = 8
      setInterval(() => {
        if (this.skill.value < this.skillLevel) {
          this.skill.value++
          interval--
        }
      }, interval)
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
    grid-template-columns: 85px 1fr 50px;
    // grid-gap: 10px;
    margin-top: -8px;
    align-items: center;
    @media screen and (max-width: 414px) {
      text-align: left;
    }
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
