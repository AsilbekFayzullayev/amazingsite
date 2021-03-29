<template>
  <v-app>

    <Header></Header>

    <navbar/>


    <v-main>
      <v-container>
        <v-row>
          <v-col md="8" offset-md="2" class="mt-10 text-md-center">
            <nuxt/>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      style="background-color: aliceblue;z-index: 2000"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>



export default {
  data() {
    return {
      fixed: false,
    }
  }
}
</script>

<style scoped>

</style>
