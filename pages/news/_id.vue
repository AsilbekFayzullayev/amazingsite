<template>
  <div>
    <v-row class="py-10 text-center" style="background-color: aliceblue;color: darkslategray">
      <v-col md="8" offset-md="2">

        <h1>News and Events</h1>
        <v-btn style="background-color: darkslategray;color: aliceblue" :to="`/${$i18n.locale}/new`">Back to News
        </v-btn>
      </v-col>
    </v-row>

    <v-row>
      <v-col md="8" offset-md="2">
      <span style="background-color: darkred;color: aliceblue;border-radius: 50%"
            class="px-2 py-1">{{ getItem.id }}</span>
        <h4>{{ getItem.date }}</h4>
        <p>{{ getItem.description }}</p>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "id",
  computed: {
    getItem() {
      return this.$store.state.newItem
    }
  }

}
</script>

<style scoped>

</style>
