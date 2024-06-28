<template>
  <button @click=(console.log(this.squareIndex))> {{ squareData }} </button> 

</template>
<script>
  export default {
    props: {
      squareData: { type: String, default: null},
      squareIndex: { type: Number, required: true }, 
      squareId: { type: String, required: true, },
    },
    computed: {
      squareStyle() {
        // Calculate row and column based on index
        const row = Math.floor(this.index / 8);
        const col = this.index % 8;
        // Determine if the square should be black or white
        const isBlack = (row % 2 === 0) ? col % 2 === 1 : col % 2 === 0;
        return {
          backgroundColor: isBlack ? 'black' : 'white',
          color: isBlack ? 'white' : 'black', // Text color for better visibility
        };
      },
    },
  };
</script>
<style scopped>
  button { width: 60px; height: 60px; border: 1px solid #d5d4d4; font-size: 20px;}
</style>
