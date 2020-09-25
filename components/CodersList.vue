<template>
  <div class="coders-list">
    <coder-card :coder="coders[0]" />
  </div>
</template>

<script>
import CoderCard from '~/components/CoderCard.vue'

export default {
  components: {
    CoderCard,
  },
  props: {
    coders: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style>
.coders-list {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
</style>
