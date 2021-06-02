<template>
  <v-app>
    <v-app-bar
      color="#34558b"
      dark
    >

      <v-spacer></v-spacer>
      <h1>Aidan Mackey</h1>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <Index/>
    </v-main>
  </v-app>
</template>

<script>
import Index from './components/Index';

export default {
  name: 'App',

  components: {
    Index,
  },

  created() {
    document.title = "Music 7 Final"
  },

  data: () => ({
    //
  }),
};
</script>
