<template>
<div>
  <pages_header
    title="Subdomain"
  />
  <v-row class="text-center">
    <v-col md="6" offset-md="3">
      <h2 class="my-5">Tariffs</h2>
      <p>Our company offers ssl certificates issued by well-known certification centers such as
        Comodo, Symantec, RapidSSL, GogetSSL, Thawte, and Geotrust.
        Comodo, Symantec, RapidSSL, GogetSSL, Thawte, and Geotrust.
      </p>
    </v-col>
  </v-row>
  <v-row>
    <v-col md="8" offset-md="2" class="text-center">
      <v-row class="text-center">
        <v-col cols="12" md="6" sm="6">
          <p style="color: darkred">Subdomain</p>
          <span>Certificates in the Domain category are called Domain Validated and provide security for a single domain.
                  These ssl certificates can be purchased by individuals and legal entities simply by filling out the Application form.
                  You can buy them for one year or if you want to save from 5 to 10% money, we recommend buying immediately for two year.
                </span>
        </v-col>
        <v-col cols="12" md="6" sm="6">
          <img src="https://eskiz.uz/assets/images/sslNote2.png" width="250" height="150"/>
        </v-col>
      </v-row>
      <v-row class="my-5">
        <v-col cols="12" md="3" sm="3">
          <v-card outlined class="px-4 py-4 text-center cards">
            <v-img src="https://my.eskiz.uz/data/4d479f2f294fdc3222377110c0e0833f.png" alt=""/>
            <p>RapidSSL Standard</p>
            <v-select
              class="px-10 mt-10"
              :items="itemsSelect"
              item-text="text"
              item-value="value"
              v-model="select"
              solo
            >
            </v-select>

            <h2>{{ value }}</h2>
            <p>UZS</p>

            <v-btn class="button" color="#8B0000FF" outlined>select</v-btn>
          </v-card>
        </v-col>
        <v-col cols="12" md="3" sm="3">
          <v-card outlined class="px-4 py-4 text-center cards">
            <v-img src="https://my.eskiz.uz/data/6e851d750452911f41edf2a599038762.png" alt=""/>
            <p>RapidSSL Standard</p>
            <v-select
              class="px-10 mt-10"
              :items="itemsSelect"
              item-text="text"
              item-value="value"
              v-model="select"
              solo
            >
            </v-select>

            <h2>{{ value }}</h2>
            <p>UZS</p>

            <v-btn class="button" color="#8B0000FF" outlined>select</v-btn>
          </v-card>
        </v-col>
        <v-col cols="12" md="3" sm="3">
          <v-card outlined class="px-4 py-4 text-center cards">
            <v-img src="https://my.eskiz.uz/data/4d479f2f294fdc3222377110c0e0833f.png" alt=""/>
            <p>RapidSSL Standard</p>
            <v-select
              class="px-10 mt-10"
              :items="itemsSelect"
              item-text="text"
              item-value="value"
              v-model="select"
              solo
            >
            </v-select>

            <h2>{{ value }}</h2>
            <p>UZS</p>

            <v-btn class="button" color="#8B0000FF" outlined>select</v-btn>
          </v-card>
        </v-col>
        <v-col cols="12" md="3" sm="3">
          <v-card outlined class="px-4 py-4 text-center cards">
            <v-img src="https://my.eskiz.uz/data/dd03eba42a82cb27f872b7671620ad88.png" alt=""/>
            <p>RapidSSL Standard</p>
            <v-select
              class="px-10 mt-10"
              :items="itemsSelect"
              item-text="text"
              item-value="value"
              v-model="select"
              solo
            >
            </v-select>

            <h2>{{ value }}</h2>
            <p>UZS</p>

            <v-btn class="button" color="#8B0000FF" outlined>select</v-btn>
          </v-card>
        </v-col>
      </v-row>

      <h2 class="my-10">We are trusted</h2>
      <v-tabs class="my-10" color="#8b0000" centered>
        <v-tab>Banks</v-tab>
        <v-tab>Government agencies</v-tab>
        <v-tab>Business</v-tab>
        <v-tab-item>
          <v-row class="mt-10 ">
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/kdbbank.jpg" alt="">
            </v-col>
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/kdbbank.jpg" alt="">
            </v-col>
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/kdbbank.jpg" alt="">
            </v-col>
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/kdbbank.jpg" alt="">
            </v-col>
          </v-row>
        </v-tab-item>
        <v-tab-item>
          <v-row class="mt-10 ">
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/utg.png" alt="">
            </v-col>
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/utg.png" alt="">
            </v-col>
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/utg.png" alt="">
            </v-col>
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/utg.png" alt="">
            </v-col>
          </v-row>
        </v-tab-item>
        <v-tab-item>
          <v-row class="mt-10">
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/uzbekinvest.png" alt="">
            </v-col>
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/uzbekinvest.png" alt="">
            </v-col>
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/uzbekinvest.png" alt="">
            </v-col>
            <v-col cols="12" sm="3" md="3">
              <img src="https://eskiz.uz/assets/images/ssllogo/uzbekinvest.png" alt="">
            </v-col>
          </v-row>
        </v-tab-item>
      </v-tabs>
      <hr>
      <share-with-friends />
    </v-col>
  </v-row>
</div>
</template>

<script>
import Pages_header from "../layouts/pagesHeader";
export default {
  name: "subdomain",
  components: {Pages_header},
  data: () => ({
    value: 185000,
    select: {text: "1 year", value: 1},
    itemsSelect: [
      {text: "1 year", value: 1},
      {text: "2 year", value: 2},
    ]
  }),
  watch: {
    select(item) {
      this.value = 185000 * item
    }
  }
}
</script>

<style scoped>

</style>
