<template>
  <v-app>
    <v-container>
      <!-- Headline -->
      <v-row>
        <v-col xs="12">
          <h1 class="text-center mb-5">
            {{ 'my mountains site'.toUpperCase() }}
          </h1>
        </v-col>
      </v-row>
      <!-- Carousel -->

      <v-row>
        <v-col xs="4" cols="12" class="mb-10">
          <Carousel />
        </v-col>
      </v-row>
      <hr style="border-top: 1px solid rgb(61, 61, 61);">
      <hr style="border-top: 1px solid rgb(61, 61, 61);margin-bottom: 50px;">
      <!-- Main -->

      <v-row v-for="(mountain , i) in mountains" :key="i">
        <v-col
          cols="12"
          md="6"
          sm="12"
          class="content"
          style=" display: flex;
                  flex-direction: column;
                  justify-content: center;"
        >
          <div class="name">
            <h2 style="display: inline-block">
              {{ 'continent'.toUpperCase() +' : ' }}
            </h2>
            <h3 style="display: inline-block">
              {{ mountain.continent }}
            </h3>
            <br>
            <h4 style="display: inline-block">
              {{ 'country'.toUpperCase() +' : ' }}
            </h4>
            <h5 style="display: inline-block">
              {{ mountain.countries[0] }}
            </h5>
          </div>
          <div class="decription">
            <p>{{ mountain.description }}</p>
          </div>
        </v-col>
        <v-col cols="12" md="6" sm="12" class="img mt-10">
          <div class="img">
            <img width="100%" :src="mountain.image" alt="Mountain-image">
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>
<script>
export default {
  data () {
    return {
      mountains: this.fetch
    }
  },
  async fetch () {
    this.mountains = await fetch(
      'https://api.nuxtjs.dev/mountains'
    ).then(res => res.json())
  }
}
</script>
