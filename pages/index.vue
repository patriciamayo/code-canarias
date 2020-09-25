<template>
  <div class="container">
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
