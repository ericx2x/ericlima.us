<template>
  <section>
    <div class="portfolio">
      <ScrollDown />
      <div class="dashedLine extended"></div>
      <NumberContainer num="2" />
      <h3 class="large u-space-top--xlarge">
        My <span>Portfolio</span>.<br />
      </h3>
      <div class="grid">
        <div class="row">
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-3 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
          </div>
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-3 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
          </div>
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-3 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
          </div>
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-3 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
          </div>
        </div>
        <div class="row">
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-3 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
          </div>
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-3 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
          </div>
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-3 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
          </div>
          <div class="item col-xs-12 col-xs-offset-0 col-sm-6 col-sm-offset-0 col-md-3 col-md-offset-0 col-lg-3 col-lg-offset-0 u-space-top--large">
            <img src="../assets/133W.png" alt="Lorem ipsum dolor sit amet" />
            <p class="u-space-top">A site created for MRP Realty in Downtown Manhattan.</p>
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
  .portfolio{
    max-width: 1000px;
    margin: 40px auto 0 auto;
    .grid{
      margin: 0 20px;
      & .item {
        & > img{
          width: 100%;
        }
      }
    }
  }
</style>