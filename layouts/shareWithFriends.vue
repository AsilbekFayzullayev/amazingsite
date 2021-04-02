<template>
  <v-row class="mt-5 px-1 align-center">
    <v-col cols="12" md="6" class="text-left">
      <p class="py-0 my-0">share with friends</p>
      <v-btn icon style="color: deepskyblue">
        <v-icon>mdi-telegram</v-icon>
      </v-btn>
      <v-btn icon style="color:darkslateblue ">
        <v-icon>mdi-facebook</v-icon>
      </v-btn>
      <v-btn icon style="color: darkred">
        <v-icon>mdi-instagram</v-icon>
      </v-btn>
      <v-btn icon style="color: green">
        <v-icon>mdi-whatsapp</v-icon>
      </v-btn>
    </v-col>
    <v-col cols="12" md="6" class="text-right mt-5">
      <v-icon small>mdi-eye</v-icon>
      <span>{{ 10000 }}</span>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "shareWithFriends"
}
</script>

<style scoped>

</style>
