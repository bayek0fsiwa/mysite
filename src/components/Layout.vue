<template>
  <div class="layout">
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon>mdi-{{ `chevron-${miniVariant ? "right" : "left"}` }}</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn href="https://github.com/bayek0fsiwa" target="_blank">
      <v-icon>notranslate mdi mdi-github theme--light</v-icon>
      </v-btn>
      <v-btn href="https://gitlab.com/bayek0fsiwa" target="_blank">
      <v-icon>notranslate mdi mdi-gitlab theme--light</v-icon>
      </v-btn>
      <v-btn href="https://t.me/Diablo_Nemesis" target="_blank">
      <v-icon>notranslate mdi mdi-telegram theme--light</v-icon>
      </v-btn>
      <v-btn href="https://twitter.com/HH_EE_RR_OO" target="_blank">
      <v-icon>notranslate mdi mdi-twitter theme--light</v-icon>
      </v-btn>
    </v-app-bar>
    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      fixed: true,
      items: [
        {
          icon: "mdi-apps",
          title: "Home",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Timeline",
          to: "/timeline",
        },
      ],
      title: "Hi, There!👀",
    };
  },
};
</script>