<template>
  <div class="dashborad">
    <v-container class="my-2">
      <h1 class="text-xs-center grey--text">
        Works
      </h1>
      <v-layout row wrap>
        <v-flex v-for="(work,key) in works" :key="key" xs12 sm12 md6>
          <v-hover>
            <v-card slot-scope="{ hover }" class="ma-4" :class="`elevation-${hover ? 12 : 2}`">
              <v-img :src="work.img" height="200" />
              <hr>

              <v-card-title primary-title>
                <div>
                  <h3 class="headline grey--text">
                    {{ work.title }}
                  </h3>
                </div>
              </v-card-title>

              <div class="text-xs-center">
                <v-chip
                  v-for="tag in work.tags"
                  :key="tag.id"
                  label
                  disabled
                  color="primary lighten-2 white--text"
                >
                  {{ tag }}
                </v-chip>
              </div>

              <v-card-actions>
                <v-spacer />
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
