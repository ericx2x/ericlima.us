<template>
  <section>
    <div class="ambitions">
      <ScrollDown />
      <div class="dashedLine extended"></div>
      <NumberContainer num="5" />
      <h3 class="large u-space-top--xlarge ericTransEffect">
        <span>Personal </span> Interests.<br />
      </h3>
      <div class="grid">
        <div class="row">
          <div
            class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-4 col-md-offset-0 col-lg-4 col-lg-offset-0 u-space-top--large ericTransEffect"
          >
            <div class="dashedLine"></div>
            <img
              src="../assets/LeetCode_logo.png"
              alt="Lorem ipsum dolor sit amet"
            />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Leetcode<br /></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
                I utilize platforms such as LeetCode to enhance my programming
                skills. By tackling a variety of challenges, I not only refine
                my technical abilities but also equip myself for real-world
                problem-solving scenarios.
              </p>
            </div>
            <div class="dashedLine"></div>
            <img
              src="../assets/chess_play_chess_game.png"
              alt="Lorem ipsum dolor sit amet"
            />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Gaming<br /></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
                I thrive in competitive environments and embrace challenges.
                Whether it's a strategic game or a coding competition, I’m
                always ready to rise to the occasion.
              </p>
            </div>
          </div>
          <div
            class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-4 col-md-offset-0 col-lg-4 col-lg-offset-0 u-space-top--large ericTransEffect"
          >
            <div class="dashedLine"></div>
            <img src="../assets/1948.png" alt="Lorem ipsum dolor sit amet" />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Design<br /></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
              I am passionate about bringing code to life, continually exploring new techniques to innovate and create unique solutions.
              </p>
            </div>
          </div>
          <div
            class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-4 col-md-offset-0 col-lg-4 col-lg-offset-0 u-space-top--large ericTransEffect"
          >
            <div class="dashedLine"></div>
            <img src="../assets/books.png" alt="Lorem ipsum dolor sit amet" />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Books<br /></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">
              My goal is to immerse myself in reading a diverse range of books over the next decade. I believe in the importance of lifelong learning and seek to cultivate my knowledge and perspective through literature. Reading not only enriches my mind but also fuels my passion for continuous growth.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <BigCircle :resume="this.resume" />
  </section>
</template>

<script>
import ScrollDown from '@/components/ScrollDown.vue';
import NumberContainer from '@/components/NumberContainer.vue';
import BigCircle from '@/components/BigCircle.vue';

export default {
  name: 'home',
  components: {
    ScrollDown,
    NumberContainer,
    BigCircle,
  },
  props: {
    resume: String,
  },
};
</script>

<style scoped lang="scss">
.dashedLine {
  height: 40px;
  margin-top: 20px;
}
.ambitions {
  max-width: 1000px;
  margin: 0 auto;
  .grid {
    // display: grid;
    // grid-template-columns: 1fr 1fr 1fr;
    margin: 0 20px;
    & .item {
      // margin: 5%;
      float: left;
      & > img {
        width: 100%;
      }
      & > .paragraphContent {
        // width: 230px;
        // margin: 20px auto;
      }
    }
  }
}

@media only screen and (min-width: 48em) {
  .ambitions {
    .grid {
      & .item {
        &:nth-of-type(2) {
          height: 500px;
          // height: auto;
        }
        &:nth-of-type(3) {
          margin-left: 50%;
          margin-top: -53%;
          // margin-left: 0;
        }
      }
    }
  }
}
@media only screen and (min-width: 64em) {
  .ambitions {
    .grid {
      & .item {
        &:nth-of-type(1) {
          img {
            &:nth-of-type(1) {
              margin-top: 20px;
              width: 80%;
            }
          }
        }
        &:nth-of-type(2) {
          height: auto;
          height: 500px;
          margin-top: 150px;
        }
        &:nth-of-type(3) {
          margin-left: 0;
          margin-top: 0px;
          height: 100%;
        }
      }
    }
  }
}
@media only screen and (min-width: 75em) {
  .ambitions {
    .grid {
      & .item {
      }
    }
  }
}
</style>
