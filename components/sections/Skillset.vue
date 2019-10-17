<template>
  <div id="skillset">
    <h2>skillset</h2>
    <div v-for="skill in skills" :key="skill.name">
      <wx-skill :skill="skill" />
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
#skillset {
  // margin-bottom: 100px;
    @media screen and (max-width: 414px) {
      transform: translateY(520px) !important;
      margin: 200px auto;
      text-align: center;
    }
    @media screen and (max-width: 537px) and (min-width: 414px) {
      transform: translateY(220px);
    }
    @media screen and (max-width: 743px) and (min-width: 537px) {
      transform: translateY(80px);
    }
}
</style>
