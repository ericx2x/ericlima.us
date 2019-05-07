<template>
  <div>
    <div>(Controls - rotate: u,i,&nbsp; move: j,k,l)</div>
    <canvas id="tetris" height="240" width="400"></canvas>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    tagClick() {}
  },
  mounted() {
    const canvas = document.getElementById("tetris");
    const context = canvas.getContext("2d");
    context.scale(20, 20);

    function arenaSweep() {
      outer: for (let y = arena.length - 1; y >= 0; y--) {
        for (let x = 0; x < arena[y].length; x++) {
          if (arena[y][x] === 0) {
            continue outer;
          }
        }
        const row = arena.splice(y, 1)[0].fill(0);
        arena.unshift(row);
        y++;
      }
    }

    function collide(arena, player2) {
      const [m, o] = [player2.matrix, player2.pos];
      for (let y = 0; y < m.length; y++) {
        for (let x = 0; x < m[y].length; x++) {
          if (
            m[y][x] !== 0 &&
            (arena[y + o.y] && arena[y + o.y][x + o.x]) !== 0
          ) {
            return true;
          }
        }
      }
      return false;
    }

    function createMatrix(w, h) {
      const matrix = [];
      while (w--) {
        matrix.push(new Array(h).fill(0));
      }
      return matrix;
    }

    function createPiece(type) {
      if (type === "T") {
        return [[0, 0, 0], [1, 1, 1], [0, 1, 0]];
      } else if (type === "O") {
        return [[2, 2], [2, 2]];
      } else if (type === "L") {
        return [[0, 3, 0], [0, 3, 0], [0, 3, 3]];
      } else if (type === "J") {
        return [[0, 4, 0], [0, 4, 0], [4, 4, 0]];
      } else if (type === "I") {
        return [[0, 5, 0, 0], [0, 5, 0, 0], [0, 5, 0, 0], [0, 5, 0, 0]];
      } else if (type === "S") {
        return [[0, 6, 6], [6, 6, 0], [0, 0, 0]];
      } else if (type === "Z") {
        return [[7, 7, 0], [0, 7, 7], [0, 0, 0]];
      }
    }

    function draw() {
      // var img = document.getElementById("dot");
      // var dot = context.createPattern(img, "repeat");
      // context.rect(0, 0, 150, 100);
      // context.fillStyle = dot;
      // context.fill();
      context.fillStyle = "rgba(27, 152, 224, .05)"; // set color
      context.fillRect(0, 0, canvas.width, canvas.height); // draw rectangle

      drawMatrix(arena, { x: 0, y: 0 });
      drawMatrix(player2.matrix, player2.pos);
    }

    function drawMatrix(matrix, offset) {
      matrix.forEach((row, y) => {
        row.forEach((value, x) => {
          if (value != 0) {
            //   context.shadowBlur = 10;
            //   context.shadowOffsetX = 20; //X
            //   context.shadowColor = "gray";
            // context.shadowBlur = 20;
            // context.shadowColor = "white";
            context.fillStyle = colors[value];
            context.fillRect(x + offset.x, y + offset.y, 1, 1);
            context.strokeStyle = "#FF0000";
            context.strokeRect(20, 20, 150, 100);
          }
        });
      });
    }

    function playerDrop() {
      player2.pos.y++;
      if (collide(arena, player2)) {
        player2.pos.y--;
        merge(arena, player2);
        playerReset();
        arenaSweep();
      }
      dropCounter = 0;
    }

    function playerMove(dir) {
      player2.pos.x += dir;
      if (collide(arena, player2)) {
        player2.pos.x -= dir;
      }
    }

    function playerReset() {
      const pieces = "ILJOTSZ";
      player2.matrix = createPiece(pieces[(pieces.length * Math.random()) | 0]);
      player2.pos.y = 0;
      player2.pos.x =
        ((arena[0].length / 2) | 0) - ((player2.matrix[0].length / 2) | 0);
      if (collide(arena, player2)) {
        arena.forEach(row => row.fill(0));
      }
    }

    function playerRotate(dir) {
      rotate(player2.matrix, dir);
      if (collide(arena, player2)) {
        rotate(player2.matrix, -dir);
      }
    }

    function rotate(matrix, dir) {
      for (let y = 0; y < matrix.length; y++) {
        for (let x = y + 1; x < matrix.length; x++) {
          [matrix[x][y], matrix[y][x]] = [matrix[y][x], matrix[x][y]];
        }
      }

      if (dir > 0) {
        matrix.forEach(row => row.reverse());
      } else {
        matrix.reverse();
      }
    }

    let dropCounter = 0;
    let dropInterval = 1000;

    let lastTime = 0;

    function update(time = 0) {
      const deltaTime = time - lastTime; // millisecond
      lastTime = time;
      dropCounter += deltaTime;
      if (dropCounter > dropInterval) {
        playerDrop();
      }
      draw();
      requestAnimationFrame(update);
    }

    const colors = [
      null,
      "red",
      "blue",
      "violet",
      "green",
      "purple",
      "orange",
      "pink"
    ];

    const arena = createMatrix(12, 20);

    function merge(arena, player2) {
      player2.matrix.forEach((row, y) => {
        row.forEach((value, x) => {
          if (value !== 0) {
            arena[y + player2.pos.y][x + player2.pos.x] = value;
          }
        });
      });
    }
    const player2 = {
      pos: { x: 5, y: 5 },
      matrix: null
    };

    document.addEventListener("keydown", event => {
      //console.log(event);
      if (event.keyCode === 74) {
        // keycode lookup: http://pomle.github.io/keycode/
        playerMove(-1);
      } else if (event.keyCode === 76) {
        playerMove(1);
      } else if (event.keyCode === 75) {
        playerDrop();
      } else if (event.keyCode === 85) {
        playerRotate(-1);
      } else if (event.keyCode === 73) {
        playerRotate(1);
      }
    });

    playerReset();
    update();
  }
};
</script>

<style scope lang="scss">
canvas {
  border: solid 0.2em #fff;
  height: 35vh;
  max-width: 100%;
}
</style>
