<template>
  <v-app dark>
    <Layout />
    <v-content class="mx-4 mb-4">
       <router-view />
    </v-content> 
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
