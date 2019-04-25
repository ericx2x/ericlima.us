<template>
  <section>
    <div class="bigCircle">
      <div>
          <a href="http://www.linkedin.com/profile/view?id=44720940&amp;trk=tab_pro">
            <figure class=""></figure>
            <div class=""></div>
          </a>
          <p class="">
              <a href="http://www.linkedin.com/profile/view?id=44720940&amp;trk=tab_pro">Add me  <br class="br1">on <br>Linkedin</a>
          </p>
          <div class="horizontalLine"></div>
          <p class="">Thanks for viewing my website.</p>
          <a class="" target="_blank" href="/resume">Click here to view my resume.</a>
        </div>
    </div>
  </section>
</template>

<script>
    import ScrollDown from "@/components/ScrollDown.vue";
    import NumberContainer from "@/components/NumberContainer.vue";

    export default {
        name: "home",
        components: {
            ScrollDown,
            NumberContainer,
        }
    };
</script>

<style scoped lang="scss">
  .bigCircle {
    max-width: 1000px;
    margin: 0 auto;
    .grid{
        // display: grid;
        // grid-template-columns: 1fr 1fr 1fr;
        margin: 0 20px;
        & .item{
            // margin: 5%;
            & > img{
              width: 100%;
            }
            & > .paragraphContent{
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