<template>
  <div class="container">
    <header class="header">
      <wx-socialicons />
      <div id="overlay" />
      <div class="container">
        <div id="developer-info">
          <div class="header-avatar-frame" />
          <div class="name-header">
            ROB DUFFUS
          </div>
          <div class="developer">
            Full Stack Software Engineer
          </div>
        </div>
      </div>
    </header>
    <!-- <a href="https://github.com/moringaman" target="_blank">
      <img id="github" src="github-brands.svg" alt="github">
    </a> -->
  </div>
</template>

<style lang="scss" scoped>

@import '../assets/scss/main.scss';
// #github {
//   position: absolute;
//   width: 40px;
//   top: 20px;
//   right: 20px;
//   z-index: 9000;
//   cursor: pointer;
// }
.container {
  /* margin: 0 auto; */
  /* min-height: 100vh; */
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  // overflow-X: hidden;
  /* margin-top: -50px; */
}

.header {
  background: url(/mountains.jpg);
  background-size: cover;
  background-position: center 200%;
  background-attachment: fixed;
  background-repeat: no-repeat;
  width: 100%;
  min-height: 300px;
  margin-top: 0px;
  color: #fff;
}

#overlay {
  height: 100%;
  position: absolute;
  z-index: 10;
  background-color: $dark-text-color;
  width: 100%;
  height: 300px;
  opacity: 0.5;
}

#developer-info {
  left: 11vw;
  position: absolute;
  display: grid;
  grid-gap: 20px;
  // margin-top: 20rem;
  transform: translateY(320px);
  justify-items: left;
  grid-template-columns: 150px 550px;
  z-index: 15;
}

.name-header {
  grid-column: 2;
  transform: translateY(4px);
  font-size: 4rem;
  font-weight: 700;
    @media screen and (max-width: 414px) {
      font-size: 1.8rem;
    transform: translateY(43px);
    }
}
.developer {
  grid-column: 2;
  transform: translateY(-79px);
  color: #0E4C6F;
  font-weight: 500;
  font-size: 2rem;
    @media screen and (max-width: 414px) {
      font-size: 1rem;
      transform: translateY(-75px);
      width: 200px;
      text-align: left !important;
      font-weight: 600;
    }
}

.header-avatar-frame {
  height: 150px;
  width: 150px;
  border: 1px solid #fff;
  background-color: #666;
  border-radius: 50%;
  background: url(/avatar.jpg);
  background-size: 120%;
  background-position: 25% 31%;
  /* box-shadow: 4px 4px 4px rgba(0,0,0, 0.2); */
}
</style>
