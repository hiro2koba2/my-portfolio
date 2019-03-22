<template>
  <v-container class="my-2">
    <h1 class="text-xs-center">about this App</h1>

    <v-flex sm12>
      <v-card class="ma-4" slot-scope="{ hover }" :class="`elevation-${hover ? 12 : 2}`">
        <v-img src="https://cdn.vuetifyjs.com/images/cards/desert.jpg" aspect-ratio="2.75"></v-img>

        <v-chip disabled color="green">Vue.js</v-chip>
        <v-chip disabled color="orange">Laravel</v-chip>

        <v-card-title primary-title>
          <div>
            <h3 class="headline">Kangaroo Valley Safari</h3>
          </div>
        </v-card-title>

        <v-card-actions>
          <v-btn flat color="orange" v-bind:href="work.url" target="_blank" rel="noopener noreferrer">URL</v-btn>
          <v-btn flat color="orange">Github</v-btn>
        </v-card-actions>

        <!-- 戻るボタン -->

      </v-card>
    </v-flex>
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
