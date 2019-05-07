<template>
  <section>
    <div class="dashedLine"></div>
    <h4 class="nextTitle u-space-top--small">Who Am I?</h4>
    <ScrollDown />
    <div class="dashedLine extended"></div>
    <NumberContainer num="1" />
    <h3 class="large u-space-top--xlarge ericTransEffect">
      I'm <span>Eric Lima</span>.<br />
      A web developer.
    </h3>
    <Tetris class=" ericTransEffect" />
    <p class="u-space-top--large ericTransEffect">
      I'm a passionate and dedicated web developer who has developed hundreds of
      different websites that have a combined total of over a
      <span>million page views</span>. Websites including maps, statistics,
      valued information and more. <br />Throughout my years, I've developed
      things in <span>C, C++, C#, Java, JS, Ruby, Python and more</span>. I'm
      more focused with JS and web development at the moment though. My love for
      programming lead me to pursue a
      <span>Bachelors of Science degree in Computer Science</span> at the
      University of Massachusetts Lowell. This website showcases some of my best
      work.
    </p>
    <p class="u-space-top--large ericTransEffect">
      Currently, I am working fulltime to build client websites. Here are some
      of my publicly release works. Many projects cannot be included because of
      Non-Disclosure Agreements.
    </p>
  </section>
</template>

<script>
import ScrollDown from "@/components/ScrollDown.vue";
import Tetris from "@/components/Tetris.vue";
import NumberContainer from "@/components/NumberContainer.vue";

export default {
  name: "home",
  components: {
    ScrollDown,
    Tetris,
    NumberContainer
  }
};
</script>

<style scoped lang="scss">
$white: #fff;
$pink: #f14189;
$blue: #1b98e0;
$darkBlue: #1e3446;
$lightGray: #ced1e4;
$darkGray: #444;
$black: #000;

section {
  max-width: 1005px;
  margin: 0 auto;
}

p {
  font-size: 1.2rem;
  line-height: 1.6rem;
  margin: 20px 20px 0 20px;
}

.scrollDownAnimation {
  position: relative;
  width: 100%;
  height: 100%;
}

@media only screen and (min-width: 75em) {
}
@media only screen and (min-width: 64em) {
}
@media only screen and (min-width: 48em) {
  p {
    font-size: 1.5rem;
    line-height: 1.9rem;
  }
}
</style>
