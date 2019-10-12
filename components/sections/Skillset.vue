<template>
  <div id="skills">
    <h2>skillset</h2>
    <div v-for="skill in skills" :key="skill.name" class="skill">
      <div class="skill-name">
        {{ skill.name }}
      </div>
      <div class="skill-line" />
      <div class="skill-line-bar" :style="{ width: skill.value + '%' }" />
      <!-- <p>{{ skill.value + '%' }}</p> -->
    </div>
  </div>
</template>

<script>
export default {
  props: {
    skills: {
      type: Array,
      required: true,
      default: () => {
        return []
      }
    }
  }
}
</script>

<style lang="scss" scoped>
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
