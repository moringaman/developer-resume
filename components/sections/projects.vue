<template>
  <div id="project-work">
    <h2 id="project-work-title">
      Recent Projects
    </h2>
    <div class="project-item">
      <p class="skill-name">
        Technologies
      </p>
      <div class="project-item__right" />
      <div class="project-item__left">
        <div class="project-item__left--tech">
          <p
            v-for="(tech, key) in projects[selected].tech"
            :key="key"
            class="skill-name"
          >
            {{ tech }}
          </p>
        </div>
        <div class="project-item__left--description" />
        <div class="project-item__left--frame" :style="{'background-image': 'url(/'+ projects[selected].thumb + ')'}">
          <a :href="projects[selected].url" target="_blank">
            <div class="project-item__left--frame-overlay">
              {{ projects[selected].desc }}
              <div id="link">
                <fa
                  :icon="['fas', 'external-link-alt']"
                />
              </div>
            </div>
          </a>
          <!-- <img src="/scampz.png" alt=""> -->
        </div>
        <div class="project-item__left--list">
          <ul>
            <li
              v-for="(project, index) in projects"
              :key="index"
              :class="{active: index == selected}"
              @click="selected = index"
            >
              <p
                :class="{highlight: index == selected}"
                style="color: white"
              >
                {{ project.title }}
              </p>
            </li>
          </ul>
        </div>
        <div class="project-item__buttons">
          left right
        </div>
      </div>
    </div>
    <p id="project-note">
      The above selection of projects shows my versitility as both a designer and programmer.
      I am adebt at creating in various styles and to a design brief. Solving a wide range of problems.
    </p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      projects: [
        { title: 'CDN Desktop', url: 'http://cadence-desktop.com', thumb: 'cdndesktop.png', desc: 'A desktop app written in Vue and Electron', tech: [ 'html', 'javascript', 'vuejs', 'nodejs', 'electron', 'firebase', 'sass', 'couchdb', 'REST' ] },
        { title: 'Scampz music', url: 'http://scampz-music.herokuapp.com', thumb: 'scampz.png', desc: 'A pwa with music player, showcasing a grime artist', tech: [ 'html', 'javascript', 'nuxtjs', 'sass', 'pwa' ] },
        { title: 'Onset travel', url: 'http://onset-travel-client.herokuapp.com', thumb: 'onset.png', desc: 'A travel website with weather and qoute calculator', tech: [ 'html', 'javascript', 'vuejs', 'nodejs', 'sass', 'REST' ] },
        { title: 'CDN-Desktop Website', url: 'http://cadence-desktop.com', thumb: 'cdnweb.png', desc: 'App support & sales Website with Stripe subscriptions', tech: [ 'html', 'javascript', 'nuxt', 'nodejs', 'sass', 'REST', 'firebase', 'Stripe API' ] },
        { title: 'Video Commercial', url: 'http://cadence-desktop.com', thumb: 'video.png', desc: 'Promotional video & app showcase with voiceover', tech: ['video', 'voice', 'kdenlive', 'handbreak'] },
        { title: 'Q-DSK Mobile', url: 'http://cadence-desktop.com', thumb: 'Q-DSK2.png', desc: 'A GeoApp made with Vuejs + Quasar + Cordova', tech: [ 'html', 'javascript', 'Vuejs', 'Cordova', 'Quasar', 'Phonegap', 'Firebase' ] },
        { title: 'AFK Kickboxing Website', url: 'http://afk-kickboxing.herokuapp.com', thumb: 'afk.png', desc: 'Martial Arts website, with fancy graphics', tech: [ 'html', 'javascript', 'Vuejs', 'pwa', 'sass', 'gimp' ] }
      ],
      selected: 0
    }
  },
  watch: {
    selected (val) {
      if (val === 6) {
        const vm = this
        setTimeout(() => {
          vm.cycle()
        }, 3000)
      }
    }
  },
  created () {
    this.cycle()
  },
  methods: {
    cycle () {
      const vm = this
      this.projects.forEach(function (item, index, array) {
        // set a timeout so each second one button gets clicked
        setTimeout((function (index) {
          return function () {
            vm.selected = index
          }
        }(index)), (3000 * index))
      })
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/main.scss';
  #project-work {
    @media screen and (max-width: 743px) {
      transform: translateY(-280px);
    }
    @media screen and (max-width: 1407) {
      height: 700px;
    }
    .highlight {
      transition: all 0.3s ease-in;
      color: $highlight-text-color !important;
    }
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
        grid-template-columns: 2fr 1fr 2.4fr;
        grid-template-rows: 200px 50px;
        justify-content: right;
        // border-top: 1px solid $dark-text-color;
        transition: all 0.3s ease-in;
        &--tech {
          margin-top: 5px;
          display: flex;
          flex-wrap: wrap;
          align-content: flex-start;
          align-content: top;
          // display: grid;
          // grid-auto-rows: 20px;
          // grid-gap: 5px;
          // grid-template-columns: repeat(auto-fill, minmax(60px, 1fr));
          p {
            background-color: $light-gray;
            // font-size: 0.7rem;
            line-height: 27px;
            padding: 0 8px;
            border-radius: 3px;
            margin: 5px;
            // height: 20px;
          }
        }
        &--frame {
          background-color: $highlight-text-color;
          width: 220px;
          height: 120%;
          grid-column: 2;
          grid-row: 1;
          padding: 20px;
          transform: translate(-1px, -20px);
          box-shadow: 4px 6px 16px rgba($dark-text-color, 0.2);
          overflow: hidden;
          background-size: cover;
          // transition: all 0.2s ease-in;
        &-overlay {
          width: 180px;
          height: 220%;
          z-index: 2000;
          grid-column: 2;
          grid-row: 1;
          background-color: $highlight-text-color;
          transform: translate(-20px, 130px);
          opacity: 0.8;
          transition: all 0.3s ease-in;
          padding: 10px 10px;
          color: #fff;
          font-weight: 600;
          cursor: pointer;
          &:hover #link {
            opacity: 0.9;
          }
          #link {
            // transform: translateY(-100px);
            left: 189px;
            top: -150px;
            z-index: 6000;
            font-size: 1.2rem;
            opacity: 0.1;
            padding: 0px 5px;
            position: absolute;
            background-color: rgba(0, 0, 0, 0.5);
            transition: opacity 0.3s ease-in-out ;
          }
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
          // padding-top: 10px;
          transform: translateX(-20px);
          width: 120%;
          grid-column: 3;
          grid-row: 1;
          li {
            padding: 5px 5px;
            cursor: pointer;
            transition: all 0.3s ease-in;
          }
            .active {
              color: $highlight-text-color !important;
              background-color: $mid-gray;
            }
        }
      }
      &__buttons {
        grid-column: 2;
        margin-left: 50%;
        transform: translateX(-50%);
        visibility: hidden;
        // color: white;
      }
    }
  }
  #project-note {
    transform: translateY(-80px);
  }
</style>
