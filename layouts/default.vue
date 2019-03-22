<template>
	<v-app>
		<nav>
			<v-toolbar flat app>
				<v-toolbar-title class="display-1 ma-3">
					Portfolio
				</v-toolbar-title>

				<v-spacer></v-spacer>
				<v-toolbar-items class="hidden-sm-and-down" v-for="link in links" :key="link.text">
					<v-btn flat router :to="link.route"><v-icon>{{ link.icon }}</v-icon>{{link.text}}</v-btn>
				</v-toolbar-items>
				<v-toolbar-side-icon class="hidden-md-and-up mr-3" @click.stop="rightDrawer = !rightDrawer"></v-toolbar-side-icon>
			</v-toolbar>
		</nav>

		<v-content id="top">
			<v-container>
				<nuxt/>
			</v-container>
		</v-content>

		<v-navigation-drawer v-model="rightDrawer" :right="right" temporary app>
      <v-list>

				<v-list-tile v-for="link in links" :key="link.text" router :to="link.route">
					<v-list-tile-action>
						<v-icon>{{ link.icon }}</v-icon>
					</v-list-tile-action>
					<v-list-tile-content>
						<v-list-tile-title>
							{{ link.text }}
						</v-list-tile-title>
					</v-list-tile-content>
				</v-list-tile>

      </v-list>
    </v-navigation-drawer>

		<v-footer class="pa-4">
			<v-spacer></v-spacer>
			<span> &copy;2019 — roffet</span>
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
			links: [
				{ icon: 'code', text: 'Works', route: '/' },
				{ icon: 'person', text: 'About', route: '/about' },
				{ icon: 'mail', text: 'Contact', route: '/contact' },
			]
		}
	}
}
</script>
