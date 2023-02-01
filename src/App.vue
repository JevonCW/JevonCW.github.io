<template>
  <div class="main">

    <div>
    <AboutModal v-show="showAbout" @close-modal="showAbout = false"/>
    <ProjectsModal v-show="showProjects" @close-modal="showProjects = false"/>
    <ContactModal v-show="showContact" @close-modal="showContact = false"/>
    <ResumeModal v-show="showResume" @close-modal="showResume = false"/>
    </div>

    <div class="title">Jevon Watson</div>

    <div class="container">

      <div class="img-left">
        <div class="frame">
          <a href="https://github.com/JevonCW" target=”_blank”><img class="frame-img" src="./assets/img/Abstract3D-1-text.png" ></a>
        </div>
        <div class="frame">
          <a @click="showAbout = true"><img class="frame-img" src="./assets/img/Abstract3D-2-text.png"></a>
        </div>
      </div>

      <div class="center">
        <div class="frame-main">
          <a @click="showResume = true"><img  lass="frame-img" src="./assets/img/Abstract3D-0-text.png"></a>
        </div>
      </div>

      <div class="img-right">
        <div class="frame">
          <a @click="showProjects = true"><img class="frame-img" src="./assets/img/Abstract3D-3-text.png"></a>
        </div>
        <div class="frame">
          <a @click="showContact = true"><img class="frame-img" src="./assets/img/Abstract3D-4-text.png"></a>
        </div>
      </div>
    </div>
    <div class="cube-container">
      <div id="cube">
        <div id="front"></div>
        <div id="back"></div>
        <div id="left"></div>
        <div id="right"></div>
        <div id="top"></div>
        <div id="bottom"></div>
        <div class="shadow"></div>
      </div>
    </div>
  </div>
</template>

<script>
import "@/assets/styles/reset.css";
import "@/assets/styles/global.css";

import AboutModal from './components/AboutModal.vue'
import ProjectsModal from './components/ProjectsModal.vue'
import ContactModal from './components/ContactModal.vue'
import ResumeModal from './components/ResumeModal.vue'

export default {
  name: "App",
  components: {
    AboutModal, 
    ProjectsModal, 
    ContactModal, 
    ResumeModal,
  },
  data() {
    return {
      showAbout: false,
      showProjects: false,
      showContact: false,
      showResume: false,
    }
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700;900&display=swap");
@font-face {
    font-family: Cinzel;
    src: url('~@/assets/fonts/cinzel/Cinzel-Regular.ttf');
}

.main{
  max-width: 100%;
  height: 100vh;
  margin: 0px auto;
  padding: 0px 20px 0px 20px;
  background: radial-gradient(75% 35% at 50% 95%, rgba(33, 33, 35, 0.6) 20%, rgba(80, 82, 98, 0) 90%), 
  linear-gradient(rgba(28, 35, 50, 0) 15%, rgb(228, 228, 228) 80%);
}
.title {
  font-family: Cinzel;
  font-size: 95px;
  color: white;
  position: fixed;
  top: 10%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  overflow: visible;
  white-space: nowrap;
}
.container {
  position: fixed;
  top: 55%;
  left: 50%;
  width: 65%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  display: flex;
  flex-direction: row;}
.img-left {
  display: flex;
  flex-direction: column;
  margin-right: 90px;
}
.img-center {
  justify-content: center;
}
.img-right {
  display: flex;
  flex-direction: column;
  margin-left: 90px;
}
div[class^="frame"] {
	display: inline-block;
  height: auto;
  margin-bottom: 25px;
	padding: 7.5px;
	background: #f5f5f5;
	background-image: linear-gradient(#a9a8a3, #878781);
	box-shadow: inset 0 2px 5px rgba(0,0,0,.6),0 5px 2px rgba(0,0,0,.1), 0 10px 20px rgba(0,0,0,.8);
	position: relative;
	overflow: hidden;
}
.frame-img {
	box-shadow:  0 -1px 1px rgba(0,0,0,.1), 0 1px 1px 1px rgba(69, 69, 69, 0.7);
}
.frame{
  max-width: 750px;
}
.frame-main {
  max-width: 1250px;
  top: 27.5%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
}
.cube-container {
  position: fixed;
  top: 80%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
}
#cube {
    width: 100px;   
    transform-style: preserve-3d; 
    animation: rotate 15s linear infinite;
}

#cube div {
    position: absolute;
    width: 100px;
    height: 100px;
    opacity: 0.9 ;
    color: white;
}

#front {
    transform: translateZ(50px);
    background: transparent;
    outline: auto;
    outline-width: 2px;
    background-position: center;
    background-repeat: no-repeat;
    background-size: 500px ;
}


#back {
    transform: rotateY(180deg) translateZ(50px);
    background: transparent;
    outline: auto;
    outline-width: 2px;
    background-position: center;
    background-repeat: no-repeat;
    background-size: 500px ;   
}

#left {
    transform: rotateY(-90deg) translateX(-50px);
    transform-origin: left;
    background: transparent;
    outline: auto;
    outline-width: 2px;
    background-position: center;
    background-repeat: no-repeat;
    background-size: 500px ;  
}

#right {
    transform: rotateY(90deg) translateX(50px);
    transform-origin: right;
    background: transparent;  
    outline: auto;
    outline-width: 2px;
    background-position: center;
    background-repeat: no-repeat;
    background-size: 500px ;  
}

#top {
    transform: rotateX(-90deg) translateY(-50px);
    transform-origin: top;
    background: transparent;
    outline: auto;
    outline-width: 2px;
    background-position: center;
    background-repeat: no-repeat;
    background-size: 500px ;   
}

#bottom {
    transform: rotateX(90deg) translateY(50px);
    transform-origin: bottom;
    background: transparent;
    outline: auto;
    outline-width: 2px;
    background-position: center;
    background-repeat: no-repeat;
    background-size: 500px ;   
}

@keyframes rotate {
    0% { transform: rotateX(-45deg) rotateY(45deg) rotateZ(0deg); }
    100% { transform: rotateX(-45deg) rotateY(405deg) rotateZ(0deg); }
}
.shadow {
    width:100px;
    height:100px;
    background: rgba(0,0,0,0.5);
    box-shadow: 0 0 50px 50px rgba(0,0,0,0.5);
    -webkit-transform: rotateX(90deg) translateZ(-250px) rotateY(180deg) translateX(0px);

}
</style>