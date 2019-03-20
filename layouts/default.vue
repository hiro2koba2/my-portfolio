<template>
	<v-app>
		<nav>
			<v-toolbar flat app>
				<v-toolbar-title app class="display-1 ma-3">
					Portfolio
				</v-toolbar-title>
				<v-toolbar-items class="hidden-sm-and-down">
					<router-link to="/" class="ma-3 decoration"><v-btn flat><i class="fas fa-code fa-2x mr-2"></i>Works</v-btn></router-link>
					<router-link to="about" class="ma-3 decoration"><v-btn flat><i class="fas fa-user fa-2x mr-2"></i>About</v-btn></router-link>
					<router-link to="history" class="ma-3 decoration"><v-btn flat><i class="fas fa-envelope fa-2x mr-2"></i>Contact</v-btn></router-link>
				</v-toolbar-items>
				<v-spacer></v-spacer>
				<v-toolbar-side-icon class="hidden-md-and-up mr-3" @click.stop="rightDrawer = !rightDrawer"></v-toolbar-side-icon>
			</v-toolbar>
		</nav>
		<v-content id="top">
			<v-container>
				<nuxt/>
			</v-container>
		</v-content>

		<v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>

				<router-link to="/">
					<v-list-tile>
						<v-list-tile-action>
							<i class="fas fa-code fa-1x ma-2"></i>
						</v-list-tile-action>
						<v-list-tile-content>
							Works
						</v-list-tile-content>
					</v-list-tile>
				</router-link>

				<router-link to="/about">
					<v-list-tile>
						<v-list-tile-action>
							<i class="fas fa-user fa-1x ma-2"></i>
						</v-list-tile-action>
						<v-list-tile-content>
							About
						</v-list-tile-content>
					</v-list-tile>
				</router-link>

				<router-link to="/history">
					<v-list-tile>
						<v-list-tile-action>
							<i class="fas fa-envelope fa-1x ma-2"></i>
						</v-list-tile-action>
						<v-list-tile-content>
							Contact
						</v-list-tile-content>
					</v-list-tile>
				</router-link>

      </v-list>
    </v-navigation-drawer>

		<v-footer :fixed="fixed" app>
      <span>&copy; 2019</span>
    </v-footer>
	</v-app>
</template>

<script>
export default {
	data() {
		return {
			miniVariant: false,
			right: true,
      rightDrawer: false,
		}
	}
}
</script>

<style>
  a {
    text-decoration: none;
  }
</style>
