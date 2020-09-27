<template>
  <vs-navbar
    v-model="active"
    target-scroll="#padding-scroll-content"
    padding-scroll
    center-collapsed
  >
    <template #left>
      <img class="navbar-logo" src="/images/logo.png" alt="" />
    </template>
    <vs-navbar-item id="coders" to="/" :active="active == 'coders'">
      Coders
    </vs-navbar-item>
    <vs-navbar-item id="about" to="/about" :active="active == 'about'">
      ¿Quiénes somos?
    </vs-navbar-item>
    <template #right>
      <vs-button relief size="l">¿Te apuntas?</vs-button>
    </template>
  </vs-navbar>
</template>

<script>
export default {
  data: () => ({
    active: 'coders',
  }),
}
</script>

<style scoped>
.navbar-logo {
  width: 100%;
  max-width: 220px;
}
</style>
