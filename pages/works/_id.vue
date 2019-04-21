<template>
  <v-container class="my-2">
    <h1 class="text-xs-center grey--text">
      {{ work.title }}
    </h1>

    <v-card class="ma-4">
      <v-img :src="work.img" aspect-ratio="2" />
      <!-- <v-card-title primary-title>
        <div>
          <h3 class="headline">
            {{ work.title }}
          </h3>
        </div>
      </v-card-title> -->

      <v-chip v-for="tag in work.tags" :key="tag.id" disabled color="blue white--text ma-2">
        {{ tag }}
      </v-chip>

      <v-card-text>
        {{ work.body }}
      </v-card-text>

      <v-card-actions>
        <v-btn flat color="orange" :href="work.url" target="_blank" rel="noopener noreferrer">
          URL
        </v-btn>
        <v-btn flat color="orange" :href="work.github" target="_blank" rel="noopener noreferrer">
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
