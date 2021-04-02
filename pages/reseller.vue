<template>
  <div class="text-center">
    <Pages_header title="Reseller program" text="GET A DISCOUNT ON EVERY ORDER"/>
    <h4 class="mt-10">Profitable Partnership Program</h4>
    <v-row>
      <v-col md="8" offset-md="2" style="z-index: 0;position: relative">
        <v-card outlined
                style="display: flex;background-color: darkslategray;color: aliceblue;padding: 80px;margin: 100px">
          <div>
            <h2>Earn With Our Partnership Program</h2>
            <span>Receive a discount on every payment</span>
          </div>
          <v-progress-circular
            style="margin: 2rem; background-color: aliceblue;color: darkred;padding: 100px;border-radius: 50%;position:absolute;top:-75px;right:-90px;z-index: 10;font-size: 50px"
            :rotate="90"
            :size="300"
            :width="30"
            :value="80"
          >
            <p>
              {{ 80 }}%
            </p>
          </v-progress-circular>
        </v-card>
      </v-col>
    </v-row>
    <v-row style="background-color: darkslategray">
      <v-col md="8" offset-md="2" style="color: aliceblue">
        <h2 class="my-5">How does the program work ?</h2>
        <v-row class="py-4 text-center">
          <v-col>
            <v-img width="100" height="100" src="https://eskiz.uz/assets/images/contract1.svg">
            </v-img>
            <p class="mt-4">Place an order</p>
          </v-col>
          <v-spacer></v-spacer>
          <v-col>
            <v-img width="100" height="100" src="https://eskiz.uz/assets/images/shopping-cart(1).svg">
            </v-img>
            <p class="mt-4">You or your client makes a payment</p>
          </v-col>
          <v-spacer></v-spacer>
          <v-col>
            <v-img width="100" height="100" src="https://eskiz.uz/assets/images/discount(1).svg">
            </v-img>
            <p class="mt-4">The percentage (%) of the amount is returned to your balance
            </p>
          </v-col>
          <v-spacer></v-spacer>

          <v-col>
            <v-img width="100" height="100" src="https://eskiz.uz/assets/images/offer.svg">
            </v-img>
            <p class="mt-4">Spend the received discount on the purchase of new services</p>
          </v-col>
        </v-row>
      </v-col>
    </v-row>

    <v-row>
      <v-col md="8" offset-md="2">
        <h4 class="mt-5">IT IS EASY TO BECOME A PARTNER!</h4>

        <v-row class="mt-10">
          <v-col cols="12" md="3" sm="3">
            <span style="background-color: darkgoldenrod;border-radius: 50%" class="px-4 py-3">1</span>
            <v-card class="mt-5 py-4 px-2" outlined>
              <h4>To Send an application in order to get a partnership</h4>
              <hr class="mt-2"/>
              <span><v-icon>mdi-arrow-down-drop-circle </v-icon></span>
              <p>After receiving the request, we will contact you</p>
            </v-card>
          </v-col>
          <v-col cols="12" md="3" sm="3">
            <span style="background-color: darkgoldenrod;border-radius: 50%" class="px-4 py-3">2</span>
            <v-card class="mt-5 py-4 px-2" outlined>
              <h4>Recharge your balance</h4>
              <hr class="mt-2"/>
              <span><v-icon>mdi-arrow-down-drop-circle </v-icon></span>
              <p>Minimum balance replenishment amount is 200,000 sum</p>
            </v-card>
          </v-col>
          <v-col cols="12" md="3" sm="3">
            <span style="background-color: darkgoldenrod;border-radius: 50%" class="px-4 py-3">3</span>
            <v-card class="mt-5 py-4 px-2" outlined>
              <h4>To Send an application in order to get a partnership</h4>
              <hr class="mt-2"/>
              <span><v-icon>mdi-arrow-down-drop-circle </v-icon></span>
              <p>After receiving the request, we will contact you</p>
            </v-card>
          </v-col>
          <v-col cols="12" md="3" sm="3">
            <span style="background-color: darkgoldenrod;border-radius: 50%" class="px-4 py-3">4</span>
            <v-card class="mt-5 py-4 px-2" outlined>
              <h4>To Send an application in order to get a partnership</h4>
              <hr class="mt-2"/>
              <span><v-icon>mdi-arrow-down-drop-circle </v-icon></span>
              <p>After receiving the request, we will contact you</p>
            </v-card>
          </v-col>
        </v-row>
        <v-btn class="py-5 mt-10 button">Become a partner</v-btn>
      </v-col>
    </v-row>

  </div>
</template>

<script>
import Pages_header from "@/layouts/pagesHeader";

export default {
  name: "reseller",
  components: {Pages_header}
}
</script>

<style scoped>
.button {
  background-color: darkslategray !important;
  color: aliceblue!important;
  border-radius: 30px
}

.button:hover {
  transform: scale(1.1);
}
</style>
