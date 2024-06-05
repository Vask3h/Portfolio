<template>
  <div class="fixed w-screen z-40 border-b">
    <nav class="border-gray-200 bg-gray-900">
      <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
        <div class="cursor-default flex">
          <nuxt-img
              src="/vaskehLogo.png"
              width="30"
          />
          <span class="self-center text-2xl italic font-semibold whitespace-nowrap text-white">Vaskeh.dev</span>
        </div>
        <button data-collapse-toggle="navbar-default" type="button"
                class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm  rounded-lg md:hidden focus:outline-none focus:ring-2 text-gray-400 hover:bg-gray-700 focus:ring-gray-600"
                aria-controls="navbar-default" aria-expanded="false">
          <span class="sr-only">Open main menu</span>
          <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="M1 1h15M1 7h15M1 13h15"/>
          </svg>
        </button>
        <div class="hidden w-full text-lg  md:block md:w-auto" id="navbar-default">
          <ul class="font-medium flex flex-col gap-7 p-4 md:p-0 mt-4 border rounded-lg md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0 md:bg-white bg-gray-800 md:dark:bg-gray-900 border-gray-700">
            <navbar-content
                text="Inicio"
            />
            <navbar-content
                text="Habilidades"
            />
            <navbar-content
                text="Proyectos"
            />
            <navbar-content
                text="Contacto"
            />
          </ul>
        </div>
      </div>
    </nav>
  </div>


</template>
<script setup lang="ts">
import NavbarContent from "~/components/generic/navbarContent.vue";
</script>