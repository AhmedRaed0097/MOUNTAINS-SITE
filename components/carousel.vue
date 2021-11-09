<template>
  <v-carousel
    cycle
    height="450"
    :show-arrows="false"
    hide-delimiters
  >
    <v-carousel-item
      v-for="(mountain,i) in mountains"
      :key="i"
      :src="mountain.image"
      reverse-transition="slide-x-transition"
      transition="slide-x-transition"
    />
  </v-carousel>
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
