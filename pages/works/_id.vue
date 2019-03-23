<template>
  <v-container class="my-2">
    <h1 class="text-xs-center">about this App</h1>
        <v-card class="ma-4">
          <v-img src="https://cdn.vuetifyjs.com/images/cards/desert.jpg" aspect-ratio="1/2"></v-img>

          <v-card-title primary-title>
            <div>
              <h3 class="headline">{{ work.title }}</h3>
            </div>
          </v-card-title>

          <v-chip disabled color="green">Vue.js</v-chip>
          <v-chip disabled color="orange">Laravel</v-chip>

          <v-card-actions>
            <v-btn flat color="orange" v-bind:href="work.url" target="_blank" rel="noopener noreferrer">URL</v-btn>
            <v-btn flat color="orange">Github</v-btn>
          </v-card-actions>

          <!-- 戻るボタン -->
          <NuxtLink to="/">
            Back home
          </NuxtLink>
        </v-card>
  </v-container>
</template>

<script>
import Works from '~/components/MyWorks.vue'
export default {
  data(){
    return {
      work: Works[this.$route.params.id],
    }
  }
}
</script>
