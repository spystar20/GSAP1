<script setup>
import { onMounted } from 'vue';
import gsap from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger)
onMounted(()=>{
    const tl = gsap.timeline()
    const cardSection = document.querySelector('.cards-wrapper')
    const ScrollWidth = cardSection.scrollWidth - window.innerWidth
tl.from(".hero",{
  scale:1.2,duration:1.5,ease:"sine",opacity:0, scrollTrigger:{
    start:'top top',end:'+=100%',trigger:'.hero',scrub:true
  }
})

,gsap.from(".card",{
    y:100,opacity:0,stagger:0.3,duration:1,ease:'power3.inOut',scrollTrigger:{
        start:'top 80%',
        toggleActions:'play none none reverse',
        trigger:'.card',
        markers: true,
        
 }
}
),
gsap.to(cardSection,{
    x:-ScrollWidth,opacity:1,scrollTrigger:{
        trigger:'.horizontal-section',pin:true,scrub:true,start:'top top',end:`+=${ScrollWidth}`
    }
}),
gsap.from('.title',{
    yPercent:100,duration:3, ease:'power3.inOut',scrollTrigger:{trigger:'.title',start:'top 80%',markers :true
    }
})
},
 

)

</script>
<template>
    
    <div class="w-full h-screen">
<img src="https://i1-e.pinimg.com/webp85/1200x/fb/37/42/fb3742598694224cd9eff596195b6a57.webp" class="hero object-cover w-full h-screen" alt="">
    </div>
   <div class="overflow-hidden py-6">
    <h2 class="title text-4xl font-semibold text-center" >
        PORTFOLIO
    </h2>
    </div>
<div class="horizontal-section h-screen overflow-hidden">
    <div class="cards-wrapper flex w-max gap-5 p-20 ">
        
            <img class="card w-[500px] h-[400px]  border border-gray-400/30 rounded-3xl p-3" src="https://i1-e.pinimg.com/webp85/1200x/fb/37/42/fb3742598694224cd9eff596195b6a57.webp" alt="">
       
          <img class="card w-[500px] h-[400px]  border border-gray-400/30 rounded-3xl p-3" src="https://i1-e.pinimg.com/webp85/1200x/fb/37/42/fb3742598694224cd9eff596195b6a57.webp" alt="">
         <img class="card w-[500px] h-[400px]  border border-gray-400/30 rounded-3xl p-3" src="https://i1-e.pinimg.com/webp85/1200x/fb/37/42/fb3742598694224cd9eff596195b6a57.webp" alt="">
            <img class="card w-[500px] h-[400px]  border border-gray-400/30 rounded-3xl p-3" src="https://i1-e.pinimg.com/webp85/1200x/fb/37/42/fb3742598694224cd9eff596195b6a57.webp" alt="">   <img class="card w-[500px] h-[400px]  border border-gray-400/30 rounded-3xl p-3" src="https://i1-e.pinimg.com/webp85/1200x/fb/37/42/fb3742598694224cd9eff596195b6a57.webp" alt="">   <img class="card w-[500px] h-[400px]  border border-gray-400/30 rounded-3xl p-3" src="https://i1-e.pinimg.com/webp85/1200x/fb/37/42/fb3742598694224cd9eff596195b6a57.webp" alt="">
        </div>
    </div>

  
</template>
<style scoped></style>