<template>
  <section>
    <div class="languages">
      <ScrollDown />
      <div class="dashedLine extended"></div>
      <NumberContainer num="3" />
      <h3 class="large u-space-top--xlarge ericTransEffect">
        What <span>technologies</span> <br />
        do I prefer?<br />
      </h3>
      <div class="grid">
        <div class="row">
          <div
            class="item col-xs-12 col-xs-offset-0 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-0 col-lg-4 col-lg-offset-0 u-space-top--large ericTransEffect"
          >
            <div class="overlayImg"></div>
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Typescript<br /></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
                I have always been an admirer of TypeScript, an advanced version
                of JavaScript that introduces static typing for improved code
                quality and maintainability. But I also know many other languages like RoR, C-styled, or Python.
              </p>
            </div>
          </div>
          <div
            class="item col-xs-12 col-xs-offset-0 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-0 col-lg-4 col-lg-offset-0 u-space-top--large ericTransEffect"
          >
            <div class="overlayImg"></div>
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">React<br /></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
                React is ubiquitous on the web, allowing for dynamic data
                updates without the need for a full page reload.
              </p>
            </div>
          </div>
          <div
            class="item col-xs-12 col-xs-offset-0 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3 col-lg-4 col-lg-offset-0 u-space-top--large ericTransEffect"
          >
            <div class="overlayImg"></div>
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Vue<br /></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
                This is another single-page application, which I find more
                approachable than React. It was developed using Vue.js.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import ScrollDown from '@/components/ScrollDown.vue';
import NumberContainer from '@/components/NumberContainer.vue';

export default {
  name: 'home',
  components: {
    ScrollDown,
    NumberContainer,
  },
};
</script>

<style scoped lang="scss">
.languages {
  max-width: 1000px;
  margin: 0 auto;
  .grid {
    margin: 0 20px;
    // display: grid;
    // grid-template-columns: 1fr 1fr 1fr;
    & .item {
      // margin: 5%;
      .overlayImg {
        width: 230px;
        height: 230px;
        margin: auto;
        border-radius: 50%;
        background: url('../assets/ruby.png') center no-repeat,
          url('../assets/bg-blue-noise.png');
        // background-repeat: no-repeat;
      }
      &:nth-of-type(2) {
        .overlayImg {
          background: url('../assets/react.png') center no-repeat,
            url('../assets/bg-blue-noise.png');
          background-size: 80%;
        }
      }
      &:nth-of-type(3) {
        .overlayImg {
          background: url('../assets/vue.png') center no-repeat,
            url('../assets/bg-blue-noise.png');
          background-size: 70%;
        }
      }
      & img {
        width: 100%;
      }
      & > .paragraphContent {
        // width: 230px;
        // margin: 20px auto;
      }
    }
  }

  @media only screen and (min-width: 75em) {
  }
  @media only screen and (min-width: 64em) {
  }
  @media only screen and (min-width: 48em) {
  }
}
</style>
