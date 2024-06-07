<template>
  <li>
    <a
        class="cursor-pointer text-white ease-in duration-300 bg-clip-text hover:text-transparent hover:bg-gradient-to-r from-pink-500 via-red-500 to-yellow-500 "
        :href=link
    >
      {{ text }}
    </a>
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
      default: ""
    }
  }
}
</script>