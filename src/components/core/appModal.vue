<template>
  <div class="modal">
    <div class="modal-content">
      <slot></slot>
      <button @click="close">Close</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppModal",
  methods: {
    close() {
      this.$emit("close")
    },
  },
}
</script>

<style scoped>
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 20;
}

.modal-content {
  background: white;
  padding: 2rem;
  border-radius: 4px;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  min-width: 600px;
  min-height: 450px;
}

.modal-content button {
  margin-left: auto;
  margin-top: auto;
  background-color: #4285f4;
  border-color: #4285f4;
  text-transform: capitalize;
  border-radius: 5px;
  color: #fff;
  text-decoration: none;
  font-size: 18px;
  padding: 8px 20px;
  box-shadow: 0px 3px 5px #f2f2f2;
}
</style>
