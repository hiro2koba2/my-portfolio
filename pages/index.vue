<template>
  <div class="dashborad">
    <v-container class="my-2">
      <h1 class="text-xs-center grey--text">
        Works
      </h1>
      <v-layout row wrap>
        <v-flex v-for="(work,key) in works" :key="key" sm12 md6>
          <v-hover>
            <v-card slot-scope="{ hover }" class="ma-4" :class="`elevation-${hover ? 12 : 2}`">
              <v-img src="https://cdn.vuetifyjs.com/images/cards/desert.jpg" aspect-ratio="2.75" />

              <v-card-title primary-title>
                <div>
                  <h3 class="headline">
                    {{ work.title }}
                  </h3>
                </div>
              </v-card-title>

              <v-card-actions>
                <v-btn flat color="orange" href="https://www.google.com" target="_blank" rel="noopener noreferrer">
                  URL
                </v-btn>
                <v-btn flat color="orange" router :to="{ name: 'works-id', params: { id: key }}">
                  Learn More
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-hover>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import Works from '~/components/MyWorks.vue'
export default {
  data() {
    return {
      works: Works,
    }
  }
}
</script>
