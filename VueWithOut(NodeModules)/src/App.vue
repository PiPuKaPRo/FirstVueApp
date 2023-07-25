<template>
  <div class="app">
    <h1>Calc</h1>
    <CalculatorA />
  </div>
</template>
  
<script>
import CalculatorA from './components/CalculatorA.vue';

export default {
  components: {
    CalculatorA,
  },
};
</script>
  
<style>
.app {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  font-family: Arial, sans-serif;
}

h1 {
  margin-bottom: 30px;
}
</style>
