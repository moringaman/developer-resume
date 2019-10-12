<template>
<div>
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
  }
}
</script>