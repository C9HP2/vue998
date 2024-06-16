<template>
  <button> {{ squareData }} </button> 
</template>
<script>
  export default {
    props: {
      squareData: { type: String, default: null},
    },
  };
</script>
<style scopped>
  button { width: 60px; height: 60px; border: 1px solid #d5d4d4 ; }
</style>
