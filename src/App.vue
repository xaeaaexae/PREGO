<template>
  <div id="app">
    <header class="header">
      <a href="/">/</a>
      <nav class="header-nav-primary">
        <a href="#about" @click="smoothScroll('about')">about</a>
        <a href="#projects" @click="smoothScroll('projects')">projects</a>
        <a href="#contact" @click="smoothScroll('contact')">contact</a>
        <div class="cursor"></div>
      </nav>
      <div class="hamburger" v-on:click="activeMobileNav">
        <!--
        <svg class="ham hamRotate ham1" viewBox="0 0 100 100" width="80" onclick="this.classList.toggle('active')">
            <path class="line top" d="m 30,33 h 40 c 0,0 9.044436,-0.654587 9.044436,-8.508902 0,-7.854315 -8.024349,-11.958003 -14.89975,-10.85914 -6.875401,1.098863 -13.637059,4.171617 -13.637059,16.368042 v 40" />
            <path class="line middle" d="m 30,50 h 40" />
            <path class="line bottom" d="m 30,67 h 40 c 12.796276,0 15.357889,-11.717785 15.357889,-26.851538 0,-15.133752 -4.786586,-27.274118 -16.667516,-27.274118 -11.88093,0 -18.499247,6.994427 -18.435284,17.125656 l 0.252538,40" />
        </svg>
        -->
      </div>
      <nav class="header-nav-mobile">
        <a href="#about" @click="smoothScroll('about')" v-on:click="CloseMobileNav">about</a>
        <a href="#projects" @click="smoothScroll('projects')" v-on:click="CloseMobileNav">projects</a>
        <a href="#contact" @click="smoothScroll('contact')" v-on:click="CloseMobileNav">contact</a>
      </nav>
    </header>

    <div id="hero">

      <svg class="logo" version="1.1" xmlns="http://www.w3.org/2000/svg" x="0px" y="0px"
           viewBox="0 0 445.9 140.8">

        <path id="letter-5" d="M333.6,52.1c-1.5,2.1-2.6,3.5-3.9,5.6c-0.4,0.7,0.2,1.6,1,1.3c1.7-0.5,3.8-1,4-1.1c3-1.6,7-4,10-5.5
                c16.9-8.3,33.8-16.5,50.7-24.8c0.2-0.1,0.4-0.2,0.8-0.3c-0.9,1.6-1.8,2.9-2.5,4.3c-3,5.6-5.1,11.4-4.7,17.8
                c0.1,5.3,3.6,9.9,8.6,11.4c3.3,1.1,6.9,1.3,10.3,0.8c4.6-0.8,8.9-2.8,12.4-5.9c2.6-2.2,11.7-11.5,11.4-11.7l0.7-1.1
                c3.5-5,6.3-10.4,8.1-16.3c1.1-3.4-0.2-12.1-9.3-12.7c-0.4,0-2.4,0.7,0.1,1.3c1.9,0.5,6,2.9,6,6.5c-0.1,1.1-0.2,2.2-0.5,3.3
                c-1.8,5.7-4.5,11-8,15.8v-0.1c-1.1,1.9-2.9,3.7-4.2,5.1c-0.3,0.3-0.5,0.6-0.9,0.9c-3.8,3.7-7.9,7-13,8.7
                c-1.4,0.4-2.9,0.7-4.3,0.8c-2.6,0.2-4.5-1-5.5-3.4c-0.8-2.1-0.8-4.2-0.4-6.4c1.5-9.9,6.4-18,15-23.4c2.5-1.4,4.1-4,4.1-6.8
                c0.1-1.8-1.3-3.4-3.2-3.5c-2.2,0-4.3,0.7-6.1,1.8c-1.9,1.1-3.7,2.5-5.6,3.5c-7.7,4-15.5,7.9-23.3,11.7
                c-11.9,5.8-23.8,11.5-35.7,17.3c-0.7,0.3-1.3,0.7-2,1c-0.5,0.3-6.6,2.2-8.6,2.6c-0.4,0.1-0.7,0.3-1,0.6L333.6,52.1z"/>
        <path class="st0" id="mask-5" d="M428.8,14.2c1.5,0.2,4.5,0.8,7.1,3.1c1.1,1,3.5,3,3.8,6c0.2,1.8-0.5,2.9-2,5.8c-3.5,6.9-2.4,6.1-4.4,9.6
                c-2,3.4-3.9,5.5-7.1,9.1c-3.5,3.9-5.3,5.9-7.9,7.7c-2,1.3-5.4,3.6-10.3,4.1c-2.5,0.3-7.8,0.1-11-3.4c-3.1-3.1-3.2-6.1-1.7-12.9
                c0.9-4.7,2.8-9.6,6.7-14.8c5.2-7,13.5-11.6,13.3-11.9c-0.4-0.8-37.1,17.5-37.1,17.5c-17.8,8.6-33.5,15.5-43.9,20.3"/>

        <path id="letter-4" d="M342.4,19.5c0.8-0.6,0.7-1.6,0-2.2c-5.7-4.8-12.2-6.9-19.8-5.6c-7,1.2-12.8,4.6-18,9.3c0,0,0,0-0.1,0.1
                c-0.6,0.6-1.2,1.2-1.8,1.7c-3.2,3.3-6.4,6.7-8.2,11.2c-0.1,0.1-0.1,0.2-0.1,0.2c-0.1,0.2-4.3,10.3-3.8,15.7
                c0.3,3.4,1.7,6.2,4.7,7.9c2.8,1.6,6,2,9.2,1.4c3.9-0.8,7.1-2.8,10.3-5c6.8-4.8,12.7-10.6,18.5-16.5l0.1-0.1
                c0.3-0.3,0.5-0.7,0.8-1.1l0.3,0.3c-0.2,0.3-0.3,0.6-0.4,0.8c-4.1,7-8.3,14-12.3,21.1c-0.4,0.7-5.9,9.6-6.2,10.2l-0.1,0.1
                c-2.6,4-5.2,8.1-7.8,12.1c-7.1,10.8-14.4,21.4-22.9,31.1c-4,4.6-8.2,9-13.4,12.3c-2.5,1.5-5,1.8-8.1,2c-1.5,0-2.8,1-3.3,2.4
                c-0.1,0.4-0.3,0.5,0.1,1.1c0.7,0.3,1.4,0.6,2.1,0.7c3.1,0.6,6.3,0.3,9.2-0.8c5.4-1.8,10-5,14.3-8.6c8.2-6.8,15.1-14.8,21.7-23.2
                c9.7-12.6,18.7-25.7,26.9-39.2c0.2-0.4,0.5-0.8,0.7-1.2c1.4-2.9,5-9.1,6.2-10.6c0.1-0.2,0.4-0.7,0.6-0.9l8.3-16.3
                c2-6-2.6-7.4-7.6-4c-9.9,8.2-11.5,8.8-20.8,17.1c-4.1,3.9-8.3,7.6-13.4,10.2c-1.7,0.9-3.6,1.5-5.5,1.8c-2.3,0.4-3.8-0.8-3.9-3.1
                c-0.1-1.3,0.1-2.7,0.4-4c1.4-4.9,3.8-9.5,6.9-13.6c4.3-5.8,9.1-11,15.6-14.5c5.6-3,11.3-3.4,17.1-0.3
                C340.4,20.2,341.3,20.3,342.4,19.5L342.4,19.5z"/>
        <path class="st0" id="mask-4" d="M258.3,128.2c1.5,0.6,3.8,1.3,6.7,1.3c5.1,0,9.1-2.3,12-4.4c14.9-10.8,24.9-27.1,24.9-27.1
                c13.3-21.6-1.8,5.8,28.4-42.9c29-38,12.4-25.5,6.4-21.9c-9.7,9.9-5.1,3.4-16.4,14.5c-6.9,6.8-9.7,9.9-14.7,10.4
                c-3.5,0.4-8.7-0.5-10.9-4c-2.5-4,0.3-9.4,4.9-18.2c3.9-7.6,6.5-10.8,12-14.7c1.8-1.3,7-6.3,14.7-6.4c2.1-0.1,8.9-0.1,14.7,4.2
                c0.6,0.5,1.1,0.9,1.4,1.2"/>

        <path id="letter-3" d="M244.1,27.4c-1,2.6-4.2,3.3-4.8,5.9c1-0.3,12-4.5,17.2-7.6c2.2-1.5,4.1-3.7,4.9-6.3c1.2-4.5-0.7-7.9-5-8.7
                c-1-0.2-2-0.2-3-0.2c-4.7,0.3-9.2,1.9-13,4.6c-2.5,1.8-4.8,3.8-7.2,5.8c-0.3,0.3-0.6,0.6-1,0.9c-3.1,3.3-7.4,11.4-7.5,11.6
                c-1.9,3.9-3,8-3.3,12.3c-0.4,6.6,3,11.7,9.3,13.7c4.3,1.3,8.9,1.4,13.3,0.3c6.4-1.6,12.7-3.9,18.6-7
                c10.7-5.3,34.4-21.3,34.4-21.4c1.5-1.1,3.1-2.3,6.4-5.5c0.9-0.8,1.5-2.3,1.3-2.8c-0.2-0.6-1.4-0.6-2-0.2
                c-7.9,5.2-17.4,11.6-25.3,16.5c-8.1,5.3-16.8,9.8-25.8,13.5c-4,1.8-8.4,2.8-12.8,3.1c-2.9,0.1-5.5-2-6-4.8
                c-0.2-1-0.2-1.9-0.2-2.9c0.4-4.5,1.5-7.9,3.2-12.1c0.1-0.4,0.3-0.8,0.5-1.2c0.8-2.5,5.6-9.7,6-10.3c2.1-3,4.3-5.7,7.2-7.8
                c1.3-1.1,3-1.7,4.7-1.8c1.4-0.2,2.6,0.8,2.8,2.1c0,0.3,0,0.7-0.1,1c-0.2,1.5-1,2.9-2.2,3.8s-2.5,1.7-3.8,2.4
                C248.6,25.8,244.1,27.4,244.1,27.4z"/>
        <path class="st0" id="mask-3" d="M305.5,23.6c-9.6,5.6-19.1,13.5-24.3,16.7c-6.6,4-12.4,7.6-21,11.9c-8.3,4.1-13.8,6.1-20.4,6.2
                                c-4.1,0.1-8.1-0.9-10.7-4.4c-2.3-3.1-3.2-6.9-0.2-14.3c1.6-5.2,3.4-11.3,8.6-17.5c2.8-3.3,5.9-5.9,9.6-7.7c1.5-0.7,4.1-1.7,7.3-1.5
                c1.3,0.1,2.9,0.2,4.1,1.5c1.6,1.5,1.5,3.7,1.5,3.9c0,0.4-0.1,1.6-1.9,3.9c-1.9,2.4-4,3.8-4.6,4.1c-2.8,1.8-5.2,2.6-8.4,3.6"/>

        <path id="letter-2" d="M104.8,36.4c-1,2.2-0.7,2,1.6,3.8c0-0.1,1.4-0.3,1.4-0.4c1-0.3,1.8-0.6,2.8-0.8c5.8-1.5,11.6-3.1,17.5-4.7
                c12.3-3.5,24.2-7.7,34.8-15.1c0.3-0.1,0.7-0.1,1,0c1.4,0.6,2,2.2,1.4,3.6c0,0,0,0.1-0.1,0.1c-0.8,2-1.8,3.8-3,5.6
                c-2.7,3.8-5.6,7.5-8.3,11.3c-2,2.6-3.6,5.7-4.5,8.9c-1,4.1,1,8.4,4.8,10.2c0.6,0.3,1.3,0.6,2,0.8c4.7,1.3,9.6,1.5,14.4,0.5
                c7.1-1.5,13.6-4.7,22.2-8.1c11.1-5,18.8-8,30.2-12.7c0.4-0.2,15.5-5.9,16.7-6.3c1.1-0.4,7-4.3,4.4-5.7
                c-15.3,5.4-32,12.6-47.1,18.8c-8.4,3.6-14.4,6-22.1,8.3c-3,1.1-6.3,1.6-9.5,1.3c-1.8-0.2-5.1-2.2-4.9-4c0.2-1.9,1.5-3.6,2.5-5.2
                c2.9-5,6.5-9.8,9.7-14.7c2.1-3.3,4.3-6.5,6.1-10c1.6-2.9,0.5-5.4-2.6-6.8c-0.5-0.3-1.1-0.5-1.7-0.6c-4.2-0.9-8.6-1.2-12.9-0.7
                c-0.5,0-1,0.8-1.4,1.2c-0.4,0.5-0.6,1-1,1.2c-3.6,2.2-7.2,4.4-10.9,6.2c-8.7,4.2-18,6.9-27.2,9.4L105,36.2L104.8,36.4z"/>
        <path class="st0" id="mask-2" d="M245.1,30c-5.7,1.8-7.6,2.1-11.4,3.3c-2.3,0.7-3.2,0.8-7.4,2.6l-4,1.4c-7.5,1.8-12.2,4.4-16,6.2
                c-7.1,3.3-8.8,5.2-18.1,9.3c-0.9,0.4-6.2,2.7-13.3,4.6c-4.5,1.2-7.1,1.5-9.9,1.3c-2.4-0.2-8-0.9-9.3-3.7c-0.3-0.7-2.2-2.4,0.1-7.3
                c1.8-3.8,4.1-6.2,7-10.7c6.3-10.1,5.9-9,6.3-9.6c1.4-1.9,4.4-3.3,5-6.3c0.2-0.8-0.4-3-1.7-4c-0.9-0.7-1.7,0.2-4.4,0.1
                c-2.9,0-3.5-1-5.2-0.4c-1.5,0.5-1.8,1.5-3.3,3c-1.4,1.4-2.7,2.1-6.1,3.6c-8.2,3.6-12.3,5.5-16.1,6.7c-11,3.6-20.8,6.3-27.4,7.8"/>

        <path id="letter-1" d="M7.1,124.5c-0.1,0.7,0.3,1.4,1,1.6c0.2,0.1,0.4,0.1,0.6,0.1c1.2,0.2,2.5,0.1,3.7-0.1c4-0.8,7.2-3.3,10.2-5.8
                c6.3-5.4,11.5-11.8,16.5-18.3c9.3-12.4,27.8-48.8,29.7-51.9c0-0.1,3.5-6.4,4.1-7.4c5.5-8.9,6.7-9.4,13.4-15.8
                c2.1-1.8,5.7-4.3,8.7-5.4c1.1-0.5,3.9-1.1,5-1.3c2.1-0.2,3,0.2,3.1,2.2c-0.1,2.1-0.4,4.3-1.1,6.3v0.1c-1.1,3.2-2.7,6.2-4.1,9.3
                c0,0.1-3.6,6.4-3.8,6.7c-4.1,6.1-8.4,11.9-14.2,16.4c-1.8,1.4-3.4,2.9-5.8,3.3c-0.6,0.1-1.1,0.2-1.7,0.3c-0.1,0-0.3,0-0.4,0
                c-1.5-0.2-5.1-0.3-5.2,1.4c0,1.8,3.6,2.6,5.9,2.4c4.3,0,8.6-1.1,12.4-3.3c10.2-5.6,17.6-13.9,23.1-24c0.7-1.2,1.1-2.5,1.7-3.8
                c0.5-0.9,0.9-1.8,1.3-2.8c0.1-0.6,0.3-1,0.4-1.4c0.5-2.4,0.8-4.9,1-7.3c0.3-4-1.9-7.7-5.5-9.2c-3.8-1.5-8.3-1.7-12.1-0.2
                c-6.9,2.4-9,4-11.4,5.8c-3,2.1-8.1,6.5-10.3,9c-9.1,10.1-14.7,18.7-22,32C51,64,44.1,76.2,44.1,76c-0.1,0.2-0.1,0.3-0.2,0.5
                c-6.5,11.1-12.8,22.3-20.2,32.8c-2.7,3.9-9,11.5-13.4,13.4C9.1,123.2,7.5,122.3,7.1,124.5"/>
        <path class="st0" id="mask-1" d="M66.8,66.2c3.2-0.2,11.6,0.1,13.7-0.8c4.5-2,7.7-4.7,9.4-6.3c0.5-0.4,2.7-3.3,7.1-8.9c2.5-3.2,3.1-4.9,4.3-6.9
                c0.6-1.1,1.7-2.8,3.3-6.4c3.1-6.7,3.2-7.6,3.3-9c0.1-1.2,1-4.7-1.1-7.1c-1-1.1-2.2-1.7-2.4-1.9c-1.5-0.8-2.9-0.8-3.8-0.9
                c-0.6,0-1.9-0.1-3.3,0.3c-1.8,0.5-2.9,1.4-4.2,2.4c-1,0.6,0.1,0-3.4,1.8c-2.7,1.6-2,1.1-2.8,1.7c-2.4,1-3.2,2.4-4.9,3.7
                c-1.7,2-12,12.2-15.9,20.1c-2.5,5-6,11-12.8,23.8c-7.7,10.4-7.7,10.4-10.6,15.1c-3.8,6-6.1,12.6-9.4,16.9c-3.2,4.3-5.2,6.8-8.1,10
                c-2.8,3-3.3,3.1-5.5,5.7c-1.9,2.3-2.4,3.3-4.1,4.3c-2.4,1.3-5,1.4-5.7,1.4c-1,0-3.2-0.5-3.8-0.6"/>
      </svg>
      <h1>
        <span class="h1">LOREM IPSUM</span>
        <span class="h1">DOLOR SIT AMET</span>
      </h1>


      <div class="scroll-down">
        <span class="scroll-button" @click="smoothScroll('about')">scroll down</span>
        <div class="scroll-line"></div>
      </div>
    </div>
    <div class="about"></div>
    <div class="projects"></div>
    <div class="contact"></div>
    <div class="coming-soon">ADIPISCING</div>

  </div>
