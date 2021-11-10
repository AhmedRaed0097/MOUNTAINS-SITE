<template>
  <v-app class="app">
    <div>
      <Nav />
    </div>
    <div>
      <Nuxt />
    </div>
    <div>
      <Footer />
    </div>
    <!-- <v-row>
      <v-col xs="12" style="padding: 0;margin-top: 250px;">
      </v-col>
    </v-row> -->
    <!-- <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer> -->
  </v-app>
</template>

<script>
// import Nav from '~/components/nav.vue'
export default {
  components: {
    // Nav
  },
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
<style>
*{
  font-family: cairo ;
  color: rgb(61, 61, 61);
  /* color: #fff; */
}

</style>
