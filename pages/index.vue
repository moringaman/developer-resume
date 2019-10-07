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
        </div>
      </div>
      <div id="right-column">
        right column
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

body {
  margin: 0px;
}
.container {
  /* margin: 0 auto; */
  /* min-height: 100vh; */
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  /* margin-top: -50px; */
}

.header {
  background: url(/mountains.jpg);
  background-size: 100%;
  background-position: center 30%;
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
  left: 15vw;
  position: absolute;
  display: grid;
  grid-gap: 20px;
  margin-top: 320px;
  justify-items: left;
  grid-template-columns: 150px 450px;
  z-index: 15;
}

.name-header {
  grid-column: 2;
  transform: translateY(4px);
  font-size: 4rem;
  font-weight: 700;
}
.developer {
  grid-column: 2;
  transform: translateY(-79px);
  color: #0E4C6F;
  font-weight: 500;
  font-size: 2rem;
}

.header-avatar-frame {
  height: 150px;
  width: 150px;
  border: 1px solid #fff;
  background-color: #666;
  border-radius: 50%;
  /* box-shadow: 4px 4px 4px rgba(0,0,0, 0.2); */
}

.contact-method {
  display: grid;
  grid-gap: 50px;
  margin-top: 50px;
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
  grid-template-columns:  4fr 6fr;
}
#left-column {
  background-color: $mid-gray;
  height: 100vh;
}
 #left-column-content {
   margin-top: 330px;
   text-align: left;
   padding: 0 80px;
   border-right: solid 3px $dark-text-color;
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
  grid-column: 2;
  background-color: white;
  height: 100vh;
}
</style>
