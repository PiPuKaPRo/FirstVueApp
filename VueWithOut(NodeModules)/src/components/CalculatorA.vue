<template>
  <div class="calculator">
    <DisplayA :displayValue="displayValue" />
    <ButtonPanel @buttonClick="handleButtonClick" @panelClick="handlePanelClick" />
  </div>
</template>
  
<script>
import ButtonPanel from './ButtonPanel.vue';
import DisplayA from './DisplayA.vue';

export default {
  components: {
    ButtonPanel,
    DisplayA,
  },
  data() {
    return {
      displayValue: '0',
    };
  },
  methods: {
    handleButtonClick(label) {
      if (label === '=') {
        try {
          this.displayValue = eval(this.displayValue).toString();
        } catch (error) {
          this.displayValue = 'Error';
        }
      } else if (label === 'C') {
        this.displayValue = '0';
      } else if (this.displayValue === '0' || this.displayValue === 'Error') {
        this.displayValue = label;
      } else {
        this.displayValue += label;
      }
    },
    handlePanelClick(event) {
      event.stopPropagation();
    },
  },
};
</script>
  
<style>
.calculator {
  max-width: 300px;
  margin: 0 auto;
  background-color: #ff0000;
  border: 1px solid #3d3939;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 20px;
}
</style>