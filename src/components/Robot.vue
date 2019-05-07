<template>
  <div class="bot">
    <div class="eyes">
      <div class="left">
        <div class="eye"></div>
      </div>
      <div class="right">
        <div class="eye"></div>
      </div>
    </div>
    <!-- <div class="forearm">
            <div class="fist"></div>
        </div>
        <div class="rightarm">
            <div class="finger"></div>
            <div class="finger"></div>
        </div> -->
    <div class="neck"></div>
    <div class="body"></div>
    <div class="ear">
      <div class="left"></div>
      <div class="right"></div>
    </div>
    <div class="tail">
      <div class="heart"></div>
    </div>
  </div>
</template>

<style scoped lang="scss">
$white: #fff;
$pink: #f14189;
$blue: #1b98e0;
$darkBlue: #1e3446;
$lightGray: #ced1e4;
$darkGray: #444;
$black: #000;
.bot {
  position: relative;
  margin: 0 auto;
  height: 30px;
  top: 20px;
  text-align: center;
  width: 50px;
  border-radius: 25px;
  background-color: $lightGray;
  animation: 4s Dance linear infinite;
  margin-bottom: 50px;
  .tail {
    position: relative;
    width: 212px;
    height: 100px;
    box-sizing: content-box;
  }
  .tail:before,
  .tail:after {
    //   content: "";
    //   box-sizing: content-box;
    //   position: absolute;
    //   top: 0;

    //   width: 60px;
    //   height: 60px;
    //   border: 20px solid red;
    //   border-radius: 50px 50px 0 50px;
    //   transform: rotate(-45deg);
    content: "";
    position: absolute;
    top: 30px;
    left: 34px;
    height: 25px;
    width: 25px;
    border: 4px solid $lightGray;
    border-top: 0px;
    border-radius: 0px 0px 85px 85px;
    transform: rotate(-23deg);
  }
  .tail:after {
    height: 15px;
    width: 15px;
    margin-top: -22px;
    margin-left: 18.5px;
    transform: rotate(154deg);
  }

  .heart {
    position: relative;
    width: 10px;
    height: 9px;
    left: 72px;
    top: 20px;
  }
  .heart:before,
  .heart:after {
    position: absolute;
    content: "";
    left: 5px;
    top: 0;
    width: 5px;
    height: 8px;
    background: $blue;
    border-radius: 5px 5px 0 0;
    transform: rotate(-45deg);
    transform-origin: 0 100%;
    z-index: 1;
  }
  .heart:after {
    left: 0;
    transform: rotate(45deg);
    transform-origin: 100% 100%;
  }

  .eyes {
    position: absolute;
    width: 40px;
    height: 20px;
    top: 5px;
    left: 5px;
    border-radius: 25px;
    background-color: $darkGray;
    .eye {
      height: 10px;
      width: 5px;
      background-color: $blue;
      animation: 5.6s eyeBlink 0.35s linear infinite;
      border-radius: 40%;
    }
    .left {
      position: absolute;
      top: 50%;
      left: 25%;
      margin-top: -5px;
    }
    .right {
      position: absolute;
      top: 50%;
      right: 25%;
      margin-top: -5px;
    }
  }
  .rightarm {
    position: absolute;
    top: 46px;
    left: 45px;
    background: lightGray;
    height: 9px;
    width: 24px;
    border-radius: 1px;
  }
  .neck {
    position: absolute;
    top: 30px;
    left: 10px;
    width: 20px;
    height: 10px;
    z-index: 1;
    background-color: $blue;
    margin-left: 5px;
    animation: 5s neckMotion linear forwards;
  }
  .body {
    position: absolute;
    border-radius: 25px;
    top: 40px;
    width: 50px;
    height: 25px;
    background-color: $lightGray;
    animation: 5s bodyMotion linear forwards;
  }
  .ear {
    .left {
      position: absolute;
      top: -13px;
      // background: $lightGray;
      left: 32px;
      height: 15px;
      width: 15px;
      // border-radius: 25px;
      transform: rotate(15deg);
      width: 0;
      height: 0;
      border-left: 8px solid transparent;
      border-right: 8px solid transparent;
      border-bottom: 16px solid $lightGray;
    }
    .right {
      position: absolute;
      top: -13px;
      // background: $lightGray;
      left: 2px;
      height: 15px;
      width: 15px;
      transform: rotate(-15deg);
      // border-radius: 25px;
      width: 0;
      height: 0;
      border-left: 8px solid transparent;
      border-right: 8px solid transparent;
      border-bottom: 16px solid $lightGray;
    }
  }
  .forearm {
    position: absolute;
    top: 20px;
    left: 65px;
    background: $lightGray;
    height: 35px;
    border-radius: 15px;
    width: 10px;
    animation: 3s foreArm linear infinite;
    .fist {
      width: 20px;
      height: 20px;
      border-radius: 20px;
      background: $lightGray;
      // position: absolute;
      margin-left: -5px;
      margin-top: -10px;
    }
  }
}

@keyframes Dance {
  0% {
    left: 0;
  }
  10% {
    left: 62px;
  }
  20% {
    left: -62px;
  }
  30% {
    left: 62px;
  }
  40% {
    left: 0;
  }
  100% {
    left: 0;
  }
}

@keyframes foreArm {
  0% {
    transform: rotate(10deg);
    left: 65px;
  }
  45% {
    transform: rotate(0deg);
    left: 63px;
  }
  50% {
    transform: rotate(10deg);
    left: 65px;
  }
  55% {
    transform: rotate(0deg);
    left: 63px;
  }
  60% {
    transform: rotate(-10deg);
    left: 60px;
  }
  65% {
    transform: rotate(0deg);
    left: 63px;
  }
  70% {
    transform: rotate(10deg);
    left: 65px;
  }
  75% {
    transform: rotate(0deg);
    left: 63px;
  }
  80% {
    transform: rotate(10deg);
    left: 65px;
  }
  85% {
    transform: rotate(0deg);
    left: 63px;
  }
  90% {
    transform: rotate(-10deg);
    left: 60px;
  }
  95% {
    transform: rotate(0deg);
    left: 63px;
  }
  100% {
    transform: rotate(10deg);
    left: 65px;
  }
}

@keyframes eyeBlink {
  0%,
  10% {
    background-color: $blue;
  }
  15% {
    background-color: $darkGray;
  }
  20%,
  50%,
  80% {
    background-color: $blue;
  }
  85% {
    background-color: $darkGray;
  }
  90%,
  100% {
    background-color: $blue;
  }
}
</style>
