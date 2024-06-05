<template>
  <div>
    <div :style="variableStyle"
         class="z-10 relative   items-center flex " id="myScreenContainer">
      <div class="absolute flex items-center justify-between min-w-full px-3 ">
        <button
            class=" relative rounded-full bg-white flex opacity-60 z-20 hover:opacity-100 "
            @click="goLeft()">
          <generic-icon
              name="chevronLeft"
              width="30"
          />
        </button>
        <button
            class=" relative rounded-full bg-white flex opacity-60 z-20 hover:opacity-100 "
            @click="goRight()">
          <generic-icon
              name="chevronRight"
              width="30"
          />
        </button>
      </div>
      <div class="flex overflow-hidden scroll-smooth gap-[10px]  " id="myScreen">
        <component :is="carouselComponents"
                   id="myComponent"
                   v-for="item in carrouselContent"
                   :key="item.carrouselContent"
                   :img="item.img"
                   :type="item.type"
                   :price="item.price"
        />
      </div>
    </div>
  </div> <!-- Boton de las pruebas -->
  <generic-button
      font-size="20"
      text="Testing 1"
      @click="testing()"
  />
</template>
<script>
import cardTaxi from "~/components/card/taxi.vue";
export default {
  name: "carrousel2",
  data: () => ({
    chooseContainer: "",
    containerWidth: "",
    chooseComponent: "", // Utilizado para sacar el ancho del componente. En uso.
    componentWidth: "",  // Ancho de cada componente.                     En uso.
    variableStyle: "",   // Estilo que se le dara al contenedor.          En uso.
    scrollDistance: "",   //
    totalComponents: "1",  // Numero de componentes que se van a mostrar
  }),
  mounted() {
    this.mountedFunction()
  },
  methods: {
    goLeft() {
      let element = document.getElementById("myScreen")
      element.scrollBy(-this.scrollDistance, 0,)
    },
    goRight() {
      let element = document.getElementById("myScreen")
      element.scrollBy(this.scrollDistance, 0)
    },
    testing() {
      console.log("Tamaño del cada componente infividualmente = " + this.componentWidth)
      console.log("Estilo que se asgina = " + this.variableStyle)
      console.log("Cuantos pixeles se scrolea = " + this.scrollDistance)
      console.log("prueba prop a var = " + this.totalComponents)
    },
    mountedFunction() {
      this.chooseContainer = document.getElementById("myScreenContainer")
      this.containerWidth = this.chooseContainer.offsetWidth
      this.totalComponents = this.propTotalComponents
      this.chooseComponent = document.getElementById('myComponent')
      this.componentWidth = this.chooseComponent.offsetWidth * this.totalComponents
      this.variableStyle = "max-width:" + this.componentWidth + "px"
      this.scrollDistance = this.componentWidth + 20
    },
  },
  props: {
    carrouselContent: {
      type: Array,
    },
    propTotalComponents: {
      type: Number,
      default: 2
    },
    carouselComponents: {
      type: Object,
      default: cardTaxi
    }
  }
}
</script>
