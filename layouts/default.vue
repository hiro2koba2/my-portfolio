<template>
	<v-app>
		<v-toolbar>
			<v-toolbar-title class="grey--text ma-4">My portfolio</v-toolbar-title>
			<v-toolbar-items class="hidden-sm-and-down">
				<v-btn flat class="ml-4"><i class="fas fa-code fa-2x mr-2"></i>Works</v-btn>
				<v-btn flat class="ml-4"><i class="fas fa-user fa-2x mr-2"></i> About</v-btn>
				<v-btn flat class="ml-4"><i class="fas fa-envelope fa-2x mr-2"></i>Contact</v-btn>
			</v-toolbar-items>
			<v-spacer></v-spacer>
			<v-toolbar-side-icon class="hidden-sm-and-up mr-3"></v-toolbar-side-icon>
		</v-toolbar>
		<v-content>
			<v-container>
				<nuxt/>
			</v-container>
		</v-content>
	</v-app>
</template>

<script>
export default {};
</script>
