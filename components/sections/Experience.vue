<template>
  <div id="experience">
    <wx-dot />
    <h2>work experience</h2>
    <div class="experience-item">
      <wx-dot />
      <p class="date light">
        2020 -
      </p>
      <p class="jobtitle">
        React / React-Native Developer
      </p>
      <p class="company">
        Xanda Ltd
      </p>
      <p>
        <span style="font-weight: bold">
          Responsibilites:
        </span>
        Front end development of React and React Native apps working in close
        contact with back-end PHP developers and UI/UX Designers. Required to
        be a team player contributing to application design and architecture.
        A high ability to problem solve is required in my current role including
        researching the integration of in house and third party Api's into projects
        and presentation of data to end users. The role also requires proficiency in
        test driven development using Mocha with Chia Assertions.
      </p>
    </div>
    <div class="experience-item">
      <wx-dot />
      <p class="date light">
        2017 - 2020
      </p>
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
        consulting on website functionality & UX, Creation of wireframes and mockups, Coding and deployment of backend API's
        as well as front end websites. Deployment of assets to heroku and zeit, management of
        continuous delivery pipelines and deployment of features and hotfixes. Development
        of company desktop and mobile apps inluding the new CDN Desktop. Dealing with issues
        & bugs as well as production of promotional video content.
      </p>
    </div>
    <div class="experience-item">
      <wx-dot />
      <span class="date light">Sept 2012 - Apr 2017</span>
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
        Design of product labelling, logos and websites for clients and franchaisees,
        Product photography and product image optimization and upload for company website.
        Trouble shooting, website issues and application of fixed and patches for online shopping carts.
        Setup and managment of Adwords PPC, SEO optimization and creation and customization of website sales
        funnels in accordance with google analytics data.
      </p>
    </div>
    <div class="experience-item">
      <wx-dot />
      <span class="date light">Jul 2010 - Sept 2012</span>
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
        Implementation and support of Uk Wide Area Network, setup, config and support of company PBX VOIP telephone
        systems. Support of local area network of four UK offices including config and support of patch-panel, cisco
        routers and fibre-channel. Training of offshore network support contractors and assisting web team with deployment
        and network related issues. Authoring of technical documentation to provide indepth training material and continuity
        resources for future support contractors.
      </p>
    </div>
    <div class="experience-item">
      <wx-dot />
      <span class="date light">Jan 2009 - Apr 2010</span>
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
        To Manage and Provide technical leadership in deployment of hardware and software deliverables
        to the business. To design and implement software deployment infrastructure inline with established
        industry standards and to liaise with projects team to ensure smooth integration of new solutions
        into user environment. To test, package and deploy new software and updates to users and assist
        development team in delivery of software enhancements whilst providing change management and post
        deployment support & documentation.
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../../assets/scss/main.scss';
  .experience-item {
    // &:not(:first-child) {
    //   transform: translateY(20px);
    // }
    @media screen and (max-width: 414px) {
      transform: translateY(450px) !important;
      text-align: center;
    }
    @media screen and (max-width: 743px) {
      transform: translateY(-280px);
    }
    .experience-item {
      margin-top: 55px;
    }
  }
</style>
