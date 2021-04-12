<template>
  <div>
    <pages_header
      title="Mail"
      text="MAIL FOR YOUR BUSINESS AT .UZ DOMAIN"
    />
    <v-row class="text-center">
      <v-col md="8" offset-md="2">
        <h2 class="my-5">Mail Plans</h2>
        <v-row class="my-10">
          <v-col cols="12" md="3" sm="3" v-for="i of card" :key="i.id">
            <v-card outlined style="border-radius: 30px">
              <h4 class="py-2" style="background-color: aquamarine;font-size: 20px">Mail-{{ i.mail_plan }}GB</h4>
              <h4 style="color: orangered;letter-spacing: 8px;transform: skew(-10deg);font-size: 30px"
                  class="font-weight-bold">cPanel</h4>
              <div class="d-flex mx-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">Storage</span>
                <v-spacer></v-spacer>
                <span class="text-right font-weight-bold">{{ i.storage }} GB</span>
              </div>
              <div class="d-flex mx-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">Mailbox</span>
                <v-spacer></v-spacer>
                <span class="text-right font-weight-bold">{{ i.mailbox }}</span>
              </div>
              <div class="d-flex mx-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">Domains count</span>
                <v-spacer></v-spacer>
                <span class="text-right font-weight-bold">{{ i.domains_count }}</span>
              </div>
              <div class="d-flex px-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">In tas-ix zone</span>
                <v-spacer></v-spacer>
                <span class="text-right font-weight-bold"><v-icon style="color: darkred">mdi-checkbox-multiple-marked-circle-outline </v-icon></span>
              </div>
              <v-select
                class="mt-5 mx-10"
                :items="items"
                placeholder="placeholder"
                v-model="valueSum"
                item-text="text"
                item-value="value"
                outlined
                dense
              ></v-select>

              <h2>{{ i.forOneMonthValue * selectPlan }}</h2>
              <p>UZS</p>
              <h4 class="py-2" style="background-color: aquamarine;font-size: 20px">Select</h4>
            </v-card>
          </v-col>
        </v-row>
        <p class="text-left">It is provided only when paid for a year and is valid for one year *</p>
        <share-with-friends />
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Pages_header from "../layouts/pagesHeader";
import card from "../fake_services/mailservices.json"
import ShareWithFriends from "../layouts/shareWithFriends";

export default {
  name: "mail",
  data: () => ({
    items: [
      {text: 'for 1 month', value: '1'},
      {text: 'for 3 month', value: '3'},
      {text: 'for 6 month', value: '6'},
      {text: 'for 1 year', value: '12'}
    ],
    card: card,
    selectPlan: 1,
    valueSum: {text: 'for 1 month', value: '1'}
  }),
  components: {ShareWithFriends, Pages_header},
  watch: {
    valueSum(value) {
      this.selectPlan = value
    }
  }
}
</script>

<style scoped>

</style>
