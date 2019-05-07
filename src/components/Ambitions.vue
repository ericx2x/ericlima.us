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
                Trying to use my spare time to tackle some leetcode problems.
                Always feel the need to brush up my skillset.
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
                I love competition. If you ever challenge me to a convinent game
                of anything I will be sure to accept.
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
                I love making code come to life. There's always a new technique
                learn to do something different.
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
                I'm aiming to read 1000 books in the next 10 years. Hopefully I
                undercut that by quite a bit. I never want to stop learning. I
                believe in the Red Queen's race.
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
import ScrollDown from "@/components/ScrollDown.vue";
import NumberContainer from "@/components/NumberContainer.vue";
import BigCircle from "@/components/BigCircle.vue";

export default {
  name: "home",
  components: {
    ScrollDown,
    NumberContainer,
    BigCircle
  },
  props: {
    resume: String
  }
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
