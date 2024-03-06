<template>
  <div class="container">
    <div class="block"></div>
    <button>Animate</button>
  </div>
  <base-modal @close="hideDialog" v-if="dialogIsVisible">
    <p>This is a test dialog!</p>
    <button @click="hideDialog">Close it!</button>
  </base-modal>
  <div class="container">
    <button @click="showDialog">Show Dialog</button>
  </div>
</template>

<script>
export default {
  data() {
    return { dialogIsVisible: false };
  },
  methods: {
    showDialog() {
      this.dialogIsVisible = true;
    },
    hideDialog() {
      this.dialogIsVisible = false;
    },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
html {
  font-family: sans-serif;
}
body {
  margin: 0;
}
button {
  padding: 0.5rem 2rem;
  border: 1px solid #810032;
  border-radius: 30px;
  color: white;
  font: inherit;
  cursor: pointer;
  background-color: #810032;
}
button:hover,
button:active {
  border-color: #a80b48;
  background-color: #a80b48;
}
.block {
  width: 8rem;
  height: 8rem;
  margin-bottom: 2rem;
  background-color: #290033;
}
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  max-width: 40rem;
  margin: 2rem auto;
  padding: 2rem;
  border: 2px solid #ccc;
  border-radius: 12px;
}
</style>
