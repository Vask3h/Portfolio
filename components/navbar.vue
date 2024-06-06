<template>
  <div
      class="fixed  w-screen z-40 flex flex-col bg-clip-border font-semibold gap-1 text-5xl  bg-gradient-to-r from-pink-500 via-red-500 to-yellow-500 pb-1">
    <div class="bg-gray-900">
      <nav class="border-red-200  bg-gray-900">
        <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
          <div class="cursor-default flex">
            <span class="self-center text-2xl italic font-semibold whitespace-nowrap text-white">Vaskeh.dev</span>
          </div>
          <div class=" w-full text-lg  md:block md:w-auto" id="navbar-default">
            <ul class="font-medium flex gap-7 space-x-8 ">
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
  </div>
</template>
<script setup lang="ts">
import NavbarContent from "~/components/generic/navbarContent.vue";
</script>