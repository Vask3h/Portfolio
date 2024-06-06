<template>
  <li>
    <nuxt-link
        class="cursor-pointer text-white ease-in duration-300 bg-clip-text hover:text-transparent hover:bg-gradient-to-r from-pink-500 via-red-500 to-yellow-500 "
        to=""
    >
      {{ text }}
    </nuxt-link>
  </li>
</template>
<script>
export default {
  name: 'navbarContent',
  props: {
    text: {
      type: String,
      default: "texto"
    },
    link: {
      type: String,
      default: "google.com"
    }
  }
}
</script>