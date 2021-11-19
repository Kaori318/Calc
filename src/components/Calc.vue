<template>
  <div>
    <div class="display">
      <input type="number" v-model.number="op1">
      <input type="number" v-model.number="op2">
      = {{ result }}
    </div>
    <div class="keyboard">
      <button @click="add">+</button>
      <button @click="sub">-</button>
      <button @click="multiplication">*</button>
      <button @click="division">/</button>
      <button @click="exponentiation">**</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Calc',
  data: () => ({
    op1: 0,
    op2: 0,
    result: 0,
  }),
  methods: {
    add() {
      this.result = this.op1 + this.op2;
    },
    sub() {
      this.result = this.op1 - this.op2;
    },
    division() {
      this.result = Math.round(this.op1 / this.op2);
    },
    multiplication() {
      this.result = this.op1 * this.op2;
    },
    exponentiation() {
      this.result = this.op1 ** this.op2;
    },
  },
};
</script>

<style scoped lang="scss">
</style>
