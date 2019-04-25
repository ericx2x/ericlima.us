<template>
    <div class="numPush">
        {{this.num}}
        <div class="numContainer">
        </div>
    </div>
</template>

<script>

    export default {
        
        props: {
            num: String,
        },
    }

</script>


<style lang="scss">
    $white: #fff;
    $pink: #F14189;
    $blue: #1B98E0;
    $lightBlue: #2CA9F1;
    $darkBlue: #1e3446;
    $lightGray: #CED1E4;
    $darkGray: #444;
    $black: #000;
    .numPush{
        color: $blue;
        font-weight: 600;
        font-size: .8rem;;
        position: relative;
        height: 30px;
        line-height: 32px;
        width: 30px;
        margin: 0 auto;
        .numContainer{
            position: absolute;
            top: 0px;
            left: -2px;
            height: 30px;
            line-height: 30px;
            margin: 0 auto;
            width: 30px;
            border: 1px solid $lightBlue;
            border-radius: 25px;
            transform: rotate(45deg);
        }
    }
</style>