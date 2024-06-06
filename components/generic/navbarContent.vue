<template>
  <li>
    <nuxt-link
        class="block cursor-pointer text-white transition ease-out duration-700 hover:bg-clip-text hover:text-transparent hover:bg-gradient-to-r hover:from-pink-500 hover:via-red-500 hover:to-yellow-500 "
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