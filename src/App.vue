<template>
  <v-app>

    <!-- Top Navigation -->
    <v-app-bar app color="blue darken-1" dark height="75" >

      <v-toolbar-title class="font-weight-bold headline">
        TRANSWORD
      </v-toolbar-title>
    </v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
