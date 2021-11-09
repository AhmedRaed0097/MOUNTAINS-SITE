<template>
  <v-row>
    <v-col>
      <h1>This is a inspire page</h1>
      <nuxt-link to="/">
        Back to home
      </nuxt-link>
    </v-col>
    <v-col class="text-center">
      <img
        src="/v.png"
        alt="Vuetify.js"
        class="mb-5"
      >
      <blockquote class="blockquote">
        &#8220;First, solve the problem. Then, write the code.&#8221;
        <footer>
          <small>
            <em>&mdash;John Johnson</em>
          </small>
        </footer>
      </blockquote>
    </v-col>
  </v-row>
</template>