</template>

<script setup>
import {gsap} from "gsap";
import {ScrollToPlugin} from "gsap/ScrollToPlugin";
import {onMounted} from "vue";

gsap.registerPlugin(ScrollToPlugin);

function smoothScroll(id) {
  gsap.to(window, {duration: 1, scrollTo: `.${id}`});
}

function activeMobileNav(event) {
  const navMobile = document.querySelector(".header-nav-mobile");

  if (event.target.classList.contains("active")) {
    event.target.classList.remove("active");
    navMobile.classList.remove("open");
  } else {
    event.target.classList.add("active");
    navMobile.classList.add("open");
  }
}

function closeMobileNav() {
  const navMobile = document.querySelector(".header-nav-mobile");
  const hamburger = document.querySelector(".hamburger");
  navMobile.classList.remove("open");
  hamburger.classList.remove("active");
}

onMounted(() => {
  gsap.set(".cursor", {xPercent: -50, yPercent: -50});

  const ball = document.querySelector(".cursor");
  const pos = {x: window.innerWidth / 2, y: window.innerHeight / 2};
  const mouse = {x: pos.x, y: pos.y};
  const speed = 0.2;

  const xSet = gsap.quickSetter(ball, "x", "px");
  const ySet = gsap.quickSetter(ball, "y", "px");

  window.addEventListener("mousemove", (e) => {
    mouse.x = e.x;
    mouse.y = e.y;
  });

  gsap.ticker.add(() => {
    pos.x += (mouse.x - pos.x) * speed;
    pos.y += (mouse.y - pos.y) * speed;
    xSet(pos.x);
    ySet(pos.y);
  });
});
</script>

