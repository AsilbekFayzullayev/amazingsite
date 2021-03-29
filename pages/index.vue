<template>
  <div>
    <v-row class="mt-10 text-center">
      <v-col md="8" offset-md="2" style="color: darkslategray!important">
        <h1>{{ $t('index_page.start_busines') }}</h1>
        <p class="my-5">{{ $t('index_page.register_domains') }}</p>
        <v-col
          md="8"
          offset-md="2"
          class="d-flex align-content"
        >
          <v-text-field
            class="text_field"
            :placeholder="$t('index_page.search_label')"
            :rules="rules"
            outlined
          >
            <v-icon slot="prepend-inner" style="color: darkslategray!important;font-family: 'Calibri'">
              www.
            </v-icon>
            <v-icon slot="append">
              mdi-magnify
            </v-icon>
          </v-text-field>
        </v-col>
        <p>{{ $t('index_page.price_year') }}</p>

        <!--  cards  -->

        <v-row class="my-10">
          <v-col>
            <v-card outlined class="cards py-3 px-3">
              <v-icon
                style="
            background-color: aliceblue;
            color: darkslategray;
            padding: 20px;
            border-radius: 50%;
            font-size: 80px;
            ">
                mdi-web
              </v-icon>
              <h2 class="my-10" style="letter-spacing: 0.5rem">Hosting</h2>
              <span>For all types of sites and CMS: Wordpress, Joomla, Drupal, Shopify and others</span>
              <p class="mt-10 mb-0 pb-0">from</p>
              <h2>14.000</h2>
              <p>sum / month</p>
              <v-btn class="tarif_btn" :to="`/${$i18n.locale}/hosting`">
                Tariffs
              </v-btn>
            </v-card>
          </v-col>
          <v-col>
            <v-card outlined class="cards py-3 px-3">
              <v-icon
                style="
            background-color: aliceblue;
            color: darkslategray;
            padding: 20px;
            border-radius: 50%;
            font-size: 80px;
            ">
                mdi-server-network
              </v-icon>
              <h2 class="my-10" style="letter-spacing: 0.5rem">VPS/VDS</h2>
              <span>Inexpensive and safety VPS / VDS hosting on SSD drives in Uzbekistan</span>
              <p class="mt-10 mb-0 pb-0">from</p>
              <h2>60.000</h2>
              <p>sum / month</p>
              <v-btn class="tarif_btn" :to="`/${$i18n.locale}/vps`">
                Tariffs
              </v-btn>
            </v-card>
          </v-col>
          <v-col>
            <v-card outlined class="cards py-3 px-3">
              <v-icon
                style="
            background-color: aliceblue;
            color: darkslategray;
            padding: 20px;
            border-radius: 50%;
            font-size: 80px;
            ">
                mdi-server
              </v-icon>
              <h2 class="my-10" style="letter-spacing: 0.5rem">Server</h2>
              <span>Dedicated server for highly loaded online stores, portals and game servers</span>
              <p class="mt-10 mb-0 pb-0">from</p>
              <h2>850.000</h2>
              <p>sum / month</p>
              <v-btn class="tarif_btn" :to="`/${$i18n.locale}/servers`">
                Tariffs
              </v-btn>
            </v-card>
          </v-col>

        </v-row>


      </v-col>
    </v-row>

    <v-row style="background-color: aliceblue" class="py-10 text-center">
      <v-col md="8" offset-md="2">
        <v-row>
          <v-col cols="12" md="8" style="">
            <v-card outlined class="py-5">
              <h2>Exclusive Sites</h2>
              <span>creative approach!</span>
              <p>
                <img width="200" height="200" src="https://eskiz.uz/assets/images/site_img.png" alt="">
              </p>
              <v-btn style="color: aliceblue;box-shadow: none;background: darkslategray;border-radius: 20px">more</v-btn>
            </v-card>
          </v-col>
          <v-col cols="12" md="4">
            <v-row>
              <v-col  cols="12" sm="12" >
                <v-card outlined class="py-5">
                  <h2>Exclusive Sites</h2>
                  <span>creative approach!</span>
                  <p>
                    <img width="200" height="200" src="https://eskiz.uz/assets/images/site_img.png" alt="">
                  </p>
                  <v-btn style="color: aliceblue;box-shadow: none;background: darkslategray;border-radius: 20px">more
                  </v-btn>
                </v-card>
              </v-col>
              <v-col  cols="12" sm="12" >
                <v-card outlined class="py-5">
                  <h2>Exclusive Sites</h2>
                  <span>creative approach!</span>
                  <p>
                    <img width="200" height="200" src="https://eskiz.uz/assets/images/site_img.png" alt="">
                  </p>
                  <v-btn style="color: aliceblue;box-shadow: none;background: darkslategray;border-radius: 20px">more
                  </v-btn>
                </v-card>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>

</template>

<script>
export default {
  data() {
    return {
      rules: [val => (val || '').length > 0 || `${this.$t('index_page.search_requires')}`]
    }
  },
  components: {}
}
</script>
<style scoped>
.text_field {
  border-radius: 20px;
  color: darkslategray !important;
  font-size: 25px;
}

.cards {
  box-shadow: 0 0 5px darkslategray;
}

.cards:hover {
}

.tarif_btn {
  color: aliceblue !important;
  background-color: darkslategray !important;
  box-shadow: none !important;
  border-radius: 20px !important;
}

.tarif_btn:hover {
  transform: scale(1.1);
}
</style>
