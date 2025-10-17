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
                I have always been passionate about developing a startup. With
                numerous ideas and interests, I have previously explored several
                concepts as part of the Reverse Startups foundation. I remain
                enthusiastic about planning my next big venture.
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
              <h3 class="montserratBold u-space-top">Bitcoin<br /></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
                I have been immersing myself in Bitcoin for years, gaining a
                deep understanding of its potential impact on the world. My
                involvement in this space is extensive, and I find it to be both
                an exciting journey and an ongoing learning experience. There’s
                always more to explore and discover.
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
                Artificial Intelligence<br />
              </h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
                I am deeply passionate about artificial intelligence and its
                transformative potential in various industries. I am committed
                to developing my expertise in machine learning, natural language
                processing, and data analysis. Understanding
                AI not only positions me at the forefront of technological
                advancements but also empowers me to contribute innovative
                solutions in a rapidly evolving landscape.
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
                I possess significant knowledge about investing, and I'm
                surprised this essential topic isn't taught in schools.
                Understanding compound interest is crucial: "He who understands
                it, earns it; he who doesn’t, pays it." - Einstein. I believe
                that financial literacy is key to building wealth.
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
