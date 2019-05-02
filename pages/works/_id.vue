<template>
  <v-container fluid>
    <v-layout row wrap>
      <v-flex xs12 class="text-xs-center grey--text" mt-3>
        <h1>{{ work.title }}</h1>
      </v-flex>
      <v-flex xs12 sm6 offset-sm3 mt-3>
        <p class="subheading text-xs-center">
          {{ work.body }}
        </p>
      </v-flex>

      <v-flex xs12 sm6 offset-sm3 mt-3>
        <v-img :src="work.img" aspect-ratio="2.15" />
      </v-flex>

      <v-flex xs12 sm6 offset-sm3 class="text-xs-center" mt-5>
        <v-btn outline color="orange" :href="work.url" target="_blank">
          URL
        </v-btn>
        <v-btn outline color="orange" :href="work.github" target="_blank">
          Github
        </v-btn>
      </v-flex>
    </v-layout>
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
