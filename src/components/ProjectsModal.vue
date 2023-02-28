<template>
  <transition name="fade" appear>
    <div class="modal-overlay">
      <div class="modal">
        <h6>Project Demos</h6>
        <hr>
        <h6>Coming Soon</h6>
        <hr>
        <button @click="$emit('close-modal')">Close</button>
      </div>
    </div>
  </transition>
  </template>
  
  <script>
    import "@/assets/styles/modal.css";
    export default {};
  </script>

<style scoped>
</style>