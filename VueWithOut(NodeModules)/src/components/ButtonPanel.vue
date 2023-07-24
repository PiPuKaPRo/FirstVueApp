<template>
  <div class="button-panel">
    <Button v-for="buttonLabel in buttons" :key="buttonLabel" :label="buttonLabel" @click="handleButtonClick"></Button>
  </div>
</template>
  
<script>
import Button from './ButtonA.vue';

export default {
  components: {
    Button,
  },
  data() {
    return {
      buttons: ['7', '8', '9', '/', '4', '5', '6', '*', '1', '2', '3', '-', '0', '.', '=', '+', 'C'],
    };
  },
  methods: {
    handleButtonClick(label) {
      this.$emit('buttonClick', label);
    },
  },
};
</script>
  
<style>
.button-panel {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 10px;
}
</style>