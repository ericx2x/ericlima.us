<template>
    <section>
        <div class="dashedLine"></div>
        <h4 class="nextTitle u-space-top--small">Who Am I?</h4>
        <ScrollDown />
        <div class="dashedLine extended"></div>
        <NumberContainer num="1" />
        <h3 class="large u-space-top--xlarge">
            I'm <span>Eric Lima</span>.<br />
            A web developer.
        </h3>
        <Tetris />
        <p class="u-space-top--large">I'm a passionate and dedicated web developer who has developed hundreds of different websites that have a combined total of over a million page views. My love for programming lead me to pursue a <span>Bachelors of Science degree in Computer Science</span> at the University of Massachusetts Lowell. This website showcases some of my best work. Throughout my years, I've developed things in C, C++, C#, Java, JS,Ruby, Python and more. I'm more focused with JS and web development at the moment though.</p>
        <p class="u-space-top--large">Currently, I am working fulltime to build client websites. While I have completed over hundreds projects, I have highlighted only some of my best work below.</p>
    </section>
</template>

<script>
    import ScrollDown from "@/components/ScrollDown.vue";
    import Tetris from "@/components/Tetris.vue";
    import NumberContainer from "@/components/NumberContainer.vue";

    export default {
        name: "home",
        components: {
            ScrollDown,
            Tetris,
            NumberContainer,
        }
    };
</script>


<style scoped lang="scss">
    $white: #fff;
    $pink: #F14189;
    $blue: #1B98E0;
    $darkBlue: #1e3446;
    $lightGray: #CED1E4;
    $darkGray: #444;
    $black: #000;

    section{
        max-width: 1005px;
        margin: 0 auto;
    }

    p{
        font-size: 1.2rem;
        line-height: 1.6rem;
        margin: 20px 20px 0 20px;
    }

    .scrollDownAnimation {
        position: relative;
        width: 100%;
        height: 100%;
    }


    @media only screen and (min-width: 75em) {
    }
    @media only screen and (min-width: 64em) {
    }
    @media only screen and (min-width: 48em) {
        p{
            font-size: 1.5rem;
            line-height: 1.9rem;
        }
    }
</style>