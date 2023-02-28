<template>
  <transition name="fade" appear>
    <div class="modal-overlay">
      <div class="modal">
        <h6>About Me</h6>
        <hr>
        <br>
        <p>I am a software developer based in Western Australia.</p>
        <br>
        <p>Experienced in a variety of programming languages and frameworks. I have several years experience developing software in small to medium agile development teams focused on delivering quality applications to my clients.</p>
        <br>
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
  p {
    font-family: 'Hanken Grotesk', sans-serif;
    font-weight: 300;
    font-size: 18px;
    letter-spacing: 1.9px;
    color: white;
    }
</style>