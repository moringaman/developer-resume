<template>
  <div id="contact">
    <h2>CONTACT</h2>
    <div class="contact-method">
      <div class="contact-method__circle">
        <fa :icon="['fas', 'map-marker-alt']" />
      </div>
      <div class="contact-method__heading">
        <h3>Location</h3>
        <p>
          London<br>
          England<br>
        </p>
      </div>
    </div>
    <div class="contact-method">
      <div class="contact-method__circle">
        <fa :icon="['fas', 'envelope']" />
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
        <fa :icon="['fas', 'phone-alt']" />
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
        <fa :icon="['fas', 'laptop-code']" />
      </div>
      <div class="contact-method__heading">
        <h3>Website</h3>
        <p>
          www.robduffus.co.uk
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../../assets/scss/main.scss';
#contact {
  margin-bottom: 130px;
  margin-top: 120px;
    @media screen and (max-width: 743px) {
      transform: translateY(190px);
    }
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
</style>
