<template>
  <vs-card>
    <template #title>
      <h3>{{ coder.name }}</h3>
    </template>
    <template #img>
      <img src="/foto5.png" alt="" />
    </template>
    <template #text>
      <p>{{ coder.bio }}</p>
    </template>
    <template #interactions>
      <vs-button danger icon>
        <i class="bx bx-heart"></i>
      </vs-button>
      <vs-button v-if="coder.github" danger icon :href="coder.github" blank>
        <i class="bx bxl-github"></i>
      </vs-button>
    </template>
  </vs-card>
</template>

<script>
export default {
  props: {
    coder: {
      type: Object,
      required: true,
    },
  },
}
</script>
