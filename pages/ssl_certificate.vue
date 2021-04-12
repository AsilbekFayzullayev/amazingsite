<template>
  <div>
    <pages_header
      title="SSL Certificate"
      text="Domain validation certificate (DV)"
    />
    <v-tabs centered color="#033">
      <v-tab>Domain</v-tab>
      <v-tab>Subdomain</v-tab>
      <v-tab>Cetificate with company name</v-tab>

      <v-tab-item>
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
                <p style="color: darkred">Domain</p>
                <span>Certificates in the Domain category are called Domain Validated and provide security for a single domain.
                  These ssl certificates can be purchased by individuals and legal entities simply by filling out the Application form.
                  You can buy them for one year or if you want to save from 5 to 10% money, we recommend buying immediately for two year.
                </span>
              </v-col>
              <v-col cols="12" md="6" sm="6">
                <img src="https://eskiz.uz/assets/images/sslNote1.png" width="250" height="150"/>
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
      </v-tab-item>

      <v-tab-item>
        <subdomain />
      </v-tab-item>
      <v-tab-item>
        <certificate_company_name />
      </v-tab-item>
    </v-tabs>
  </div>
</template>

<script>
import Pages_header from "../layouts/pagesHeader";
import ShareWithFriends from "../layouts/shareWithFriends";
import Subdomain from "./subdomain";
import Certificate_company_name from "./certificate_company_name";

export default {
  name: "ssl_certificate",
  components: {Certificate_company_name, Subdomain, ShareWithFriends, Pages_header},
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
.cards {
  transition: all .5s ease-in-out;
}

.cards:hover {
  box-shadow: 0 2px 4px grey;
  transform: scale(1.04);
}

.button {
  color: darkred;
  box-shadow: none;
  background-color: transparent !important;
  border-radius: 20px !important;

}
</style>