<style>
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@-webkit-keyframes bounceIn {
  0% {
    -webkit-transform: scale(0.1);
    transform: scale(0.1);
    opacity: 0;
  }
  60% {
    -webkit-transform: scale(1.2);
    transform: scale(1.2);
    opacity: 1;
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

@keyframes bounceIn {
  0% {
    -webkit-transform: scale(0.1);
    transform: scale(0.1);
    opacity: 0;
  }
  60% {
    -webkit-transform: scale(1.2);
    transform: scale(1.2);
    opacity: 1;
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}


@font-face {
  font-family: "Source Code Pro";
  src: url("assets/SourceCodePro-Regular.ttf");
}

@font-face {
  font-family: "Muli";
  src: url("assets/Muli-VariableFont_wght.ttf");
}

/* --- GENERAL --*/
html {
  /*scroll-behavior: smooth;*/
}

body {
  margin: 0;
}

#app {
  background: #ffffff;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  text-align: center;
  min-height: 100vh;
  position: relative;
  z-index: 1;
}

::-webkit-scrollbar {
  display: none;
}

/* --- NAVIGATION --- */
.header {
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  height: 100px;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
  margin: 0 auto;
  max-width: 2200px;
  padding: 0 30px;
  text-align: center;
}

.header a {
  color: #000000;
  font-family: "Muli";
  font-size: 24px;
  margin: 0 15px;
  padding: 10px 15px;
  text-decoration: none;
}

.header > a {
  pointer-events: none;
}

header .hamburger {
  display: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.hamburger {
  display: block;
  width: 24px;
  cursor: pointer;
  z-index: 3;
}

.hamburger.active {
  position: fixed;
  right: 30px;
}

.hamburger:before,
.hamburger:after {
  background-color: #000;
  content: "";
  display: block;
  height: 2px;
  -webkit-transition: all 200ms ease-in-out;
  -o-transition: all 200ms ease-in-out;
  transition: all 200ms ease-in-out;
}

.hamburger:before {
  -webkit-box-shadow: 0 8px 0 #000;
  box-shadow: 0 8px 0 #000;
  margin-bottom: 14px;
}

.hamburger.active:before {
  -webkit-box-shadow: 0 0 0 #000;
  box-shadow: 0 0 0 #000;
  -webkit-transform: translateY(8px) rotate(45deg);
  -ms-transform: translateY(8px) rotate(45deg);
  transform: translateY(8px) rotate(45deg);
}

.hamburger.active:after {
  -webkit-transform: translateY(-8px) rotate(-45deg);
  -ms-transform: translateY(-8px) rotate(-45deg);
  transform: translateY(-8px) rotate(-45deg);
}

.hamburger.active:before,
.hamburger.active:after {
  background-color: #fff;
}

@media (hover: hover) and (pointer: fine) {
  .hamburger:hover:before,
  .hamburger:hover:after {
    background-color: #ed254e;

  }

  .hamburger:hover:before {
    -webkit-box-shadow: 0 8px 0 #ed254e;
    box-shadow: 0 8px 0 #ed254e;
  }

  .hamburger.active:before {
    -webkit-box-shadow: 0 0 0 #ed254e;
    box-shadow: 0 0 0 #ed254e;
  }
}

.header-nav-mobile {
  /*display: none; LAAAAA*/
  display: block;
  opacity: 0;
  z-index: 2;
  position: fixed;
  top: -100%;
  left: 0;
  width: 100%;
  height: 100vh;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  overflow: hidden;
}

.header-nav-mobile:before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;
  background: rgba(0, 0, 0, 0.98);
  width: 100%;
  height: 0;
  padding-bottom: 100%;
  border-radius: 100%;
  overflow: hidden;
  /*display: block;*/
}

.open.header-nav-mobile {
  display: block;
  top: 0;
  opacity: 1;
}

.open.header-nav-mobile:before {
  -webkit-animation: menu-animation 0.8s ease-out forwards;
  animation: menu-animation 0.8s ease-out forwards;
}

@-webkit-keyframes menu-animation {
  0% {
    opacity: 0;
    -webkit-transform: scale(0.04) translateY(300%);
    transform: scale(0.04) translateY(300%);
  }
  40% {
    -webkit-transform: scale(0.04) translateY(0);
    transform: scale(0.04) translateY(0);
    -webkit-transition: ease-out;
    -o-transition: ease-out;
    transition: ease-out;
  }
  40% {
    -webkit-transform: scale(0.04) translateY(0);
    transform: scale(0.04) translateY(0);
  }
  60% {
    opacity: 1;
    -webkit-transform: scale(0.02) translateY(0px);
    transform: scale(0.02) translateY(0px);
  }
  61% {
    -webkit-transform: scale(0.04);
    transform: scale(0.04);
  }
  99.9% {
    height: 0;
    padding-bottom: 100%;
    border-radius: 100%;
  }
  100% {
    -webkit-transform: scale(2);
    transform: scale(2);
    height: 100%;
    padding-bottom: 0;
    border-radius: 0;
  }
}

@keyframes menu-animation {
  0% {
    opacity: 0;
    -webkit-transform: scale(0.04) translateY(300%);
    transform: scale(0.04) translateY(300%);
  }
  40% {
    -webkit-transform: scale(0.04) translateY(0);
    transform: scale(0.04) translateY(0);
    -webkit-transition: ease-out;
    -o-transition: ease-out;
    transition: ease-out;
  }
  40% {
    -webkit-transform: scale(0.04) translateY(0);
    transform: scale(0.04) translateY(0);
  }
  60% {
    opacity: 1;
    -webkit-transform: scale(0.02) translateY(0px);
    transform: scale(0.02) translateY(0px);
  }
  61% {
    -webkit-transform: scale(0.04);
    transform: scale(0.04);
  }
  99.9% {
    height: 0;
    padding-bottom: 100%;
    border-radius: 100%;
  }
  100% {
    -webkit-transform: scale(2);
    transform: scale(2);
    height: 100%;
    padding-bottom: 0;
    border-radius: 0;
  }
}


.open.header-nav-mobile a {
  color: #ffffff;
  z-index: 3;
  font-size: 35px;
  opacity: 0;
  -webkit-animation: fade 0.3s ease-in forwards;
  animation: fade 0.3s ease-in forwards;
  -webkit-animation-delay: 0.4s;
  animation-delay: 0.4s;
  margin: 30px auto 0 auto;
  display: block;
  width: 150px;
}

.header-nav-mobile a:nth-child(1) {
  margin-top: 100px;
}

.header-nav-mobile a:nth-child(2) {
  margin-top: 20px;
}

.header-nav-mobile a:nth-child(3) {
  margin-top: 20px;
}


/* --- TITLE --- */
h1 {
  -webkit-animation: fade 0.3s ease-in forwards;
  animation: fade 0.3s ease-in forwards;
  -webkit-animation-delay: 3s;
  animation-delay: 3s;
  left: 50%;
  margin-left: 470px;
  margin-right: -50%;
  opacity: 0;
  position: absolute;
  top: 45%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
}

h1 span.h1 {
  color: #000000;
  display: block;
  font-family: "Muli";
  font-size: 16px;
  font-weight: normal;
  text-align: left;
}

@-webkit-keyframes fade {
  0% {
    opacity: 0;
  }
  50% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
  }
}

@keyframes fade {
  0% {
    opacity: 0;
  }
  50% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
  }
}

