<script setup>
  // It's important to notice that without TailwindCSS the navbar wont work.
  // In order for the navbar to work you'll need to create your own classes and change the function's instructions.

  // This function is only used to show and hide navbar's menu for mobile/ipad users.
  // Just ignore it, or at least keep the code clear, you wont need to change it.
  function showNavbarMenu(){
    // Searchs for #navbarMenu and then toggles the .hidden class.
    document.getElementById('navbarMenu').classList.toggle('hidden')
    // Searchs for #navbarMenuIcon and then toggles .rotate-[-90deg] class.
    document.getElementById('navbarMenuIcon').classList.toggle('rotate-[-90deg]')
  }

  // This function only switches from fixed to relative.
  // Fixed => locked to the top of the page (over everything).
  // Relative => unlocked, just like every other element of the page.
  function unlockNavbar(){
    // Searchs for #navbar and then toggles the .fixed class.
    document.getElementById('navbar').classList.toggle('fixed')
  }
</script>

<template>
  <!-- 
    The navigation bar is fixed on the screen. When you scroll it will just stay still. 
    Just delete the #fixed class to make it relative, or use the unlockNavbar() function to remove and add it.
  -->
  <div id="nav-container" class="text-black flex justify-center mx-auto w-max">
    <div id="navbar" class="fixed w-screen py-[1.5vh] px-[1vh] text-black bg-gradient-to-r from-zinc-200/40 to-zinc-300/40 drop-shadow-2xl backdrop-blur">

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
          <RouterLink to="homepage" class="drop-shadow-lg mx-[1vh] text-[2.5vh] text-zinc-600/75 hover:text-zinc-950 duration-300">Homepage</RouterLink>
          <RouterLink to="services" class="drop-shadow-lg mx-[1vh] text-[2.5vh] text-zinc-600/75 hover:text-zinc-950 duration-300">Services</RouterLink>
          <RouterLink to="informations" class="drop-shadow-lg mx-[1vh] text-[2.5vh] text-zinc-600/75 hover:text-zinc-950 duration-300">Informations</RouterLink>
        </div>
      </div>

      <!-- This is the actual content of the hidden menu. -->
      <!-- 
        Large screen => display: none;
        Mobile/iPad screen => display: none; 
        (because you need to click the button)
      -->
      <div id="navbarMenu" class="ml-[2vh] mt-[1.5vh] py-[0.5vh] lg:hidden hidden">
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="homepage" class="drop-shadow-lg text-[2.5vh] text-zinc-600/75 hover:text-zinc-950 duration-300">Homepage</RouterLink></div>
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="services" class="drop-shadow-lg text-[2.5vh] text-zinc-600/75 hover:text-zinc-950 duration-300">Services</RouterLink></div>
        <div class="mx-[1vh] my-[1vh]"><RouterLink to="informations" class="drop-shadow-lg text-[2.5vh] text-zinc-600/75 hover:text-zinc-950 duration-300">Informations</RouterLink></div>
      </div>

    </div>
  </div>

</template>
