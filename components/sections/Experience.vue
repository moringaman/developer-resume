<template>
  <div id="experience">
    <wx-dot />
    <h2>work experience</h2>
    <div class="experience-item">
      <wx-dot />
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
      <wx-dot />
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
      <wx-dot />
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
      <wx-dot />
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
</template>

<style lang="scss" scoped>
@import '../../assets/scss/main.scss';
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
</style>