/* --- SVG --- */
#hero {
  min-height: calc(100vh - 100px);
  position: relative;
  z-index: -1;
}

svg.logo {
  left: 50%;
  margin-left: -25px;
  margin-right: -50%;
  position: absolute;
  top: 45%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  width: 700px;
  z-index: -2;
}

.st0 {
  fill: none;
  stroke: #ffffff;
  stroke-width: 14;
  stroke-miterlimit: 10;
  stroke-dashoffset: 0;
  stroke-dasharray: 360;
}

#mask-1 {
  -webkit-animation: write 1.4s 1 ease-in-out forwards;
  animation: write 1.4s 1 ease-in-out forwards;
  animation-direction: reverse;
}

#mask-2 {
  -webkit-animation: write 2s 1 ease-out forwards;
  animation: write 2s 1 ease-out forwards;
  -webkit-animation-delay: 0s;
  animation-delay: 0s;
  animation-direction: reverse;
}

#mask-3 {
  -webkit-animation: write 2s 1 ease-out forwards;
  animation: write 2s 1 ease-out forwards;
  -webkit-animation-delay: 0.4s;
  animation-delay: 0.4s;
  animation-direction: reverse;
}

#mask-4 {
  -webkit-animation: write 1.4s 1 ease-out forwards;
  animation: write 1.4s 1 ease-out forwards;
  -webkit-animation-delay: 1.4s;
  animation-delay: 1.4s;
  animation-direction: reverse;
}

