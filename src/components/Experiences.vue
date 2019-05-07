<template>
  <section>
    <div class="experiences">
      <ScrollDown />
      <div class="dashedLine extended"></div>
      <NumberContainer num="4" />
      <h3 class="large u-space-top--xlarge ericTransEffect">
        <span>Unique </span> Experience.<br />
      </h3>
      <div class="grid">
        <div class="row">
          <div
            class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-6 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large ericTransEffect"
          >
            <img
              src="../assets/startups.jpg"
              alt="Lorem ipsum dolor sit amet"
            />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">STARTUPS<br /></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
                I've always had interest in developing a startup company. I have
                many ideas and passions. In the past I've attempted a few things
                as part of the Reverse Startups foundation. I'm still quite
                interested in planning my next big thing.
              </p>
            </div>
          </div>
          <div
            class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-6 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large ericTransEffect"
          >
            <img
              src="../assets/bitcoinsvHD.png"
              alt="Lorem ipsum dolor sit amet"
            />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Bitcoin SV<br /></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
                I've learning as much as I could about Bitcoin for years. I know
                quite a bit about it and how it will impact he world in the
                future. I'm heavily involved with work in it. Lots to learn,
                lots to experience, lots of fun.
              </p>
            </div>
          </div>
          <div
            class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-6 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large ericTransEffect"
          >
            <img
              src="../assets/hacking_hacker_computer_internet.jpg"
              alt="Lorem ipsum dolor sit amet"
            />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">
                Digital Forensics<br />
              </h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
                My friends like to joke that I'm Mr. Robot. I hate that show but
                I do enjoy learning about how to safeguard valuable information.
                Most valued information is moving into electronic form making
                this quite a valued skill.
              </p>
            </div>
          </div>
          <div
            class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-6 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large ericTransEffect"
          >
            <img
              src="../assets/watch_time_pocketwatch_white.jpg"
              alt="Lorem ipsum dolor sit amet"
            />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Investing<br /></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
                I know quite a bit about investing. I can't believe they don't
                teach this in school. Compound interest. "He who understands it,
                earns it; he who doesn't, pays it." -Einstein
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import ScrollDown from "@/components/ScrollDown.vue";
import NumberContainer from "@/components/NumberContainer.vue";

export default {
  name: "home",
  components: {
    ScrollDown,
    NumberContainer
  }
};
</script>

<style scoped lang="scss">
.experiences {
  max-width: 1000px;
  margin: 0 auto;
  .grid {
    // display: grid;
    // grid-template-columns: 1fr 1fr 1fr;
    margin: 0 20px;
    & .item {
      // margin: 5%;
      & > img {
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
