<template>
  <v-container class="my-2">
    <h1 class="text-xs-center grey--text">
      {{ work.title }}
    </h1>

    <v-card class="ma-4">
      <v-img :src="work.img" aspect-ratio="2.15" />

      <v-card-text class="my-3">
        {{ work.body }}
      </v-card-text>

      <v-card-actions>
        <v-spacer />
        <v-btn flat color="orange" :href="work.url" target="_blank">
          URL
        </v-btn>
        <v-btn flat color="orange" :href="work.github" target="_blank">
          Github
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
</template>

<script>
import Works from '~/components/MyWorks.vue'
export default {
  data() {
    return {
      work: Works[this.$route.params.id],
    }
  }
}
</script>
