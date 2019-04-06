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
        <div class="leftarm">
            <div class="finger"></div>
            <div class="finger"></div>
        </div>
        <div class="rightarm">
            <div class="finger"></div>
            <div class="finger"></div>
        </div>
        <div class="neck"></div>
        <div class="body"></div>
        <div class="legs">
            <div class="left">
                <div class="foot"></div>
            </div>
            <div class="right">
                <div class="foot"></div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
$white: #fff;
$pink: #F14189;
$blue: #1B98E0;
$lightGray: #bdc3c7;
$darkGray: #444;
$black: #000;

body{
  background-color: $white;
  color: $darkGray;
  .bot{
    position: relative;
    height: 30px;
    width: 50px;
    border-radius: 25px;
    background-color: $lightGray;
    animation: 5s botMotion linear forwards;
    margin-bottom: 50px;
    .eyes{
      position: absolute;
      width: 40px;
      height: 20px;
      top: 5px;
      left: 5px;
      border-radius: 25px;
      background-color: $darkGray;
      .eye{
        height: 10px;
        width: 5px;
        background-color: $blue;
        animation: 5.6s eyeBlink .35s linear infinite;
        border-radius:  40%;
      }
      .left{
        position: absolute;
        top: 50%;
        left: 25%;
        margin-top: -5px;
      }
      .right{
        position: absolute;
        top: 50%;
        right: 25%;
        margin-top: -5px;
      }
    }
    .finger{
      position: absolute;
      height: 10px;
      width: 5px;
      top: 40px;
      background-color: $lightGray;
    }
    .leftarm{
      position: absolute;
      top: 0;
      left: 0;
      height: 30px;
      width: 25px;
      .finger:nth-of-type(1){
        animation: 5s lefttopfinger linear forwards;
      }
      .finger:nth-of-type(2){
        animation: 5s leftbotfinger linear forwards;
      }
    }
    .rightarm{
      position: absolute;
      top: 0;
      right: 0;
      height: 30px;
      width: 25px;
      .finger:nth-of-type(1){
        animation: 5s righttopfinger linear forwards;
      }
      .finger:nth-of-type(2){
        animation: 5s rightbotfinger linear forwards;
      }
    }
  .neck{
    position: absolute;
    top: 30px;
    left: 10px;
    width: 20px;
    height: 10px;
    background-color: $lightGray;
    margin-left: 5px;
    animation: 5s neckMotion linear forwards;
  }
//   #body{
//     position: absolute;
//     top: 33px;
//     width: 50px;
//     height: 10px;
//     background-color: $lightGray;
//     animation: 5s bodyMotion linear forwards;
//   }
  .legs{
    position: absolute;
    top: 63px;
    left: 25px;
    .foot{
      width: 25px;
      height: 10px;
      background-color: $lightGray;
    }
    .left{
      position: absolute;
      top: -10px;
      left: 0;
      animation: 5s leftfoot linear forwards;
    }
    .right{
      position: absolute;
      top: -10px;
      right: 0;
      animation: 5s rightfoot linear forwards;
    }
  }
}
  
// @keyframes lefttopfinger{
//   0%
//     left 0
//     top 5px
//   10%, 20%
//     left -10px
//     top 5px
//   30%
//     left -10px
//     top 2px
//   40%
//     left -10px
//     top 5px
//   50%
//     left -10px
//     top 2px
//   60%
//     left -10px
//     top 5px
//   70%
//     left -10px
//     top 2px
//   80%, 90%
//     left -10px
//     top 5px
//   100%
//     left 0
//     top 5px
// }

// @keyframes leftbotfinger{
//   0%
//     left 0
//     bottom 5px
//   10%, 20%
//     left -10px
//     bottom 5px
//   30%
//     left -10px
//     bottom 2px
//   40%
//     left -10px
//     bottom 5px
//   50%
//     left -10px
//     bottom 2px
//   60%
//     left -10px
//     bottom 5px
//   70%
//     left -10px
//     bottom 2px
//   80%, 90%
//     left -10px
//     bottom 5px
//   100%
//     left 0
//     bottom 5px
// }

// @keyframes righttopfinger{
//   0%
//     right 0
//     top 5px
//   10%, 20%
//     right -10px
//     top 5px
//   30%
//     right -10px
//     top 2px
//   40%
//     right -10px
//     top 5px
//   50%
//     right -10px
//     top 2px
//   60%
//     right -10px
//     top 5px
//   70%
//     right -10px
//     top 2px
//   80%, 90%
//     right -10px
//     top 5px
//   100%
//     right 0
//     top 5px
// }

// @keyframes rightbotfinger{
//   0%
//     right 0
//     bottom 5px
//   10%, 20%
//     right -10px
//     bottom 5px
//   30%
//     right -10px
//     bottom 2px
//   40%
//     right -10px
//     bottom 5px
//   50%
//     right -10px
//     bottom 2px
//   60%
//     right -10px
//     bottom 5px
//   70%
//     right -10px
//     bottom 2px
//   80%, 90%
//     right -10px
//     bottom 5px
//   100%
//     right 0
//     bottom 5px
// }
  
// @keyframes leftfoot{
//   0%
//     top 0
//   10%, 20%
//     top 0
//   30%
//     top 12px
//   40%
//     top 0
//   50%
//     top 12px
//   60%
//     top 0
//   70%
//     top 12px
//   80%, 90%, 100%
//     top 0
// }

// @keyframes rightfoot{
//   0%
//     top 0
//   10%, 20%, 30%
//     top 0
//   40%
//     top 12px
//   50%
//     top 0
//   60%
//     top 12px
//   70%, 80%, 90%, 100%
//     top 0
// }

// @keyframes botMotion{
//   0%,10%
//     top 0
//   20%, 80%
//     top -13px
//   90%, 100%
//     top 0
// }

// @keyframes neckMotion{
//   0%,10%{
//     top: 30px;
//   }
//   20%, 80%{
//     top: 17px;
//   }
//   90%, 100%{
//     top: 30px;
//   }
// }

// @keyframes bodyMotion{
//   0%,10%{
//     top: 33px;
//   }
//   20%, 80%{
//     top: 20px;
//   }
//   90%, 100%{
//     top: 33px;
//   }
// }

@keyframes eyeBlink{
  0%, 10%{
    background-color: $blue;
  }
  15%{
    background-color: $darkGray;
  }
  20%, 50%, 80%{
    background-color: $blue;
  }
  85%{
    background-color: $darkGray;
  }
  90%, 100%{
    background-color: $blue;
  }
}
}
</style>