#mask-5 {
  -webkit-animation: write 2s 1 ease-in-out forwards;
  animation: write 2s 1 ease-in-out forwards;
  -webkit-animation-delay: 1.6s;
  animation-delay: 1.6s;
  animation-direction: reverse;
}

@-webkit-keyframes write {
  0%, 25% {
    stroke-dashoffset: 360;
  }
  90% {
    stroke-dashoffset: 0;
  }
}

@keyframes write {
  0%, 25% {
    stroke-dashoffset: 360;
  }
  90% {
    stroke-dashoffset: 0;
  }
}

/* --- BUTTON SCROLL --- */
.scroll-button {
  font-family: "Muli";
  font-size: 14px;
  cursor: pointer;
  color: rgba(75, 87, 92, 0.6);
  text-transform: uppercase;
}

.scroll-line {
  background: rgba(75, 87, 92, 0.2);
  height: 66px;
  margin: 5px auto 5px auto;
  width: 1px;
}

.scroll-down {
  width: 100%;
  bottom: 0;
  left: 0;
  position: absolute;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  height: 140px;
  border-bottom: rgba(237, 37, 78, .4) 20px solid;
  /*border-bottom: rgba(193, 209, 117, .4) 70px solid;*/
}

/* --- SECTIONS --- */
.projects, .about, .contact {
  min-height: 100vh;
  z-index: 1;
}

