<script setup>
  // import Hero from './components/Hero.vue'
import Hero from './components/Hero.vue'
import Section2 from './components/Section2.vue'
// import Section3 from './components/Section3.vue';
import OurMission from './components/OurMission.vue';
import Info from './components/Info.vue';
import Highlights from './components/Highlights.vue';
import Team from './components/Team.vue';
import Footer from './components/Footer.vue';
</script>

<template>
<div>

<Hero/>
<Section2/>
<!-- <Section3/> -->
<Info/>
<OurMission/>
<Highlights/>
<Team/>
<Footer/>

</div>
</template>

<script>
import Lenis from '@studio-freight/lenis'
import Rellax from 'rellax';


  const smoothScroll = ()=>{

const lenis = new Lenis({
  duration: 1.2,
  easing: (t) => (t === 1 ? 1 : 1 - Math.pow(2, -10 * t)), // https://easings.net
  direction: 'vertical',
  smooth: true,
  smoothTouch: false,
  touchMultiplier: 2,
})

function raf(time) {
  lenis.raf(time)
  requestAnimationFrame(raf)
}

requestAnimationFrame(raf)
}

const parralax = ()=>{
    const rellax = new Rellax('.rellax');
}


document.addEventListener('DOMContentLoaded', ()=>{
    smoothScroll()
    parralax()
})
</script>