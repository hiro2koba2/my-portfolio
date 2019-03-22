<template>

	<div class="dashborad">
		<v-container class="my-2">
			<h1 class="text-xs-center">My Products</h1>
			<v-layout row wrap>

				<v-flex sm12 md6>
					<v-hover>

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
									<v-btn flat color="orange" href="https://www.google.com" target="_blank" rel="noopener noreferrer">URL</v-btn>
									<v-btn flat color="orange">Github</v-btn>
								</v-card-actions>
							</v-card>

					</v-hover>
				</v-flex>

				<v-flex sm12 md6>
					<v-card class="ma-4">
						<v-img src="https://cdn.vuetifyjs.com/images/cards/desert.jpg" aspect-ratio="2.75"></v-img>

						<v-chip disabled>Example Chip</v-chip>

        		<v-card-title primary-title>
          		<div>
            		<h3 class="headline mb-0">Kangaroo Valley Safari</h3>
          		</div>
        		</v-card-title>

						<v-card-actions>
							<v-btn flat color="orange" href="https://www.google.com" target="_blank" rel="noopener noreferrer">URL</v-btn>
							<v-btn flat color="orange">Github</v-btn>
						</v-card-actions>
					</v-card>
				</v-flex>

				<v-flex sm12 md6>
					<v-card class="ma-4">
						<v-img src="https://cdn.vuetifyjs.com/images/cards/desert.jpg" aspect-ratio="2.75"></v-img>

						<v-chip disabled>Example Chip</v-chip>

        		<v-card-title primary-title>
          		<div>
            		<h3 class="headline mb-0">Kangaroo Valley Safari</h3>
          		</div>
        		</v-card-title>

						<v-card-actions>
							<v-btn flat color="orange" href="https://www.google.com" target="_blank" rel="noopener noreferrer">URL</v-btn>
							<v-btn flat color="orange">Github</v-btn>
						</v-card-actions>
					</v-card>
				</v-flex>

				<v-flex sm12 md6>
					<v-card class="ma-4">
						<v-img src="https://cdn.vuetifyjs.com/images/cards/desert.jpg" aspect-ratio="2.75"></v-img>

						<v-chip disabled>Example Chip</v-chip>
						<v-chip disabled>Example Chip</v-chip>

        		<v-card-title primary-title>
          		<div>
            		<h3 class="headline mb-0">Kangaroo Valley Safari</h3>
          		</div>
        		</v-card-title>

						<v-card-actions>
							<v-btn flat color="orange" href="https://www.google.com" target="_blank" rel="noopener noreferrer">URL</v-btn>
							<v-btn flat color="orange">Github</v-btn>
						</v-card-actions>
					</v-card>
				</v-flex>
			</v-layout>

			<!-- スクロール機能　一度保留 -->
			<!-- <v-btn fab dark bottom fixed right ref="button" color="primary" class="hidden-sm-and-up" @click="$vuetify.goTo('#top', scrollOpt)">
				<v-icon>keyboard_arrow_up</v-icon>
			</v-btn> -->

		</v-container>
	</div>
</template>

<script>
import Works from '~/components/MyWorks.vue'
export default {
	data() {
		return {
			// scrollOpt: {
      //   duration: 1500,
      //   offset: 10,
      //   easing: "easeInOutCubic"
			// },
			works: Works,
		}
	}
}
</script>
