<template>
  <section>
    <div class="experiences">
      <ScrollDown />
      <div class="dashedLine extended"></div>
      <NumberContainer num="4" />
      <h3 class="large u-space-top--xlarge">
        <span>Unique </span> Experience<br />
      </h3>
      <div class="grid">
        <div class="row">
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-6 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Ruby<br></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
            </div>
          </div>
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-6 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Ruby<br></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
            </div>
          </div>
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-6 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Ruby<br></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
            </div>
          </div>
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-6 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <div class="paragraphContent">
              <h3 class="montserratBold u-space-top">Ruby<br></h3>
              <div class="horizLine"></div>
              <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
            </div>
          </div>
        </div>
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
  .experiences {
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