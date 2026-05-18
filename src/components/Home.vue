<script setup>
import { onMounted } from 'vue';
import gsap from 'gsap';
onMounted(()=>{
    const tl = gsap.timeline()
tl.from(".hero",{
  scale:1.2,duration:1.5,ease:"sine",opacity:0,
},"-=0.8")
.from(".card",{
    y:100,opacity:0,stagger:0.3,duration:1,ease:'power3.inOut'
},"-=1")
})

</script>
<template>
    <div class="w-full h-screen">
<img src="https://i1-e.pinimg.com/webp85/1200x/fb/37/42/fb3742598694224cd9eff596195b6a57.webp" class="hero object-cover w-full h-screen" alt="">
    </div>
    <div class="p-20 grid grid-cols-3 gap-5">
        <div class="card border border-gray-400/30 rounded-3xl p-12">
            <p class=" capitalize text-lg ">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quisquam modi deleniti repellat, mollitia quod eos. Voluptate cumque saepe excepturi quasi. Maiores nesciunt tenetur error animi deserunt, repellendus suscipit cum possimus quas minima. Recusandae ratione consequuntur ab, sed sunt molestias alias? Molestias, necessitatibus id? Magni, quos.</p>
        </div>
         <div class="card border border-gray-400/30 rounded-3xl p-12">
            <p class=" capitalize text-lg ">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quisquam modi deleniti repellat, mollitia quod eos. Voluptate cumque saepe excepturi quasi. Maiores nesciunt tenetur error animi deserunt, repellendus suscipit cum possimus quas minima. Recusandae ratione consequuntur ab, sed sunt molestias alias? Molestias, necessitatibus id? Magni, quos.</p>
        </div>
         <div class="card border border-gray-400/30 rounded-3xl p-12">
            <p class=" capitalize text-lg ">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quisquam modi deleniti repellat, mollitia quod eos. Voluptate cumque saepe excepturi quasi. Maiores nesciunt tenetur error animi deserunt, repellendus suscipit cum possimus quas minima. Recusandae ratione consequuntur ab, sed sunt molestias alias? Molestias, necessitatibus id? Magni, quos.</p>
        </div>
    </div>
</template>
<style scoped></style>