<template>
  <div>
    <div id="section-1" class="container">
      <div id="excerpt">
        A javascript developer with over 17 years experience in the tech space. Having performed such roles
        as application packager, network administrator and webmaster and having tought myself javascript
        development, I bring an almost uniqe and broad range of skills and knowledge to the table. I am
        passionate about programming and web technologies in general. I’m familiar with agile development
        methodologies , git-flow and git as well as various test driven development workflows.
      </div>
      <div id="left-column">
        <div id="left-column-content">
          <wx-skillset :skills="skills" />
          <wx-contact />
          <wx-education />
        </div>
      </div>
      <div id="right-column">
        <div id="right-column-content">
          <wx-experience />
          <wx-projects />
        </div>
      </div>
    </div>
    <wx-footer />
  </div>
</template>

<script>

export default {
  layout: 'default',
  data () {
    return {
      skills: [
        {
          name: 'html',
          value: 90
        },
        {
          name: 'css',
          value: 85
        },
        {
          name: 'javascript',
          value: 86
        },
        {
          name: 'nodejs',
          value: 76
        },
        {
          name: 'React',
          value: 91
        },
        {
          name: 'vuejs',
          value: 85
        },
        {
          name: 'solidity',
          value: 61
        },
        {
          name: 'linux',
          value: 90
        },
        {
          name: 'php',
          value: 34
        },
        {
          name: 'sveltejs',
          value: 76
        },
        {
          name: 'docker',
          value: 56
        },
        {
          name: 'Photoshop',
          value: 89
        },
        {
          name: 'figma',
          value: 76
        },
        {
          name: 'git',
          value: 89
        },
        {
          name: 'vim',
          value: 93
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import '../assets/scss/main.scss';
#section-1 {
  display: grid;
  grid-template-columns:  3.5fr 6.5fr;
  @media screen and (max-width: 1200px) {
    grid-template-columns: repeat(auto-fit, minmax(370px, 1fr));
  }
}
#left-column {
  background-color: $light-gray;
  height: 2600px;
    @media screen and (max-width: 1407px) {
      height: 2700px;
    }
    @media screen and (max-width: 743px) {
      height: 2100px;
    }
    @media screen and (max-width: 1205px) and (min-width: 743px) {
      height: 3300px;
    }
    @media screen and (max-width: 954px) and (min-width: 743px) {
      height: 3800px;
    }
}
 #left-column-content {
   margin-top: 362px;
   text-align: left;
   padding: 0 80px;
   border-right: solid 3px $dark-text-color;
   h2 {
     transform: translateY(-7px);
   }
 }
 #excerpt {
   position: absolute;
   top: 120px;
   width: 100%;
   padding: 0 80px;
   text-align: left;
   font-style: italic;
   font-size: 1.2rem;
   line-height: 1.9rem;
   font-weight: 400;
   color: $dark-text-color;
   column-count: 2;
    @media screen and (max-width: 537px) and (min-width: 10px) {
      column-count: 1;
    }
 }

#right-column {
  // grid-column: 3;
  background-color: white;
  height: 2600px;
  width: 100%;
    @media screen and (max-width) and (min-width: 357px) {
      height: 2400px;
    }
    @media screen and (max-width: 357px) {
      height: 4900px;
    }
    @media screen and (min-width: 358px) and (max-width: 743px) {
      height: 2200px !important;
    }
    @media screen and (max-width: 1407px) {
      height: 2700px;
    }
    @media screen and (max-width: 1205px) and (min-width: 743px) {
      height: 3300px;
    }
    @media screen and (max-width: 954px) and (min-width: 743px) {
      height: 3800px;
    }
  &-content {
    padding: 0 80px;
    margin-top: 330px;
  }
}
</style>
