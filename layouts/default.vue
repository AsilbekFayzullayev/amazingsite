<template>
  <v-app class="app">
    <Header/>
    <Navbar/>
    <v-main class="my-5">
      <transition name="route" mode="out-in">
        <nuxt/>
      </transition>
    </v-main>
    <v-footer
      :absolute="!fixed"
      style="background-color: aliceblue;z-index: 2000;border-bottom: 1px solid lightgray;border-top: 1px solid lightgray"
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
.app {
  font-family: "sans-serif";
}

.route-enter, .route-leave-to {
  opacity: 0;
}

.route-enter-active, .route-leave-active {
  transition: all 1s ease-in-out;
}
</style>
