<template>
  <div
    id="footer"
    class="container"
  >
    <button id="hire-me">
      HIRE ME
    </button>
    <p
      id="available"
      class="job-title"
    >
      Available for both permanent and contract roles
    </p>
  </div>
</template>

<style lang="scss" scoped>
@import '../assets/scss/main.scss';
 #footer {
   height: 200px;
   width: 100%;
   background-color: $dark-text-color;
   color: $highlight-text-color;
   padding: 30px 80px;
    #available {
      margin-top: 10px;
      margin-left: 50%;
      display: inline-block;
      transform: translateY(-40px) translateX(-50%);
      color: $highlight-text-color;
    }
 }
 #hire-me {
   position: relative;
   margin: 50px 50%;
   transform: translateX(-50%);
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
