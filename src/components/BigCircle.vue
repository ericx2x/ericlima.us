<template>
  <section>
    <div class="bigCircle">
      <div>
        <div class="contrast">
          <a
            href="http://www.linkedin.com/profile/view?id=44720940&amp;trk=tab_pro"
          >
            <img src="../assets/linkedin-large.png" />
          </a>
        </div>
        <a
          class="linkedinLink"
          href="http://www.linkedin.com/profile/view?id=44720940&amp;trk=tab_pro"
          >Add me on Linkedin</a
        >
        <div class="horizLine"></div>
        <p class="">Thanks for viewing my website.</p>
        <a class="" target="_blank" :href="this.resume"
          >Click here to view my resume.</a
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "home",
  props: {
    resume: String
  },
  components: {}
};
</script>

<style scoped lang="scss">
$white: #fff;
$pink: #f14189;
$blue: #1b98e0;
$lightBlue: rgb(84, 183, 240);
$darkBlue: #1e3446;
$lightGray: #ced1e4;
$darkGray: #444;
$black: #000;

section {
  max-width: 1000px;
  margin: 0 auto;
}
.horizLine {
  background: white;
  width: 200px;
  margin: 30px auto 30px auto;
}
.bigCircle {
  background: $blue;
  border-radius: 50%;
  width: 450px;
  height: 450px;
  margin: 0 auto;
  margin-top: 40px;
  // left: 0;
  & > div {
    margin-top: 80px;
    display: inline-block;
    width: 100%;
    font-size: 1.5rem;
    .contrast {
      width: 70px;
      height: 70px;
      border-radius: 20px;
      margin: 0 auto;
      // height: 50px;
      display: block;
      background: $lightBlue;
    }
    a {
      width: 100%;
      color: white;
      font-family: "Libre Baskerville", sans;
      text-decoration: none;
      font-style: italic;
      font-size: 1.3rem;
      img {
        margin-top: 10px;
        width: 100%;
      }
      &.linkedinLink {
        font-family: "Gothic A1", sans-serif;
        font-style: inherit;
        font-size: 2rem;
        margin-top: 20px;
        // display: inline-block;
      }
    }
    p {
      font-family: "Open sans", sans-serif;
      font-style: initial;
      font-size: 1.4rem;
      line-height: 1.4rem;
      margin-bottom: 20px;
    }
    color: white;
  }
}

@media only screen and (min-width: 75em) {
}
@media only screen and (min-width: 64em) {
  .bigCircle {
    // position: absolute;
    // right: 0;
    margin-right: 0px;
    margin-top: -320px;
    & > div {
      a {
      }
    }
  }
}
@media only screen and (min-width: 48em) {
}
</style>
