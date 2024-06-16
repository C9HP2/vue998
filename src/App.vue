<template>
  <div id="game-board">
    <Square v-for="(square, index) in 64" :squareData="square.text" :key="square.id"></Square>
  </div>
</template>
<!--  ///////////////////////////////////////////////////// -->
<script>
  import { nanoid } from "nanoid"; 
  import GameBoard from "./components/GameBoard.vue";
  import Square from "./components/Square.vue";

  export default { name: "app", 
    components: { GameBoard, Square }, 
    data () { return {
      squares: [
        { id: "square-" + nanoid(), text: "X", },
        { id: "square-" + nanoid(), text: "X", },
        { id: "square-" + nanoid(), text: "X", },
        { id: "square-" + nanoid(), text: "X", },
        { id: "square-" + nanoid(), text: "X", },
        { id: "square-" + nanoid(), text: "X", },
        { id: "square-" + nanoid(), text: "X", },
        { id: "square-" + nanoid(), text: "X", },
        { id: "square-" + nanoid(), text: "X", },
      ],
      // game_rows: []
    }},
  }
</script>
<!--  ///////////////////////////////////////////////////// -->
<style scoped>
  #game-board { text-align: center; padding-top: 20px;}
</style>