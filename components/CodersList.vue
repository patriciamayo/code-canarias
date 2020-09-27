<template>
  <div class="coders-list">
    <coder-card v-for="(coder, index) of coders" :key="index" :coder="coder" />
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
  grid-gap: 32px;
  justify-items: center;
}

@media (max-width: 850px) {
  .coders-list {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 560px) {
  .coders-list {
    grid-template-columns: 1fr;
  }
}
</style>
