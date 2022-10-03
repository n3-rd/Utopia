<template>
    <div>
        <div class="w-screen h-64 md:h-screen md:my-24 mb-24" id="infovid">

            <div class="absolute bottom-0 left-4 text-4xl md:text-8xl font-black pb-5">
                <div class="text-4xl">Founded By</div>
                Leoni Amerish
            </div>
        </div>
    </div>
</template>

<script>
    import vidim from 'vidim';

const vidimInit = ()=>{
    var myBackground = new vidim( '#infovid', {
        src: [
          {
            type: 'video/webm',
            src: '/vid/pexels-cottonbro-9511255.webm'
          },

        ],
        backgroundSize: 'cover',
        backgroundPosition: 'center',
        backgroundAttachment: 'fixed',
      });
}

document.addEventListener("DOMContentLoaded", ()=>{
    vidimInit()
})
</script>