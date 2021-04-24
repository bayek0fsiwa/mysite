<template>
  <div class="home">
    <v-container>
      <vue-typed-js :strings="['Developer🚀', 'Network Engineer', 'Gamer🕹']" :loop="true" @onComplete="doSmth()">
        <h2>I am a <span class="typing"></span></h2>
      </vue-typed-js>
      <vue-typed-js :strings="['IT Administrator', 'Network Engineer']" :loop="true" @onComplete="doSmth()">
        <h2>Currently Working as a <span class="typing"></span>@HCL🏢</h2>
      </vue-typed-js>
      <br>
      <v-btn href="" target="_blank">
      <v-icon>notranslate mdi mdi-file theme--light</v-icon>
        Here's My CV
      </v-btn>
    </v-container>
  </div>
</template>

<script>
import Vue from 'vue'
import VueTypedJs from 'vue-typed-js'

Vue.use(VueTypedJs)

export default {
  name: 'Home',
  components: { }
}
</script>
