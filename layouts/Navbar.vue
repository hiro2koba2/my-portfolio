<template>
  <nav>
    <v-toolbar flat app>
      <v-toolbar-title class="grey--text ma-4">
        portfolio
      </v-toolbar-title>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat class="ml-4"><i class="fas fa-code fa-2x mr-2"></i>Works</v-btn>
        <v-btn flat class="ml-4"><i class="fas fa-user fa-2x mr-2"></i> About</v-btn>
        <v-btn flat class="ml-4"><i class="fas fa-envelope fa-2x mr-2"></i>Contact</v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
      <v-toolbar-side-icon class="hidden-sm-and-up mr-3" @click="drawer = !drawer"></v-toolbar-side-icon>
    </v-toolbar>

    <v-navigation-drawer app v-model="drawer" class="primary">
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
    </v-navigation-drawer>
  </nav>
</template>
