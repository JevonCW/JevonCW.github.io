<template>
  <div class="main">

    <div>
      <AboutModal v-show="showAbout" @close-modal="showAbout = false"/>
      <ProjectsModal v-show="showProjects" @close-modal="showProjects = false"/>
      <ContactModal v-show="showContact" @close-modal="showContact = false"/>
    </div>

    <div class="title">Jevon Watson</div>

    <div class="imgcontainer">

      <div class="img-left">
        <div class="frame">
          <a href="https://github.com/JevonCW" target=”_blank”><img class="frame-img" src="./assets/img/Abstract3D-1-text.png" loading="lazy" alt="..."></a>
        </div>
        <div class="frame">
          <a @click="showAbout = true"><img class="frame-img" src="./assets/img/Abstract3D-2-text.png" loading="lazy" alt="..."></a>
        </div>
      </div>

      <div class="center">
        <div class="frame-main">
          <a href="./assets/docs/Jevon-Watson-Resume.pdf" download><img class="frame-img" src="./assets/img/Abstract3D-0-text.png" loading="lazy" alt="..."></a>
        </div>
      </div>

      <div class="img-right">
        <div class="frame">
          <a @click="showProjects = true"><img class="frame-img" src="./assets/img/Abstract3D-3-text.png" loading="lazy" alt="..."></a>
        </div>
        <div class="frame">
          <a @click="showContact = true"><img class="frame-img" src="./assets/img/Abstract3D-4-text.png" loading="lazy" alt="..."></a>
        </div>
      </div>
    </div>

    <div class="cube-container">
      <div class="cube">
        <div class="face front"></div>
        <div class="face back"></div>
        <div class="face left"></div>
        <div class="face right"></div>
        <div class="face top"></div>
        <div class="face bottom"></div>
        <div class="shadow"></div>
      </div>
    </div>
  </div>  

</template>

<script>
import "@/assets/styles/reset.css";
import "@/assets/styles/global.css";
import "@/assets/styles/frames.css";
import "@/assets/styles/cube.css";


import AboutModal from './components/AboutModal.vue'
import ProjectsModal from './components/ProjectsModal.vue'
import ContactModal from './components/ContactModal.vue'

export default {
  name: "App",
  components: {
    AboutModal,
    ProjectsModal,
    ContactModal,
  },
  data() {
    return {
      showAbout: false,
      showProjects: false,
      showContact: false,
    }
  },
};
</script>

<style>
/* Define Font(s) */
@import url('https://fonts.googleapis.com/css2?family=Cinzel&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Hanken+Grotesk:wght@300&display=swap');

/* Primary Div Styling */

.main{
  max-width: 100%;
  height: 100vh;
  margin: 0 auto;
  padding: 0 20px 0 20px;
  background: radial-gradient(75% 35% at 50% 95%, rgba(33, 33, 35, 0.6) 20%, rgba(80, 82, 98, 0) 90%),
  linear-gradient(rgba(28, 35, 50, 0) 15%, rgb(228, 228, 228) 80%);
}

/* Title Styling */

.title {
  display: block;
  font-family: "Cinzel",serif;
  font-size: 95px;
  color: rgb(196, 196, 196);
  position: fixed;
  top: 10%;
  left: 50%;
  transform: translate(-50%, -50%);
  white-space: nowrap;
}
</style>