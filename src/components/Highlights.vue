<template>
    <div class="section-3 w-full md:px-40 md:pb-10">
        <div class="section-title text-[4rem] md:text-[6rem] lg:text-[12rem] font-black text-center">HIGHLIGHTS</div>
<div class="flex flex-col md:flex-row">
    <div class="flex flex-col w-full h-[24rem] highlight-container items-center my-24 cursor-pointer" v-for="highlight in highlights" :key="highlight.name">
            <div class="highlight__inner w-[68%] h-full overflow-hidden">
                <div class="highlight__inner__image h-full w-full bg-center bg-cover hover:scale-[1.1] transition-transform duration-300" :style="{ backgroundImage: 'url(' + highlight.image + ')' }"></div>
            </div>
            <!-- <div class="highlight-desc font-black">Amari - Paris - 2019</div> -->
            <div class="highlight-desc font-black">{{highlight.name}} - {{highlight.location}} - {{highlight.year}}</div>
        </div>
</div>



    </div>
</template>

<script>
    export default{
        data(){
            return{
                highlights: [
                    {name: 'Amari', location: 'Paris', year: '2019', image: '/img/8.jpg'},
                    {name: 'Jamul', location: 'India', year: '2020', image: '/img/9.jpg'},
                    {name: 'Yaba', location: 'Lagos', year: '2021', image: '/img/10.jpg'},
                    {name: 'Lilia', location: 'Sofia', year: '2022', image: '/img/11.jpg'},
                ]
            }
        }
    }
</script>
