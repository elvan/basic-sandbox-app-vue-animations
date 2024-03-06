<template>
  <div class="backdrop" @click="$emit('close')"></div>
  <dialog open>
    <slot></slot>
  </dialog>
</template>

<script>
export default {
  emits: ['close'],
};
</script>

<style scoped>
.backdrop {
  z-index: 10;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.75);
}

dialog {
  z-index: 100;
  position: fixed;
  top: 30vh;
  left: calc(50% - 15rem);
  width: 30rem;
  margin: 0;
  padding: 1rem;
  border: none;
  border-radius: 12px;
  background-color: white;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
}
</style>
