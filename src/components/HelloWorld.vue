<template>
  <v-card
    class="mx-auto overflow-hidden"
    height="100%"
    width="100%"
  >
    <v-system-bar color="grey darken-4"></v-system-bar>

    <v-app-bar
      color="black lighten-4"
      dark
      prominent
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>My files</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-filter</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      bottom
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>New Note</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>New Folder</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Trash</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Share</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-card-text>
      If Scribi had copyright laws I would put it here but we dont.
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    group: null
  }),
  watch: {
    group () {
      this.drawer = false
    }
  }
}
</script>
