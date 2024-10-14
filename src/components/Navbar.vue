<script setup>
  function showNavbarMenu(){
    document.getElementById('navbarMenu').classList.toggle('hidden')
    document.getElementById('navbarMenuIcon').classList.toggle('rotate-[-90deg]')
  }
</script>

<template>
  <div id="navbar" class="text-black flex justify-center mx-auto w-max">
    <div class="fixed w-full py-[1.5vh] px-[1vh] text-black bg-gradient-to-r from-zinc-100/25 to-zinc-200/25 drop-shadow-2xl backdrop-blur">

      <!-- Click #showMenuButton to start showNavbarMenu() in order to show the hidden menu. -->
      <div class="flex">
        <!-- 
          Large screen => display: none; 
          Mobile/iPad screen => display: block;
        -->
        <button id="showMenuButton" v-on:click="showNavbarMenu" class="mx-[1vh] lg:hidden block"><i id="navbarMenuIcon" class="rotate-[-90deg] duration-300 text-[3vh] fa-solid fa-chevron-down"></i></button>
        <!-- 
          Large screen => display: block; 
          Mobile/iPad screen => display: none;
        -->
        <div id="" class="flex hidden lg:block">
          <RouterLink to="homepage" class="drop-shadow-lg mx-[1vh] text-[2.5vh] hover:text-sky-500 duration-300">Homepage</RouterLink>
          <RouterLink to="services" class="drop-shadow-lg mx-[1vh] text-[2.5vh] hover:text-sky-500 duration-300">Services</RouterLink>
          <RouterLink to="informations" class="drop-shadow-lg mx-[1vh] text-[2.5vh] hover:text-sky-500 duration-300">Informations</RouterLink>
        </div>
      </div>

      <!-- This is the actual content of the hidden menu. -->
      <!-- 
        Large screen => display: none;
        Mobile/iPad screen => display: none; 
        (because you need to click the button)
      -->
      <div id="navbarMenu" class="ml-[2vh] mt-[1.5vh] py-[0.5vh] lg:hidden hidden">
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="homepage" class="drop-shadow-lg text-[2.5vh] hover:text-sky-500 duration-300">Homepage</RouterLink></div>
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="services" class="drop-shadow-lg text-[2.5vh] hover:text-sky-500 duration-300">Services</RouterLink></div>
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="informations" class="drop-shadow-lg text-[2.5vh] hover:text-sky-500 duration-300">Informations</RouterLink></div>
      </div>

    </div>
  </div>
</template>