.about, .projects, .contact {
  /*background: #b6b6b4;*/
  background: rgba(237, 37, 78, .4);
  /*background: #e6edc8;*/
}


/* --- CURSOR --- */
.cursor {
  width: 12px;
  height: 12px;
  position: fixed;
  top: 0;
  left: 0;
  /*background: #c1d175;*/
  background: #ed254e;
  border-radius: 100%;
  z-index: -1;
}

@media (hover: hover) and (pointer: fine) {
  .header a:hover {
    color: #ed254e;

  }

  .header a:hover ~ .cursor, .header a:hover ~ .header-nav-primary > .cursor {
    background: rgba(237, 37, 78, .4);
    -webkit-animation: in 0.3s ease-out forwards;
    animation: in 0.3s ease-out forwards;
  }
}

@-webkit-keyframes in {
  100% {
    width: 80px;
    height: 80px;
  }
}

@keyframes in {
  100% {
    width: 80px;
    height: 80px;
  }
}

@-webkit-keyframes out {
  100% {
    width: 12px;
    height: 12px;
  }
}

@keyframes out {
  100% {
    width: 12px;
    height: 12px;
  }
}

.coming-soon {
  -webkit-writing-mode: vertical-rl;
  -ms-writing-mode: tb-rl;
  writing-mode: vertical-rl;
  -webkit-text-orientation: upright;
  text-orientation: upright;


  height: calc(100vh + 100vh + 100vh);

  font-size: 20vh;
  position: absolute;
  top: 100vh;
  font-family: Muli;

  left: 50%;
  -webkit-transform: translate(-50%, 0);
  -ms-transform: translate(-50%, 0);
  transform: translate(-50%, 0);
}

