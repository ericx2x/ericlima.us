<template>
  <div class="scrollDownAnimation" id="scrollAnimation01">
    <div class="push"></div>
    <a href="#scrollAnimation02"><span></span></a>
  </div>
</template>

<script>
const aTags = document.querySelectorAll("a"); //a[href*=#]

aTags.forEach(element => {
  element.click;
});
export default {
  data() {
    return {};
  },
  methods: {
    tagClick() {
      alert();
    }
  }
};
</script>

<style scope lang="scss">
$white: #fff;
$pink: #f14189;
$blue: #1b98e0;
$darkBlue: #1e3446;
$lightGray: #ced1e4;
$darkGray: #444;
$black: #000;

.scrollDownAnimation {
  position: relative;
  width: 100px;
  height: 100px;
  margin: 0 auto;
  .push {
    height: 80px;
  }
}
#scrollAnimation01 a span {
  position: absolute;
  top: 0;
  left: 50%;
  width: 24px;
  height: 24px;
  margin-left: -12px;
  border-left: 1px solid $blue;
  border-bottom: 1px solid $blue;
  -webkit-transform: rotateZ(-45deg);
  transform: rotateZ(-45deg);
  -webkit-animation: sdb01 1.5s infinite;
  animation: sdb01 1.5s infinite;
  box-sizing: border-box;
}
@-webkit-keyframes sdb01 {
  0% {
    -webkit-transform: rotateY(0) rotateZ(-45deg) translate(0, 0);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    -webkit-transform: rotateY(720deg) rotateZ(-45deg) translate(-20px, 20px);
    opacity: 0;
  }
}
@keyframes sdb01 {
  0% {
    transform: rotateY(0) rotateZ(-45deg) translate(0, 0);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    transform: rotateY(720deg) rotateZ(-45deg) translate(-20px, 20px);
    opacity: 0;
  }
}
</style>
