<template>
  <div class="home">
    <section>
      <ul class="scrollCircles">
        <li @click="scrollSec(1)"></li>
        <li @click="scrollSec(2)"></li>
        <li @click="scrollSec(3)"></li>
        <li @click="scrollSec(4)"></li>
        <li @click="scrollSec(5)"></li>
        <li @click="scrollSec(6)"></li>
      </ul>
      <div class="dashedLine"></div>
      <h1>Eric Lima</h1>
      <div class="dashedLine"></div>
      <div class="introContainer">
        <div class="introContent">
          <h2>Web Developer</h2>
          <h3>Crafting Stunning and Engaging User Experiences.</h3>
          <a :href="this.resume" target="_blank"
            >Click here to view my resume</a
          >
          <ul class="reList ul-nostyle clearfix">
            <li class="floatL">
              <a href="https://www.github.com/ericx2x" target="_blank"
                ><img src="../assets/github.png" alt="Git"
              /></a>
            </li>
            <li class="floatL">
              <a href="https://twitter.com/satoshilovesbsv" target="_blank"
                ><img src="../assets/twitter.png" alt="twitter"
              /></a>
            </li>
            <li class="floatL">
              <a
                href="https://www.linkedin.com/in/eric-lima-210b8812"
                target="_blank"
                ><img src="../assets/linkedin.png" alt="linkdin"
              /></a>
            </li>
          </ul>
          <Robot />
        </div>
      </div>
    </section>
    <WhoAmI />
    <Portfolio />
    <Languages />
    <Experiences />
    <Ambitions :resume="this.resume" />
  </div>
</template>

<script>
// @ is an alias to /src
import Robot from "@/components/Robot.vue";
import WhoAmI from "@/components/WhoAmI.vue";
import Languages from "@/components/Languages.vue";
import Experiences from "@/components/Experiences.vue";
import Ambitions from "@/components/Ambitions.vue";
import Portfolio from "@/views/Portfolio.vue";

export default {
  name: "home",
  components: {
    Robot,
    WhoAmI,
    Portfolio,
    Experiences,
    Ambitions,
    Languages
  },
  data() {
    return {
      resume:
        "https://docs.google.com/document/d/1uB6d2i2eycBKmjvY6cU8HXj7DhpMHLqGn8sApkyTX2A/edit?usp=sharing"
    };
  },
  mounted() {
    const scrollCircles = document.querySelectorAll(".scrollCircles > li");
    scrollCircles[0].classList.add("active");
  },
  methods: {
    scrollSec(num) {
      const homeSection = document.querySelectorAll(".home > section");
      const s1Height = homeSection[0].offsetHeight; //adding nav
      const s2Height = s1Height + homeSection[1].offsetHeight;
      const s3Height = s2Height + homeSection[2].offsetHeight;
      const s4Height = s3Height + homeSection[3].offsetHeight;
      const s5Height = s4Height + homeSection[4].offsetHeight;

      switch (num) {
        case 1:
          window.scrollTo(0, 0);
          break;
        case 2:
          window.scrollTo(0, s1Height + 400);
          break;
        case 3:
          window.scrollTo(0, s2Height + 400);
          break;
        case 4:
          window.scrollTo(0, s3Height + 400);
          break;
        case 5:
          window.scrollTo(0, s4Height + 400);
          break;
        case 6:
          window.scrollTo(0, s5Height + 400);
          break;
      }
    },
    handleScroll() {
      const trans = document.querySelectorAll(".ericTransEffect");
      const homeSection = document.querySelectorAll(".home > section");
      const scrollCircles = document.querySelectorAll(".scrollCircles > li");
      const s1Height = homeSection[0].offsetHeight; //adding nav
      const s2Height = s1Height + homeSection[1].offsetHeight;
      const s3Height = s2Height + homeSection[2].offsetHeight;
      const s4Height = s3Height + homeSection[3].offsetHeight;
      const s5Height = s4Height + homeSection[4].offsetHeight;
      const s6Height = s5Height + homeSection[5].offsetHeight;

      if (window.scrollY > 0) {
        var scrollLine = window.scrollY + window.innerHeight * 0.1;
        var botScrollLine = window.scrollY + window.innerHeight * 0.75;
        // console.log("introContainer");
        // console.log(s1Height);

        // console.log("window.innerHeight");
        // console.log(window.innerHeight);
        // console.log("window.scrollY");
        // console.log(window.scrollY);

        // console.log("botScrollLine");
        // console.log(botScrollLine);
        // console.log("scrollLine");
        // console.log(scrollLine);
        trans.forEach(e => {
          /*, indx*/
          // setTimeout(function(){
          if (e.offsetTop < botScrollLine) {
            e.classList.add("ericFadeInTrans");
          }
          // },50*indx);
        });
        if (scrollLine > 0 && scrollLine < s1Height) {
          scrollCircles.forEach(e => {
            e.classList.remove("active");
          });
          scrollCircles[0].classList.add("active");
        } else if (scrollLine > s1Height && scrollLine < s2Height) {
          scrollCircles.forEach(e => {
            e.classList.remove("active");
          });
          scrollCircles[1].classList.add("active");
        } else if (scrollLine > s2Height && scrollLine < s3Height) {
          scrollCircles.forEach(e => {
            e.classList.remove("active");
          });
          scrollCircles[2].classList.add("active");
        } else if (scrollLine > s3Height && scrollLine < s4Height) {
          scrollCircles.forEach(e => {
            e.classList.remove("active");
          });
          scrollCircles[3].classList.add("active");
        } else if (scrollLine > s4Height && scrollLine < s5Height) {
          scrollCircles.forEach(e => {
            e.classList.remove("active");
          });
          scrollCircles[4].classList.add("active");
        } else if (scrollLine > s5Height && scrollLine < s6Height) {
          scrollCircles.forEach(e => {
            e.classList.remove("active");
          });
          scrollCircles[5].classList.add("active");
        }
      }
    }
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  }
};
</script>

