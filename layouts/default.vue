<template>
  <v-app dark>
    <v-app-bar
      clipped-left
      fixed
      app
    >

      <v-toolbar-title>
        Schedular
      </v-toolbar-title>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
    absolute
    app
    >
    <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>
