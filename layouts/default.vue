<template>
  <v-app>
    <nav>
      <v-toolbar flat app class="teal accent-4 white--text">
        <v-toolbar-title class="display-1 ma-3">
          Portfolio
        </v-toolbar-title>

        <v-spacer />
        <v-toolbar-items v-for="link in links" :key="link.text" class="hidden-sm-and-down">
          <v-btn flat router :to="link.route" class="teal accent-4 white--text">
            <v-icon>{{ link.icon }}</v-icon>{{ link.text }}
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </nav>

    <v-content id="top">
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <v-footer height="65" class="white--text" color="primary lighten-1" app>
      <v-layout justify-center row wrap>
        <v-flex text-xs-center xs12 hidden-md-and-up>
          <v-btn
            v-for="link in links"
            :key="link"
            router
            :to="link.route"
            color="white"
            flat
            xs4
          >
            <v-icon>
              {{ link.icon }}
            </v-icon>
            <span>
              {{ link.text }}
            </span>
          </v-btn>
        </v-flex>
        <v-flex primary lighten-1 text-xs-center xs12>
          &copy;2019 — <strong>roffet</strong>
        </v-flex>
      </v-layout>
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
