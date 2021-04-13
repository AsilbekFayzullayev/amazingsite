<template>
  <div>
    <pages-header
      title="VPS/VDS hosting on SSD drives"
      text="INEXPENSIVE AND SAFETY VPS / VDS HOSTING ON SSD DRIVES IN UZBEKISTAN"
    />
    <v-row>
      <v-col md="8" offset-md="2" class="text-center">
        <h4 class="my-5">Tariffs</h4>
        <v-btn-toggle mandatory color="#8b0000" v-model="plan">
          <v-btn value="standart">
            Standart
          </v-btn>
          <v-btn value="powerful">
            Powerful
          </v-btn>
        </v-btn-toggle>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import PagesHeader from "../layouts/pagesHeader"
export default {
  name: "vps",
  data:()=>({
    plan: 'standart'
  }),
  components: {PagesHeader}
}
</script>

<style scoped>

</style>
