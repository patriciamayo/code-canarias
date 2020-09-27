<template>
  <vs-card>
    <template #title>
      <h3>{{ coder.name }}</h3>
    </template>
    <template #img>
      <img :src="coder.image" :alt="`Foto de ${coder.name}`" />
    </template>
    <template #text>
      <p class="bio">{{ coder.bio }}</p>
      <div>
        <vs-button
          v-for="(skill, index) of coder.skills.slice(0, maxSkills)"
          :key="index"
          class="tag"
          success
          flat
        >
          {{ skill }}
        </vs-button>
      </div>
    </template>
    <template #interactions>
      <vs-button v-if="coder.github" primary icon :href="coder.github" blank>
        <i class="bx bxl-github"></i>
      </vs-button>
      <vs-button v-if="coder.twitter" primary icon :href="coder.twitter" blank>
        <i class="bx bxl-twitter"></i>
      </vs-button>
      <vs-button v-if="coder.website" primary icon :href="coder.website" blank>
        <i class="bx bx-globe"></i>
      </vs-button>
      <vs-button
        v-if="coder.linkedin"
        primary
        icon
        :href="coder.linkedin"
        blank
      >
        <i class="bx bxl-linkedin"></i>
      </vs-button>
      <vs-button
        v-if="coder.github"
        primary
        icon
        :href="`mailto:${coder.github}`"
        blank
      >
        <i class="bx bx-envelope"></i>
      </vs-button>
    </template>
  </vs-card>
</template>

<script>
import { MAX_SKILLS } from '~/constants'

export default {
  props: {
    coder: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      maxSkills: MAX_SKILLS,
    }
  },
}
</script>

<style scoped>
.tag {
  display: inline-block;
  margin-left: 0;
}

.bio {
  margin-bottom: 16px;
}
</style>
