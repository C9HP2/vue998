<template>
  <div id="game-board">
    <Square v-for="(square, squareIndex) in squares" :squareData="square.text"
      :key="square.id" :squareIndex="squareIndex+1" :id=square.id :squareId=square.id>
    </Square>
  </div>
</template>
<!--  ///////////////////////////////////////////////////// -->
<script>
  import { nanoid } from "nanoid"; 
  import Square from "./components/Square.vue";

  export default { name: "app", 
    components: { Square }, 
    data () { return {
      squares: Array.from({length: 64}, () => ({
        id: "square-" + nanoid(), text: "X", 
      })),
    }},
  }
</script>
<!--  ///////////////////////////////////////////////////// -->
<style scoped>
  #game-board { text-align: center; padding-top: 20px;}
</style>