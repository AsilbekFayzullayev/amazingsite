<template>
  <v-row style="background-color: aliceblue;color: darkslategray" class="text-center py-10">
    <v-col md="6" offset-md="3">
      <h1>{{ title }}</h1>
      <span>{{ text }}</span>
    </v-col>
  </v-row>
</template>

<script>
export default {
  props: ['title', 'text'],
  name: "pages_header"
}
</script>

<style scoped>

</style>
