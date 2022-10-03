<template>
    <div>
        <div class="section-2 w-full flex flex-col md:flex-row justify-center md:items-center px-3 md:px-6 pb-10">
        <div class="w-full md:w-1/2 section-vid-container">
          <div class="section-vid w-[26rem] h-[29rem] overflow-hidden">
            <div class="section-vid__inner w-full h-full rellax" id="vid1"></div>
          </div>
        </div>
        <div class="w-full md:w-1/2 section-desc text-center md:text-left md:px-6">
          <div class="desc-title text-[2rem] font-black">ELEGANCE</div>
          <div class="desc-text">
            <p class="opacity-80">
              Utopia is a model agency that represents models, actors, and influencers from all over the world. We are a team of professionals who are passionate about the industry and are dedicated to providing the best service to our clients.
            </p>
            <p>
              <a href="#" class="desc-link">Learn More</a>
            </p>
          </div>


        </div>
      </div>
    </div>
</template>

<script>
import vidim from 'vidim';

const vidimInit = ()=>{
    var myBackground = new vidim( '#vid1', {
        src: [
          {
            type: 'video/webm',
            src: '/vid/pexels-polina-kovaleva-7089248.webm'
          }
        ],
      });
}

document.addEventListener("DOMContentLoaded", ()=>{
    vidimInit()
})
</script>