/* --- RESPONSIVE --- */
@media (max-width: 1300px) {
  .header-nav-primary a {
    font-size: 18px;
    padding: 10px 5px;
    margin: 0 10px;
  }

  svg.logo {
    width: 500px;
    top: 40%;
  }

  h1 {
    margin-left: 300px;
    top: 40%;
  }

  h1 span.h1 {
    font-size: 14px;
  }

  .scroll-down {
    height: 130px;
    border-bottom: rgba(237, 37, 78, .4) 60px solid;
  }

  @-webkit-keyframes in {
    100% {
      width: 60px;
      height: 60px;
    }
  }

  @keyframes in {
    100% {
      width: 60px;
      height: 60px;
    }
  }
}

@media (max-width: 1000px) {
  .header-nav-primary a {
    font-size: 16px;
  }

  svg.logo {
    width: 400px;
  }

  h1 {
    margin-left: 250px;
  }

}

@media (min-width: 801px) {
  .header-nav-primary {
    display: block;
  }

  .header-nav-mobile {
    display: none !important;
  }
}

@media (max-width: 800px) {
  .header-nav-primary {
    display: none;
  }

  .header > a {
    margin: 0;
    padding: 10px 0;
  }

  .hamburger {
    display: block !important;
  }

  svg.logo {
    margin-left: 0;
    top: 35%;
  }

  h1 span.h1 {
    text-align: right;
  }

  h1 {
    margin-left: 120px;
    margin-top: 90px;
    top: 35%;
  }

  .scroll-down {
    height: 120px;
    border-bottom: rgba(237, 37, 78, .4) 50px solid;
  }
}

@media (max-width: 600px) {
  svg.logo {
    width: 300px;
  }

  h1 {
    margin-left: 70px;
  }
}

@media (max-width: 400px) {
  svg.logo {
    width: 200px;
  }

  h1 {
    margin-left: 23px;
  }
}

</style>
