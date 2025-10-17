<template>
  <section>
    <div class="dashedLine"></div>
    <h4 class="nextTitle u-space-top--small">Who Am I?</h4>
    <ScrollDown />
    <div class="dashedLine extended"></div>
    <NumberContainer num="1" />
    <h3 class="large u-space-top--xlarge ericTransEffect">
      I'm <span>Eric Lima</span>, a skilled front-end developer dedicated to
      crafting powerful and engaging websites that make a difference.
    </h3>
    <Tetris class=" ericTransEffect" />
    <p class="u-space-top--large ericTransEffect">
      I am a passionate and dedicated web developer with extensive experience,
      having created hundreds of websites that collectively garner over a
      <span>million page views</span>. My projects range from interactive maps
      and statistics to valuable information platforms and more.
      <br />Throughout my career, I have worked with multiple programming
      languages, including <span>C, C++, C#, Java, JS, Ruby and Python</span>.
      Currently, my focus is primarily on JavaScript and web development, where
      I find the most fulfillment. My enthusiasm for programming inspired me to
      pursue a <span>Bachelors of Science degree in Computer Science</span> at
      the University of Massachusetts Lowell. This website showcases some of my
      best work and highlights my skills and dedication to the craft.
    </p>
    <p class="u-space-top--large ericTransEffect">
      Currently, I am working fulltime to build client websites. Here are some
      of my publicly release works. Many projects cannot be included because of
      Non-Disclosure Agreements.
    </p>
  </section>
</template>

<script>
import ScrollDown from '@/components/ScrollDown.vue';
import Tetris from '@/components/Tetris.vue';
import NumberContainer from '@/components/NumberContainer.vue';

export default {
  name: 'home',
  components: {
    ScrollDown,
    Tetris,
    NumberContainer,
  },
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
