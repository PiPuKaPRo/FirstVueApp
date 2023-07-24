<template>
  <button class="calculator-button" @click="handleClick">
    {{ label }}
  </button>
</template>
  
<script>
export default {
  props: {
    label: {
      type: String,
      required: true,
    },
  },
  methods: {
    handleClick() {
      this.$emit('click', this.label);
    },
  },
};
</script>
  
<style>
.calculator-button {
  width: 60px;
  height: 60px;
  font-size: 1.2rem;
  background-color: #d8cf7e;
  border: 1px solid #050505;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.calculator-button:hover {
  background-color: #eb4040;
}
</style>