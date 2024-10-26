<script setup>
  function showNavbarMenu(){
    $('#navbarMenu').slideToggle()
    document.getElementById('navbarMenuIcon').classList.toggle('rotate-[-90deg]')
  }
</script>

<template>
  <div id="nav-container" class="h-[6vh] text-black flex justify-center mx-auto w-max">
    <div id="navbar" class="z-50 fixed w-screen py-[1.2vh] px-[1vh] text-white bg-gradient-to-t from-zinc-900/70 to-zinc-950/70 drop-shadow-xl backdrop-blur-2xl">
      <button id="showMenuButton" v-on:click="showNavbarMenu" class="text-zinc-400 hover:text-white mx-[1vh]"><i id="navbarMenuIcon" class="rotate-[-90deg] duration-500 text-[2vh] fa-solid fa-chevron-down"></i></button>
      <div id="navbarMenu" class="ml-[2vh] mt-[1.5vh] py-[0.5vh] lg:hidden hidden">
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="/" class="dm-sans drop-shadow-sm hover:drop-shadow-md text-[2.5vh] text-zinc-400 hover:text-zinc-50 duration-300">Introduction</RouterLink></div>
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="/projects" class="dm-sans drop-shadow-sm hover:drop-shadow-md text-[2.5vh] text-zinc-400 hover:text-zinc-50 duration-300">Projects</RouterLink></div>
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="/informations" class="dm-sans drop-shadow-sm hover:drop-shadow-md text-[2.5vh] text-zinc-400 hover:text-zinc-50 duration-300">Integrating AI</RouterLink></div>
      </div>
    </div>
  </div>
</template>
