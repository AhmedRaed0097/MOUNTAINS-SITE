.<template>
  <nav>
    <!-- <v-card
          class="mx-auto overflow-hidden"
          height="400"
          width="344"
        > -->
    <!-- <v-system-bar color="deep-purple darken-3" /> -->
    <div class="small-nav d-lg-none d-xl-flex">
      <v-app-bar
        color="#F6D7A7"
        dark
        prominent
        height="80px"
      >
        <v-app-bar-nav-icon style="margin:10px;color: rgb(61, 61, 61);border:1px solid rgb(61, 61, 61)" @click.stop="drawer = !drawer" />
        <v-spacer />
      </v-app-bar>
      <v-navigation-drawer
        v-model="drawer"
        absolute
        left
        temporary
        style="background: #F6D7A7;"
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

    <v-row class="d-none d-lg-flex d-xl-none" style="padding-top: 5px;">
      <v-col lg="4" style="padding-top">
        <div class="logo">
          <h2>LOGO</h2>
        </div>
      </v-col>
      <v-col lg="8" style="padding-top:18px;">
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
        background-color:#F6D7A7;
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
