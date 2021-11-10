.<template>
  <nav>
    <!-- <v-card
          class="mx-auto overflow-hidden"
          height="400"
          width="344"
        > -->
    <!-- <v-system-bar color="deep-purple darken-3" /> -->
    <div class="small-nav d-flex d-md-none">
      <v-app-bar
        dark
        prominent
        height="80px"
        class="app-bar"
      >
        <v-app-bar-nav-icon style="margin:10px;color: rgb(61, 61, 61);font-size :30px" class="drawer-icon" @click.stop="drawer = !drawer" />
        <v-spacer />
      </v-app-bar>
      <v-navigation-drawer
        v-model="drawer"
        absolute
        left
        temporary
        style="background: rgb(134 174 217)"
      >
        <v-list
          nav
          dense
        >
          <v-list-item-group
            v-model="group"
            active-class="deep-blue--text text--accent-4"
          >
            <v-list-item>
              <v-list-item-title>Foo</v-list-item-title>
            </v-list-item>

            <v-list-item>
              <v-list-item-title>Bar</v-list-item-title>
            </v-list-item>

            <v-list-item>
              <v-list-item-title>Fizz</v-list-item-title>
            </v-list-item>

            <v-list-item>
              <v-list-item-title>Buzz</v-list-item-title>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </div>
    <!-- </v-card> -->

    <v-row class="larg-nav d-none d-md-flex" style="padding-top: 10px;">
      <v-col lg="4">
        <div class="logo">
          <h2>LOGO</h2>
        </div>
      </v-col>
      <v-col lg="8">
        <ul>
          <li>Services</li>
          <li>About</li>
          <li>Contact</li>
        </ul>
      </v-col>
    </v-row>
  </nav>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    group: null
  }),

  watch: {
    group () {
      this.drawer = false
    }
  }
  // async fetch () {
  //   this.mountains = await fetch(
  //     'https://api.nuxtjs.dev/mountains'
  //   ).then(res => res.json())
  // }
}
</script>
<style lang="scss">
nav{
        padding:0 0  10px 0;
.logo{
  margin: 0 20px;
}
ul{
    display: flex;
    justify-content: space-around;
    align-items: center;
    list-style: none;

  li{
    font-size: 18px;
    font-weight: bold;
}
}
}

</style>
