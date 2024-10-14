<script setup>
  function showNavbarMenu(){
    document.getElementById('navbarMenu').classList.toggle('hidden')
    document.getElementById('navbarMenuIcon').classList.toggle('rotate-[-90deg]')
  }
</script>

<template>

  <div id="navbar" class="text-black flex justify-center mx-auto w-max">
    <div class="fixed w-full py-[1.5vh] px-[1vh] text-black bg-gradient-to-r from-zinc-100/25 to-zinc-200/25 backdrop-blur">
      
      <!-- Click to start showNavbarMenu() in order to show the hidden menu. -->
      <button id="showMenuButton" v-on:click="showNavbarMenu" class="mx-[1vh]"><i id="navbarMenuIcon" class="rotate-[-90deg] duration-300 text-[3vh] fa-solid fa-chevron-down"></i></button>
      
      <!-- This is the actual content of the hidden menu. -->
      <div id="navbarMenu" class="ml-[2vh] mt-[1.5vh] py-[0.5vh] hidden">
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="" class="drop-shadow-lg text-[2.5vh] hover:text-sky-500 duration-300">Homepage</RouterLink></div>
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="" class="drop-shadow-lg text-[2.5vh] hover:text-sky-500 duration-300">Services</RouterLink></div>
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="" class="drop-shadow-lg text-[2.5vh] hover:text-sky-500 duration-300">Informations</RouterLink></div>
      </div>
      
    </div>
  </div>  

  <RouterView />
</template>
