<template>
  <div class="home">
    <v-container>
      <vue-typed-js :strings="['Developer🚀', 'Upcoming DevOps Engineer', 'Gamer🕹']" :loop="true" @onComplete="doSmth()">
        <h2>I am a <span class="typing"></span></h2>
      </vue-typed-js>
      <vue-typed-js :strings="['System Administrator', 'Analyst']" :loop="true" @onComplete="doSmth()">
        <h2>Currently Working as a <span class="typing"></span>@HCL🏢</h2>
      </vue-typed-js>
      <br>
      <v-btn href="https://www.dropbox.com/s/s70elwfl53me6go/VikasKrGupta_Resume.pdf?dl=1" target="_blank">
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
