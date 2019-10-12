<template>
  <div id="project-work">
    <h2 id="project-work-title">
      Projects
    </h2>
    <div class="project-item">
      <p>project 1</p>
      <div class="project-item__right" />
      <div class="project-item__left">
        <div class="project-item__left--description" />
        <div class="project-item__left--frame" :style="{'background-image': 'url(/'+ projects[selected].thumb + ')'}">
        <div class="project-item__left--frame-overlay">{{ projects[selected].desc }}</div>
          <!-- <img src="/scampz.png" alt=""> -->
        </div>
        <div class="project-item__left--list">
          <ul>
            <li
              v-for="(project, index) in projects"
              :key="index"
              @click="selected = index"
            >
             <p style="color: white"> {{ project.title }} </p>
            </li>
          </ul>
        </div>
        <div class="project-item__buttons">
          left right
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      projects: [
        { title: 'Scampz music', url: 'http://scampz-music.herokuapp.com', thumb: 'scampz.png', desc: 'A progressive mobile app showcasing an artists music ' },
        { title: 'Onset travel', url: 'http://onset-travel-client.herokuapp.com', thumb: 'onset.png', desc: 'A travel website with weather and qoute calculator' },
        { title: 'CDN Desktop', url: 'http://cadence-desktop.com', thumb: 'scampz.png', desc: '' }
      ],
      selected: 0
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/main.scss';
  #project-work {
    margin-top: 120px;
    // overflow: hidden;
    width: 100%;
    float: right;
    left: 0px;
    // transform: translateX(20px);
    .project-item {
    height: 400px;
      &__right {
        background-color: $light-gray;
        width: 350px;
        height: 250px;
        float: right;
        transform: translateX(80px);
        overflow: hidden;
      }
      &__left {
        // background-color: #fff;
        width: 110%;
        height: 200px;
        // transform: translate(-190px, -270px);
        transform: translateY(-250px);
        display: grid;
        grid-gap: 20px;
        grid-template-columns: 1.5fr 1fr 2fr;
        grid-template-rows: 200px 50px;
        justify-content: right;
        border-top: 1px solid $dark-text-color;
        &--frame {
          background-color: $highlight-text-color;
          width: 220px;
          height: 120%;
          grid-column: 2;
          padding: 20px;
          transform: translate(-20px, -20px);
          box-shadow: 4px 6px 16px rgba($dark-text-color, 0.2);
          // background: url('/scampz.png');
          overflow: hidden;
          background-size: cover;
          transition: all 0.4s ease-in;
        &-overlay {
          width: 180px;
          height: 220%;
          z-index: 2000;
          grid-column: 2;
          background-color: $highlight-text-color;
          transform: translate(-20px, 130px);
          opacity: 0.8;
          transition: all 0.3s ease-in;
          padding: 10px 10px;
          color: #fff;
          font-weight: 600;
          cursor: pointer;
          &:hover {
            opacity: 1;
            // transform: translate(-5px, 50px) rotate(40deg);
          }
        }
        }
        &--description {
          padding: 10px 40px 10px 0px;
        }
        &--list {
          // margin-left: 10px;
          padding-top: 10px;
          li {
            height: 50px;
            cursor: pointer;
          }
        }
      }
      &__buttons {
        grid-column: 2;
        margin-left: 50%;
        transform: translateX(-50%);
        color: white;
      }
    }
  }
</style>