<style lang="scss">
$white: #fff;
$pink: #f14189;
$blue: #1b98e0;
$lightBlue: #54b7f0;
$darkBlue: #1e3446;
$lightGray: #ced1e4;
$darkGray: #444;
$black: #000;

@import url("https://fonts.googleapis.com/css?family=Libre+Baskerville:400,400i,700");
@import url("https://fonts.google.com/specimen/Gothic+A1?selection.family=Gothic+A1:200,400,700,800");
@import url("https://fonts.googleapis.com/css?family=Montserrat:200,400,700,800");

// @font-face {
//   font-family: "Montserrat";
//   font-weight: 400;
//   src: url("") format("truetype");
// }

* {
  margin: 0;
  padding: 0;
}

body,
html {
  scroll-behavior: smooth;
  overflow-x: hidden;
}

.ericTransEffect {
  opacity: 0;
  transition: 0.5s;
  transform: matrix(0.9, 0, 0, 0.9, 0, 0);
}

.ericFadeInTrans {
  opacity: 1 !important;
  transform: matrix(1, 0, 0, 1, 0, 0) !important;
}

.scrollCircles {
  list-style: none;
  position: fixed;
  z-index: 9;
  right: 0;
  top: 50%;
  -webkit-transform: translateY(-50%);
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
  margin: 0;
  margin-top: -40px;
  & > li {
    cursor: pointer;
    height: 15px;
    width: 15px;
    background: none;
    border: 1px solid $blue;
    background: $lightBlue;
    margin-bottom: 10px;
    margin-right: 10px;
    border-radius: 25px;
    opacity: 0.5;
    &.active {
      opacity: 1;
      background: $blue;
    }
  }
}

.horizLine {
  margin: 0 auto;
  display: block;
  height: 1px;
  width: 50px;
  background: $blue;
}
.line {
  margin: 0 auto;
  display: block;
  width: 1px;
  height: 20px;
  background: $blue;
}

.dottedLine {
  margin: 0 auto;
  display: block;
  width: 1px;
  height: 20px;
  border: 1px dotted $blue;
}

.dashedLine {
  margin: 0 auto;
  display: block;
  width: 0;
  height: 20px;
  border: 1px dashed $blue;
  &.normal {
    height: 200px;
  }
  &.extended {
    height: 200px;
  }
}

