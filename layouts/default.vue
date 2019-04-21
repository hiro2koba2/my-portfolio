<template>
  <v-app>
    <nav>
      <v-toolbar flat app class="teal accent-4 white--text">
        <v-toolbar-title class="display-1 ma-3">
          Portfolio
        </v-toolbar-title>

        <v-spacer />
        <v-toolbar-items v-for="link in links" :key="link.text" class="hidden-sm-and-down">
          <v-btn flat :to="link.route" class="teal accent-4 white--text">
            <v-icon>{{ link.icon }}</v-icon>{{ link.text }}
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </nav>

    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <v-bottom-nav
      app
      :value="true"
      dark
      class="primary lighten-1 hidden-md-and-up"
    >
      <v-btn
        v-for="link in links"
        :key="link.text"
        :to="link.route"
        flat
      >
        <span>{{ link.text }}</span>
        <v-icon>
          {{ link.icon }}
        </v-icon>
      </v-btn>
    </v-bottom-nav>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      links: [
        { icon: 'code', text: 'Works', route: '/' },
        { icon: 'person', text: 'About', route: '/about' },
        { icon: 'mail', text: 'Contact', route: '/contact' },
      ]
    }
  }
}
</script>
