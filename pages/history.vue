<template>
  <v-container grid-list-md text-xs-center>
    <v-layout row wrap>
      <v-flex v-for="i in 3" :key="`4${i}`" xs4>
        <v-hover>
          <v-card slot-scope="{ hover }" :class="`elevation-${hover ? 12 : 2}`" class="mx-auto" width="344">
            <v-img
              src="https://cdn.vuetifyjs.com/images/cards/desert.jpg"
              aspect-ratio="2.75"
            />

            <v-card-title primary-title>
              <div>
                <h3 class="headline mb-0">
                  Kangaroo Valley Safari
                </h3>
                <div> {{ card_text }} </div>
              </div>
            </v-card-title>

            <v-card-actions>
              <v-btn flat color="orange">
                Share
              </v-btn>
              <v-btn flat color="orange">
                Explore
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-hover>
      </v-flex>
      <v-flex v-for="i in 3" :key="`4${i}`" xs4>
        <v-hover>
          <v-card slot-scope="{ hover }" :class="`elevation-${hover ? 12 : 2}`" class="mx-auto" width="344">
            <v-img :aspect-ratio="16/9" src="https://cdn.vuetifyjs.com/images/cards/cooking.png" />
            <v-card-title>
              <div>
                <span class="headline">Cafe Badilico</span>
                <div class="d-flex">
                  <v-rating
                    :value="value"
                    color="amber"
                    dense
                    half-increments
                    readonly
                    size="14"
                  />
                  <div class="ml-2 grey--text text--darken-2">
                    <span>{{ value }}</span>
                    <span>({{ reviews }})</span>
                  </div>
                </div>
              </div>
              <v-spacer />
              <v-btn icon class="mr-0">
                <v-icon>mdi-chevron-right</v-icon>
              </v-btn>
            </v-card-title>
          </v-card>
        </v-hover>
      </v-flex>
    </v-layout>
  </v-container>
</template>
