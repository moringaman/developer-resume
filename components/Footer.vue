<template>
  <div
    id="footer"
    class="container"
  >
    <a href="mailto: rob@webnostix.co.uk?subject=employment offer from a cool company">
      <button id="hire-me">
        HIRE ME
      </button>
    </a>
    <p
      id="available"
      class="job-title"
    >
      I'm currently available for both permanent and contract roles
    </p>
  </div>
</template>

<style lang="scss" scoped>
@import '../assets/scss/main.scss';
 #footer {
   height: 240px;
   width: 100%;
   background-color: #466576;
   color: $highlight-text-color;
   padding: 30px 80px;
   transform: translateY(-35px);
    @media screen and (max-width: 537px) and (min-width: 10px) {
      // transform: translateY(1500px);
      position: absolute;
      top: 6500px;
      margin: auto auto;
    }
    #available {
      margin-top: 10px;
      margin-left: 50%;
      display: inline-block;
      transform: translateY(-40px) translateX(-50%);
      color: #ffffff;
      text-align: center;
    }
 }
 #hire-me {
   position: relative;
   margin: 50px 50%;
   transform: translate(-50%, -10px);
   background-color: $highlight-text-color;
   display: inline-block;
   width: 200px;
   height: 60px;
   color: #fff;
   border-radius: 25px;
   font-size: 1.3rem;
   border: none;
   font-weight: 600;
   cursor: pointer;
   transition: all 0.3s ease-in;
   &:hover {
     filter: brightness(0.9);
   }
 }
</style>
