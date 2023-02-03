<template>
    <div class="modal-overlay">
      <div class="modal">
        <h6>About Me</h6>
        <hr>
        <br>
        <p>I am a software developer based in Western Australia.</p>
        <br>
        <p>My career thus far has seen me focused on front end web application development. I have experience in a variety of programming languages and frameworks and possess a continuous desire to learn and improvemy skill set.</p>
        <br>
        <hr>
        <button @click="$emit('close-modal')">Close</button>
      </div>
    </div>
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