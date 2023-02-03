<template>
    <div class="modal-overlay">
      <div class="modal">
        <h6>About Me</h6>
        <button @click="$emit('close-modal')">Close</button>
      </div>
    </div>
  </template>
  
  <script>
    import "@/assets/styles/modal.css";
    export default {};
  </script>

<style scoped>

</style>