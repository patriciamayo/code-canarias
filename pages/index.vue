<template>
  <div class="container">
    <h1 style="color: rgb(0, 245, 233); font-size: 56px">
      ¿Necesitas
      <vue-typer
        :text="[
          'una app para iOS?',
          'una app para Android?',
          'una app híbrida?',
          'una web?',
          'una tienda online?',
          'un desarrollador fullstack?',
          'mejorar tu ciberseguridad?',
          'un videojuego?',
          'un experto en AI?',
          'organizar tu base de datos?',
          'administrar tu servidor?',
          'migrar a microservicios?',
          'testear tu software?',
          'analizar tus redes?',
          'programar dispositivos IoT?',
          'analizar tu BigData?',
        ]"
        :repeat="Infinity"
        :shuffle="true"
        initial-action="typing"
        :pre-type-delay="70"
        :type-delay="70"
        :pre-erase-delay="2000"
        :erase-delay="250"
        erase-style="select-all"
        :erase-on-complete="false"
        caret-animation="blink"
      ></vue-typer>
    </h1>
    <h2 style="color: white; padding-bottom: 32px; font-size: 56px">
      ¡Piensa en el talento Canario!
    </h2>
    <CodersList :coders="coders" />
  </div>
</template>

<script>
import CodersList from '~/components/CodersList.vue'

export default {
  components: {
    CodersList,
  },
  async asyncData({ app }) {
    const coders = await app.$content('coders').fetch()

    return {
      coders,
    }
  },
}
</script>

<style>
.container {
  max-width: 1100px;
  margin: auto;
  padding: 128px 32px;
}

.vue-typer .custom.char.typed {
  color: white;
}

.vue-typer .custom.char.selected {
  background-color: #00f5e9;
}

.vue-typer .custom.caret {
  width: 10px;
  background-color: #00f5e9;
}
</style>
