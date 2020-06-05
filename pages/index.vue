<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex
      xs12
      sm8
      md6
    >
      <div class="text-center">
        <vuetify-logo />
      </div>
      <v-card>
        <v-card-title class="headline justify-center">
          Welcome to the ISKCON directory
        </v-card-title>
        <v-card-text>
          <p class=text-center>This is a list of all ISKCON temples in India.</p>
          <p class=text-center>Always chant "Hare Krishna" and be happy!</p>

        </v-card-text>
        <v-card-actions>
        <v-switch
          v-model="$vuetify.theme.dark"
          primary
          label="Dark"
        ></v-switch>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/inspire"
          >
            Continue
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  asyncData ({ params, error, $axios }) {
    return $axios.get(`https://jsonplaceholder.typicode.com/todos/1`)
      .then((res) => {
        return { title: res.data.title }
      })
      .catch((e) => {
        error({ statusCode: 404, message: 'Post not found' })
      })
  }
}
</script>
