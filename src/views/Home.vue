<template>
  <div class="home">
    <div class="dashedLine"></div>
    <h1>Eric Lima</h1>
    <div class="dashedLine"></div>
    <div class="introContainer">
      <div class="introContent">
        <h2>Developer</h2>
        <h3>Helping clients with their needs</h3>
        <a href="#">Click here to view my resume</a>
        <ul class="reList ul-nostyle clearfix">
          <li class="floatL"><a href="https://www.github.com/ericx2x" target="_blank"><img src="../assets/github.png" alt="Git"></a></li>
          <li class="floatL"><a href="https://twitter.com/satoshilovesbsv" target="_blank"><img src="../assets/twitter.png" alt="twitter"></a></li>
          <li class="floatL"><a href="https://www.linkedin.com/in/eric-lima-210b8812" target="_blank"><img src="../assets/linkedin.png" alt="linkdin"></a></li>
        </ul>
        <Robot />
      </div>
    </div>
    <WhoAmI />
    <Portfolio />
    <Languages />
    <Experiences />
    <Ambitions />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Robot from "@/components/Robot.vue";
import WhoAmI from "@/components/WhoAmI.vue";
import Languages from "@/components/Languages.vue";
import Experiences from "@/components/Experiences.vue";
import Ambitions from "@/components/Ambitions.vue";
import Portfolio from "@/views/Portfolio.vue";

export default {
  name: "home",
  components: {
    HelloWorld,
    Robot,
    WhoAmI,
    Portfolio,
    Experiences,
    Ambitions,
    Languages,
  }
};
</script>

<style lang="scss">
$white: #fff;
$pink: #F14189;
$blue: #1B98E0;
$darkBlue: #1e3446;
$lightGray: #CED1E4;
$darkGray: #444;
$black: #000;

@import url('https://fonts.googleapis.com/css?family=Libre+Baskerville:400,400i,700');
@import url('https://fonts.google.com/specimen/Gothic+A1?selection.family=Gothic+A1:200,400,700,800');
// @import url('https://fonts.google.com/specimen/Montserrat?selection.family=Montserrat:200,400,700,800');
@import url('https://fonts.googleapis.com/css?family=Montserrat:200,400,700,800');

// @font-face {
//   font-family: "Montserrat";
//   font-weight: 400;
//   src: url("") format("truetype");
// }

* {
  margin: 0;
  padding: 0;
}

body, html{
  overflow-x: hidden;
}

.horizLine{
  margin: 0 auto;
  display: block;
  height: 1px;
  width: 50px;
  background: $blue;
}

.line{
  margin: 0 auto;
  display: block;
  width: 1px;
  height: 20px;
  background: $blue;
}

.dottedLine{
  margin: 0 auto;
  display: block;
  width: 1px;
  height: 20px;
  border: 1px dotted $blue;
}

.dashedLine{
  margin: 0 auto;
  display: block;
  width: 0;
  height: 20px;
  border: 1px dashed $blue;
  &.normal{
    height: 200px;
  }
  &.extended{
    height: 200px;
  }
}

.u-space-top{
  margin-top: 20px;
  &--small{
    margin-top: 10px;
  }
  &--large{
    margin-top: 40px;
  }
  &--xlarge{
    margin-top: 80px;
  }
  &--xxlarge{
    margin-top: 160px;
  }
}
.u-space-bottom{
  margin-bottom: 20px;
  &--small{
    margin-bottom: 10px;
  }
  &--large{
    margin-top: 40px;
  }
  &--xlarge{
    margin-top: 80px;
  }
  &--xxlarge{
    margin-top: 160px;
  }
}

  .introContainer{
    position: relative;
    background: url('../assets/developer-background.jpg') no-repeat center top;
    width: 100%;
    height: 500px;
    text-align: center;
    background-size: cover;
    color: #FFF;
    .introContent{
      position: absolute;
      width: 500px;
      top: 100px;
      left: 50%;
      margin-left: -250px;
      a{
        font-size: 1.8rem;
        line-height: 1.8rem;
        margin: 1rem 0 0 0;
        display: block;
        color: $white;
        text-decoration: none;
        font-style: italic;
        font-family: 'LibreBaskervilleItalic', Serif;
        &:hover{
          text-decoration: underline;
        }
      }
      .reList{
          padding: 0px 0px 0px 0px;
          list-style: none;
          li{
            display: inline-block;
            border-radius: 25px;
            vertical-align: middle;
            line-height: 1rem;
            font-size: 1rem;
            height: 40px;
            width: 40px;
            position: relative;
            & img{
              position: absolute;
              top: 8px;
              left: 8px;
              width: 25px;
            }
            &:hover{
              background-color: rgba(255, 255, 255, 0.3);
            }
          }
      }
    }
  }
  h1{
    margin: 10px 0 10px 17px;
    font-family: Arial;
    font-size: 2rem;
    color: $blue;
  }
  h2{
    font-size: 3.3rem;
    line-height: 7rem;
    letter-spacing: 0.12em;
    font-family: Helvetica, sans-serif;
  }
  h3{
    font-size: 1.4rem;
    line-height: 1.4rem;
    letter-spacing: 0.08em;
    font-weight: 200;
    font-family: Helvetica, sans-serif;
    &.large{
      font-size: 2rem;
      line-height: 2.4rem;
      letter-spacing: 0em;
      font-weight: 400;
      text-transform: uppercase;
      font-family: "Montserrat";
      span{
        color: $blue;
        font-weight: 700;
      }
    }
    &.montserratBold{
      font-family: Montserrat, sans-serif;
      font-weight: 600;
      font-size: 1.1rem;
      text-transform: uppercase;
      color: $blue;
    }
  }
  h4{
    &.nextTitle{
      font-size: .8rem;
      text-transform: uppercase;
      letter-spacing: .1rem;
      font-family: Arial, Helvetica, sans-serif;
      font-weight: 800;
      color: $blue;
    }
  }
  p{
        font-family: 'Libre Baskerville';
        font-style: italic;
        font-size: .9rem;
        line-height: 1.3rem;
        margin: 20px auto 0 auto;
        text-align: center;
        letter-spacing: 1px;
        span{
          text-transform: uppercase;
          font-family: Arial, Helvetica, sans-serif;
          font-weight: 800;
          color: $blue;
          font-style: normal;
        }
    }
    
  @media only screen and (min-width: 75em) {
  }
  @media only screen and (min-width: 64em) {
  }
  @media only screen and (min-width: 48em) {
    h1{
      font-size: 3rem;
    }
    h2{
      font-size: 5rem;
      line-height: 7rem;
    }
    h3{
      font-size: 1.8rem;
      line-height: 1.8rem;
      letter-spacing: 0.08em;
      &.large{
        font-size: 3.4rem;
        line-height: 3.8rem;
        letter-spacing: 0em;
      }
      &.montserratBold{
        font-size: 1.1rem;
      }
    }
    h4{
      &.nextTitle{
        font-size: .8rem;
        letter-spacing: .1rem;
      }
    }
    p{
      margin: 0;
      font-size: .9rem;
      line-height: 1.3rem;
    }
  }
</style>