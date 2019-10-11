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
          <div id="contact">
            <h2>CONTACT</h2>
            <div class="contact-method">
              <div class="contact-method__circle">
                A
              </div>
              <div class="contact-method__heading">
                <h3>Address</h3>
                <p>
                  8b Ringstead Rd<br>
                  Catford London<br>
                  SE6 2BP
                </p>
              </div>
            </div>
            <div class="contact-method">
              <div class="contact-method__circle">
                @
              </div>
              <div class="contact-method__heading">
                <h3>Email</h3>
                <p>
                  rob@webnostix.co.uk
                </p>
              </div>
            </div>
            <div class="contact-method">
              <div class="contact-method__circle">
                P
              </div>
              <div class="contact-method__heading">
                <h3>Phone</h3>
                <p>
                  +44 (0) 20 3005 9450
                </p>
              </div>
            </div>
            <div class="contact-method">
              <div class="contact-method__circle">
                W
              </div>
              <div class="contact-method__heading">
                <h3>Website</h3>
                <p>
                  www.robduffus.co.uk
                </p>
              </div>
            </div>
          </div>
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
              <p>Richard Huish College (Taunton)</p>
            </div>
          </div>
          <div id="projects">
            <h2>skillset</h2>
          </div>
        </div>
      </div>
      <div id="right-column">
        <div id="right-column-content">
          <div id="experience">
            <div class="dot dot-active" />
            <h2>work experience</h2>
            <div class="experience-item">
              <div class="dot" />
              <p class="jobtitle">
                Lead Javascript developer
              </p>
              <p class="company">
                Webnostix Design & Development Services
              </p>
              <p>
                <span style="font-weight: bold">
                  Responsibilites:
                </span>
                Design & Development of corporate identity and websites for clients,
                consulting on website functionality & UX, Coding and deployment of backend API's
                as well as front end websites.
              </p>
            </div>
            <div class="experience-item">
              <div class="dot" />
              <p class="jobtitle">
                Webmaster & Web designer
              </p>
              <p class="company">
                The MoringaMutual Trust / Wildmans Herbs
              </p>
              <p>
                <span style="font-weight: bold">
                  Responsibilites:
                </span>
                DesignDevelopment of corporate identity and websites for clients,
                consulting on website functionality & UX, Coding and deployment of backend API's
                as well as front end websites.
              </p>
            </div>
            <div class="experience-item">
              <div class="dot" />
              <p class="jobtitle">
                Network Administrator
              </p>
              <p class="company">
                Meltwater
              </p>
              <p>
                <span style="font-weight: bold">
                  Responsibilites:
                </span>
                DesignDevelopment of corporate identity and websites for clients,
                consulting on website functionality & UX, Coding and deployment of backend API's
                as well as front end websites.
              </p>
            </div>
            <div class="experience-item">
              <div class="dot" />
              <p class="jobtitle">
                Software Packager / Desktop Specialist
              </p>
              <p class="company">
                Sony Entertainment
              </p>
              <p>
                <span style="font-weight: bold">
                  Responsibilites
                </span>
                DesignDevelopment of corporate identity and websites for clients,
                consulting on website functionality & UX, Coding and deployment of backend API's
                as well as front end websites.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  layout: 'default'
}
</script>

<style lang="scss">
@import '../assets/scss/main.scss';

#contact {
  margin-bottom: 130px;
}
.contact-method {
  display: grid;
  grid-gap: 50px;
  margin-top: 60px;
  grid-template-columns: 90px 200px;
  &__circle {
    width: 90px;
    height: 90px;
    border-radius: 50%;
    background-color: $highlight-text-color;
    color: white;
    text-align: center;
    line-height: 90px;
    font-weight: 700;
    font-size: 2rem;
    // padding: auto auto;
  }
}

#section-1 {
  display: grid;
  grid-template-columns:  3.5fr 6.5fr;
  // grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  @media screen and (max-width: 1200px) {
    grid-template-columns: repeat(auto-fit, minmax(370px, 1fr));
  }
}
#left-column {
  background-color: $light-gray;
  height: 1800px;
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
 }

#right-column {
  // grid-column: 3;
  background-color: white;
  height: 1800px;
  width: 100%;
  &-content {
    padding: 0 80px;
    margin-top: 330px;
  }

  #experience {
    .experience-item {
      margin-top: 55px;
    }
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
  }
}

  #education {
    height: 400px;
    .education-venue {
      margin-top: 50px;
    }
  }
</style>
