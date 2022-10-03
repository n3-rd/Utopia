<template>
    <div>
        <div class="section-3 w-full px-6 pb-10">
        <div class="section-title text-[12rem] font-black text-center">EVENTS</div>
        <div class="event-list">
          <div class="event-image w-[20rem] h-[23rem] absolute bg-[url('/img/1.jpg')] bg-center bg-cover hidden pointer-events-none select-none"></div>
          <div class="event-container ">
            <div class="marquee-event-container border-y-2 border-y-white" v-for="event in events" :key="event.name">
                <div class="marquee event uppercase event-image" :data-event-image="event.image">
              <!-- infinite marquee -->
              <div class="event__inner h-full marquee__content ">
                <div class="event__item text-[5rem] ">
                  {{event.name}}
                </div>
                <div class="event__item text-[5rem] ">
                  {{event.name}}
                </div>
                <div class="event__item text-[5rem] ">
                  {{event.name}}
                </div>
                <div class="event__item text-[5rem] ">
                  {{event.name}}
                </div>
            </div>

            <div class="event__inner h-full marquee__content" aria-hidden="true">
              <div class="event__item text-[5rem] ">
                {{event.name}}
              </div>
              <div class="event__item text-[5rem] ">
                {{event.name}}
              </div>
              <div class="event__item text-[5rem] ">
                {{event.name}}
              </div>
              <div class="event__item text-[5rem] ">
                {{event.name}}
              </div>
          </div>
          </div>
            </div>



          </div>

      </div>

      <!-- <div style="padding-bottom: 65.25%;" id="vid1"></div> -->
    </div>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                events: [
                    {name: "Paris", image: "img/2.jpg"},
                    {name: "Helsinki", image: "img/3.jpg"},
                    {name: "Lagos", image: "img/4.jpg"},
                    {name: "Miami", image: "img/6.jpg"},
                    {name: "Sydney", image: "img/7.jpg"},
                ]
            }
        },
        methods:{
            eventHoverImage(){
                // const eventImage = document.querySelector('.event-image');
                const eventItem = document.querySelectorAll('.event');

                eventItem.forEach((e)=>{
                    e.addEventListener("mouseover", (cursor)=>{
                      let eventImage = document.querySelector('.event-image')

                      let cursorX = cursor.clientX;
                      let cursorY = cursor.clientY;
                      console.log(cursorX + " " + cursorY);


      eventImage.style = `
      display:block;
    background: url(${e.dataset.eventImage});
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    transition: transform 0.2s linear;
    transform: translate(${cursorX}px, ${cursorY - 150}px);
      `
                    })
                })


                eventItem.forEach((e)=>{
                    e.addEventListener("mouseleave", ()=>{
                      let eventImage = document.querySelector('.event-image')

      eventImage.style = `
      display:none;
      `
                    })
                })
            }
        },
        mounted(){
            this.eventHoverImage()
        }
    }
</script>