.u-space-top {
  margin-top: 20px;
  &--small {
    margin-top: 10px;
  }
  &--large {
    margin-top: 40px;
  }
  &--xlarge {
    margin-top: 80px;
  }
  &--xxlarge {
    margin-top: 160px;
  }
}
.u-space-bottom {
  margin-bottom: 20px;
  &--small {
    margin-bottom: 10px;
  }
  &--large {
    margin-top: 40px;
  }
  &--xlarge {
    margin-top: 80px;
  }
  &--xxlarge {
    margin-top: 160px;
  }
}

.introContainer {
  position: relative;
  background: url("../assets/developer-background.jpg") no-repeat center top;
  width: 100%;
  height: 500px;
  text-align: center;
  background-size: cover;
  color: #fff;
  .introContent {
    position: absolute;
    width: 500px;
    top: 100px;
    left: 50%;
    margin-left: -250px;
    a {
      font-size: 1.8rem;
      line-height: 2rem;
      margin: 1rem 0 0 0;
      display: block;
      color: $white;
      text-decoration: none;
      font-style: italic;
      font-family: "Libre Baskerville", Serif;
      &:hover {
        text-decoration: underline;
      }
    }
    .reList {
      padding: 0px 0px 0px 0px;
      list-style: none;
      li {
        display: inline-block;
        border-radius: 25px;
        vertical-align: middle;
        line-height: 1rem;
        font-size: 1rem;
        height: 40px;
        width: 40px;
        position: relative;
        & img {
          position: absolute;
          top: 8px;
          left: 8px;
          width: 25px;
        }
        &:hover {
          background-color: rgba(255, 255, 255, 0.3);
        }
      }
    }
  }
}
h1 {
  margin: 10px 0 10px 17px;
  font-family: Arial;
  font-size: 2rem;
  color: $blue;
}
h2 {
  font-size: 3.3rem;
  line-height: 7rem;
  letter-spacing: 0.12em;
  font-family: "Open Sans", sans-serif;
}
h3 {
  font-size: 1.4rem;
  line-height: 1.4rem;
  letter-spacing: 0.08em;
  font-weight: 200;
  font-family: "Open Sans", sans-serif;
  &.large {
    font-size: 2rem;
    line-height: 2.4rem;
    letter-spacing: 0em;
    font-weight: 400;
    text-transform: uppercase;
    font-family: "Montserrat";
    span {
      color: $blue;
      font-weight: 700;
    }
  }
  &.montserratBold {
    font-family: Montserrat, sans-serif;
    font-weight: 600;
    font-size: 1.1rem;
    text-transform: uppercase;
    color: $blue;
  }
}
h4 {
  &.nextTitle {
    font-size: 0.8rem;
    text-transform: uppercase;
    letter-spacing: 0.1rem;
    font-family: Arial, "Open Sans", sans-serif;
    font-weight: 800;
    color: $blue;
  }
}
p {
  font-family: "Libre Baskerville";
  font-style: italic;
  font-size: 0.9rem;
  line-height: 1.3rem;
  margin: 20px auto 0 auto;
  text-align: center;
  letter-spacing: 1px;
  span {
    text-transform: uppercase;
    font-family: Arial, "Open Sans", sans-serif;
    font-weight: 800;
    color: $blue;
    font-style: normal;
  }
}

@media only screen and (min-width: 48em) {
  h1 {
    font-size: 3rem;
  }
  h2 {
    font-size: 3rem;
    line-height: 5rem;
  }
  h3 {
    font-size: 1.8rem;
    line-height: 1.8rem;
    letter-spacing: 0.08em;
    &.large {
      font-size: 3.4rem;
      line-height: 3.8rem;
      letter-spacing: 0em;
    }
    &.montserratBold {
      font-size: 1.1rem;
    }
  }
  h4 {
    &.nextTitle {
      font-size: 0.8rem;
      letter-spacing: 0.1rem;
    }
  }
  p {
    margin: 0;
    font-size: 0.9rem;
    line-height: 1.3rem;
  }
}
@media only screen and (min-width: 64em) {
}
@media only screen and (min-width: 75em) {
}
</style>
