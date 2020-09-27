<template>
  <div class="container">
    <h1 style="color: white; font-size: 56px">
      <span style="color: rgb(0, 245, 233)">¿Necesitas una mano?</span>
      piensa en el talento Canario!
    </h1>
    <h2 style="color: white; padding: 32px 0; font-size: 48px"></h2>
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

<style scoped>
.container {
  max-width: 1100px;
  margin: auto;
  padding: 128px 32px;
}
</style>
