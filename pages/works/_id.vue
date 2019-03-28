<template>
  <v-container class="my-2">
    <h1 class="text-xs-center grey--text">
      about this App
    </h1>

    <v-card class="ma-4">
      <v-img :src="work.img" aspect-ratio="1.4" />
      <!-- <img :src="work.img" alt=""> -->
      <v-card-title primary-title>
        <div>
          <h3 class="headline">
            {{ work.title }}
          </h3>
        </div>
      </v-card-title>

      <v-chip v-for="tag in work.tags" :key="tag.id" disabled color="blue white--text">
        {{ tag }}
      </v-chip>

      <v-card-text>
        {{ work.body }}
      </v-card-text>

      <v-card-actions>
        <v-btn flat color="orange" :href="work.url" target="_blank" rel="noopener noreferrer">
          URL
        </v-btn>
        <v-btn flat color="orange">
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
