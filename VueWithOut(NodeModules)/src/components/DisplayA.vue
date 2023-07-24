<template>
  <div class="calculator-display">
    {{ displayValue }}
  </div>
</template>
  
<script>
export default {
  props: {
    displayValue: {
      type: String,
      required: true,
    },
  },
};
</script>
  
<style>
.calculator-display {
  padding: 10px;
  font-size: 1.8rem;
  text-align: right;
  background-color: #dbc6c6;
  border: 1px solid #020202;
  border-radius: 5px;
}
</style>