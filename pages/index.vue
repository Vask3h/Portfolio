<template>

  <presentation/>
  <div class="w-1 h-[500px]">

  </div>
  <generic-foot/>

</template>
<script>
import {defineComponent} from "vue";
import Presentation from "~/components/presentation.vue";

export default defineComponent({
  components: {Presentation}
})
</script>
