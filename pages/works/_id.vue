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
        <v-carousel height="auto">
          <v-carousel-item v-for="(image, i) in work.img2" :key="i" :src="image">
            <!-- <v-img :src="image" /> -->
          </v-carousel-item>
        </v-carousel>
      </v-flex>

      <v-flex xs12 class="text-xs-center grey--text" mt-5>
        <h2>レスポンシブ対応</h2>
      </v-flex>

      <v-flex xs5 sm2 offset-sm3 mt-5>
        <v-img :src="work.img3" />
      </v-flex>

      <!-- offsetはもっと簡略化した形でも書けるが、なぜか効かなくなったので戻した -->
      <v-flex xs5 sm2 offset-xs2 offest-sm2 mt-5>
        <v-img :src="work.img4" />
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
