<template>
    <div>
      <header class="flex items-center justify-between p-4 bg-gray-800 text-white">
      <div class="text-lg font-bold text-purple-300">Logo</div>
      <button class="md:hidden" @click="toggleMenu">
        <span v-show="hideHamburgerMenu" class="hamburger-icon text-purple-300 font-2xl">☰</span>
      </button>
      <nav :class="{'hidden': !isMenuOpen, 'block': isMenuOpen}" class="md:flex md:items-center">
        <ul class="flex flex-col md:flex-row">
          <li class="p-2"><NuxtLink href="/">Home</NuxtLink></li>
          <li class="p-2"><NuxtLink href="/about">About</NuxtLink></li>
          <li class="p-2"><NuxtLink href="/contact">Contact</NuxtLink></li>
        </ul>
      </nav>
    </header>
    </div>
  </template>
  <script>


  export default {
    data() {
      return {
        isMenuOpen: false,
        hideHamburgerMenu: true,
      };
    },
    methods: {
      toggleMenu() {
        this.isMenuOpen = !this.isMenuOpen;
        this.hideHamburgerMenu= !this.hideHamburgerMenu
      },
    },
  };
  </script>
  
  <style>
  .hamburger-icon {
    font-size: 1.5rem;
  }
  </style>
  
  
  