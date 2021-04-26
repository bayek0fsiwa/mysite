<template>
  <v-app dark>
    <Layout />
    <v-content class="mx-4 mb-4">
       <!-- <router-view v-slot="{ Component }">
         <transition name="route" mode="out-in">
         <component :is="Component"></component>
         </transition>
       </router-view> -->
       <transition name="route" mode="out-in">
          <router-view></router-view>
       </transition>
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

<style scoped>
.route-enter-from {
  opacity: 0;
  transform: translateX(100px);
}
.route-enter-active {
  transition: all 0.3s ease-out;
}
.route-leave-to {
  opacity: 0;
  transform: translateX(-100px);
}
.route-leave-active {
  transition: all 0.3s ease-in;
}
</style>
