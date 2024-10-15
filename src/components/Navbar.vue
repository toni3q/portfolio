<script setup>
  function showNavbarMenu(){
    $('#navbarMenu').slideToggle()
    document.getElementById('navbarMenuIcon').classList.toggle('rotate-[-90deg]')
  }
</script>

<template>
  <div id="nav-container" class="h-[6vh] text-black flex justify-center mx-auto w-max">
    <div id="navbar" class="z-50 fixed w-screen py-[1.5vh] px-[1vh] text-black bg-gradient-to-r from-white/80 to-white/80 drop-shadow-2xl backdrop-blur-lg">
      <button id="showMenuButton" v-on:click="showNavbarMenu" class="mx-[1vh]"><i id="navbarMenuIcon" class="rotate-[-90deg] duration-300 text-[2vh] fa-solid fa-chevron-down"></i></button>
      <div id="navbarMenu" class="ml-[2vh] mt-[1.5vh] py-[0.5vh] lg:hidden hidden">
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="/" class="drop-shadow-sm hover:drop-shadow-md text-[2.5vh] text-zinc-600 hover:text-zinc-950 duration-300">Homepage</RouterLink></div>
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="/services" class="drop-shadow-sm hover:drop-shadow-md text-[2.5vh] text-zinc-600 hover:text-zinc-950 duration-300">Services</RouterLink></div>
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="/informations" class="drop-shadow-sm hover:drop-shadow-md text-[2.5vh] text-zinc-600 hover:text-zinc-950 duration-300">Informations</RouterLink></div>
      </div>
    </div>
  </div>
</template>
