<template>
    <div class="w-full px-6">
        <div class="flex flex-col md:flex-row pb-16">

            <div class="w-full md:w-[37.5%] flex flex-col items-left justify-center">
                <div class="text-6xl">GET IN TOUCH</div>
                <div class="py-5">
                    <input type="text" placeholder="email"
                        class="bg-black border-b-white border-b-2 outline-none w-full md:w-[80%]">
                </div>
                <div
                    class="send-email-button w-full md:w-[80%] bg-white text-black text-3xl font-black text-center py-11 cursor-pointer hover:lowercase transition-all ease-in-out duration-500">
                    SEND</div>

                    <div class="r font-bold py-3">n3rd 2022</div>
            </div>
            <div class="w-full md:w-[37.5%] flex flex-col items-start md:items-center justify-center">
                <div class="social-links text-3xl font-semibold list-none">
                   <div class="flex flex-row">
                    <div class="cursor-pointer">INSTAGRAM</div>
                    <div><svg width="32" height="32" viewBox="0 0 24 24"><path fill="#ffffff" d="M18 7.05a1 1 0 0 0-1-1L9 6a1 1 0 0 0 0 2h5.56l-8.27 8.29a1 1 0 0 0 0 1.42a1 1 0 0 0 1.42 0L16 9.42V15a1 1 0 0 0 1 1a1 1 0 0 0 1-1Z"/></svg></div>
                   </div>

                   <div class="flex flex-row">
                    <div class="cursor-pointer">TWITTER</div>
                    <div><svg width="32" height="32" viewBox="0 0 24 24"><path fill="#ffffff" d="M18 7.05a1 1 0 0 0-1-1L9 6a1 1 0 0 0 0 2h5.56l-8.27 8.29a1 1 0 0 0 0 1.42a1 1 0 0 0 1.42 0L16 9.42V15a1 1 0 0 0 1 1a1 1 0 0 0 1-1Z"/></svg></div>
                   </div>

                   <div class="flex flex-row">
                    <div class="cursor-pointer">REDDIT</div>
                    <div><svg width="32" height="32" viewBox="0 0 24 24"><path fill="#ffffff" d="M18 7.05a1 1 0 0 0-1-1L9 6a1 1 0 0 0 0 2h5.56l-8.27 8.29a1 1 0 0 0 0 1.42a1 1 0 0 0 1.42 0L16 9.42V15a1 1 0 0 0 1 1a1 1 0 0 0 1-1Z"/></svg></div>
                   </div>

                </div>
            </div>
            <div class="footer-vid-container w-3/12 hidden md:flex justify-center items-center">
                <div class="footer-vid w-[26rem] h-[24rem]" id="footervid"></div>
            </div>
        </div>
    </div>
</template>
<script>
import vidim from 'vidim';

const vidimInit = () => {
    var myBackground = new vidim('#footervid', {
        src: [
            {
                type: 'video/webm',
                src: '/vid/pexels-koolshooters-6908517.webm'
            },

        ],
        backgroundSize: 'cover',
        backgroundPosition: 'center',
        backgroundAttachment: 'fixed',
    });
}

document.addEventListener("DOMContentLoaded", () => {
    vidimInit()
})
</script>