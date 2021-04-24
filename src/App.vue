<template>
  <v-app>
    <Layout />

    <router-view />
  </v-app>
</template>

<script>
import Layout from './components/Layout';

export default {
  name: 'App',

  components: { Layout },

  data: () => ({
    //
  }),
};
</script>
