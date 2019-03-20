<template>
	<v-app>
		<nav>
			<v-toolbar flat app>
				<v-toolbar-title app class="display-1 ma-3">
					Portfolio
				</v-toolbar-title>
				<v-toolbar-items class="hidden-sm-and-down">
					<v-btn flat class="ml-4"><i class="fas fa-code fa-2x mr-2"></i>Works</v-btn>
					<v-btn flat class="ml-4"><i class="fas fa-user fa-2x mr-2"></i>About</v-btn>
					<v-btn flat class="ml-4"><i class="fas fa-envelope fa-2x mr-2"></i>Contact</v-btn>
				</v-toolbar-items>
				<v-spacer></v-spacer>
				<v-toolbar-side-icon class="hidden-md-and-up mr-3"></v-toolbar-side-icon>
			</v-toolbar>

			<!-- <v-navigation-drawer app v-model="drawer" class="primary hidden-md-and-up" >
				<v-list>
					<v-list-title>
						<v-list-tile-action>
							<v-icon class="white--text">dashboard</v-icon>
						</v-list-tile-action>
						<v-list-tile-content>
							<v-list-tile-title class="white--text">Dashboard</v-list-tile-title>
						</v-list-tile-content>
					</v-list-title>
				</v-list>
			</v-navigation-drawer> -->
		</nav>
		<v-content id="top">
			<v-container>
				<nuxt/>
			</v-container>
		</v-content>
	</v-app>
</template>

<script>
export default {
	data() {
		return {
			scrollOpt: {
        duration: 1500,
        offset: 10,
        easing: "easeInOutCubic"
      }
			// drawer: true
		}
	}
}
</script>
