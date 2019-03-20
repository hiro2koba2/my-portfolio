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
        <v-list-tile>
					<v-list-tile-action>
						<i class="fas fa-code fa-1x ma-2"></i>
          </v-list-tile-action>
          <v-list-tile-content>
            Works
          </v-list-tile-content>
        </v-list-tile>

				<v-list-tile>
					<v-list-tile-action>
						<i class="fas fa-user fa-1x ma-2"></i>
          </v-list-tile-action>
          <v-list-tile-content>
            About
          </v-list-tile-content>
				</v-list-tile>

				<v-list-tile>
					<v-list-tile-action>
						<i class="fas fa-envelope fa-1x ma-2"></i>
          </v-list-tile-action>
          <v-list-tile-content>
            Contact
          </v-list-tile-content>
				</v-list-tile>
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
      title: 'Vuetify.js',
			items: [
        {
          icon: "apps",
          title: "Top",
          to: "/"
        },
        {
          icon: "person",
          title: "About",
          to: "/about"
        },
        {
          icon: "history",
          title: "History",
          to: "/history"
				}
			]
		}
	}
}
</script>
