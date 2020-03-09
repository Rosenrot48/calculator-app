<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-content>
      <Settings/>
    </v-content>
  </v-app>
</template>

<script>

import Settings from "./components/Settings";
export default {
  name: 'App',

  components: {
    Settings
  },

  data: () => ({
    //
  }),
};
</script>
