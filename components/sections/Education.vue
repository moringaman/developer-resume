<template>
  <div id="education">
    <h2>Education</h2>
    <div class="education-venue">
      <h3 class="qualification">
        Degree
      </h3>
      <h3>
        Business Economics (Bsc)
      </h3>
      <p>Thames Valley University (1993 - 1996)</p>
    </div>
    <div class="education-venue">
      <h3 class="qualification">
        A levels
      </h3>
      <h3>
        French, History, Economics
      </h3>
      <p>Richard Huish College</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../../assets/scss/main.scss';
  #education {
    @media screen and (max-width: 414px) {
      transform: translateY(440px) !important;
      text-align: center;
    }
    @media screen and (max-width: 743px) {
      transform: translateY(180px);
    }
    height: 780px;
    .education-venue {
      margin-top: 50px;
    }
  }
</style>
