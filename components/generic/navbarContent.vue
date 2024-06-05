<template>
  <li>
    <nuxt-link
        class="block cursor-pointer py-2 px-3 rounded md:border-0  md:p-0 text-white md:hover:text-yellow-500 hover:bg-gray-700 hover:text-white md:hover:bg-transparent"
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