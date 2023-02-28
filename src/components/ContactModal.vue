<template>
  <transition name="fade" appear>
    <div class="modal-overlay">
      <div class="modal">
        <h6>Contact</h6>

        <hr>

          <ul class="contact-list">
            <li class="list-item"><span class="contact-text place">Perth, Western Australia</span></li>
            
            <li class="list-item"><span class="contact-text phone">+61 468 791 549</span></li>
            
            <li class="list-item"><span class="contact-text gmail"><a href="mailto:#" title="Send me an email">jevcwatson@gmail.com</a></span></li>
          
          </ul>
          
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
/* Location, Phone, Email Section */
.contact-list {
  list-style-type: none;
  margin-left: -30px;
  padding-right: 20px;
}

.list-item {
  line-height: 3;
  color: #aaa;
}

.contact-text {
  font-family: 'Hanken Grotesk', sans-serif;
  font-weight: 300;
  font-size: 18px;
  letter-spacing: 1.9px;
  color: white;
}

.place {
  margin-left: 62px;
}

.phone {
  margin-left: 56px;
}

.gmail {
  margin-left: 53px;
}

.contact-text a {
  color: white;
  text-decoration: none;
  transition-duration: 0.2s;
}

.contact-text a:hover {
  color: #fff;
  font-size: 20px;
  text-decoration: none;
}
</style>