<template>
  <div>
    <v-row class="py-10" style="background-color: aliceblue;color: darkslategray">
      <v-col md="8" offset-md="2" class="text-center">
        <h1>Discount and sales</h1>
        <p>Always a big collection of discounts</p>
      </v-col>
    </v-row>
    <v-tabs class="text-center" centered color="#033">
      <v-tab>Discounts for students</v-tab>
      <v-tab>For New Customers</v-tab>
      <v-tab>Reseller</v-tab>

      <v-tab-item class="pt-10">
        <Student/>
      </v-tab-item>
      <v-tab-item class="pt-10">
        <v-row>
          <v-col offset-md="2" md="8">
            <v-row class="text-center">
              <v-col cols="12" sm="3" md="3" v-for="item of discounts" :key="item.id">
                <v-card outlined>
                  <span style="color: aliceblue;background-color: darkslategray;border-radius: 50%;" class="px-5 py-5">
                    {{ item.percent }}%</span>
                  <h2 class="mt-4">{{ item.title }}</h2>
                  <p>when paying for a year</p>
                  <p style="outline: 2px dotted darkred; color: darkred" class="mx-2 py-4">
                    unique code: {{ item.unicode }}
                  </p>
                  <span>Discount is valid until: </span>
                  <p style="color: darkred">{{ item.date }}</p>
                </v-card>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
        <ShareWithFriends />
      </v-tab-item>
      <v-tab-item class="pt-10">
        <Reseller/>
      </v-tab-item>
    </v-tabs>
  </div>
</template>

<script>
import ShareWithFriends from "@/layouts/shareWithFriends";
import Reseller from "@/pages/reseller";
import Student from "@/pages/student";

export default {
  name: "sale",
  components: {Student, Reseller, ShareWithFriends},
  data() {
    return {
      discounts: [
        {id: 1, percent: 25, title: "Domain", unicode: "domain", date: "31 december 2021"},
        {id: 2, percent: 23, title: "Hosting", unicode: "hosting", date: "31 december 2021"},
        {id: 3, percent: 3, title: "SSL cetificate", unicode: "ssl", date: "31 december 2021"},
        {id: 4, percent: 10, title: "VPS/VDS", unicode: "vps", date: "31 december 2021"},
        {id: 5, percent: 20, title: "Mail", unicode: "mail", date: "31 december 2021"},
      ]
    }
  }
}
</script>

<style scoped>

</style>
