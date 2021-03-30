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
          <!--          ssl certificate  -->
          <v-col cols="12" md="12">
            <v-card outlined style="border-radius: 15px;display: flex;align-items: center">
              <div
                style="position: absolute;top: 0;left: 0;width: 100px;height: 100px; background-color: darkslategray;clip-path: polygon(80% 1%, 0 0, 0 80%);display: grid">
              </div>
              <div
                style="position: absolute;bottom: 0;right: 0;width: 100px;height: 100px; border-radius: 15px; background-color: darkslategray;clip-path: polygon(100% 20%, 20% 100%, 100% 100%)">
              </div>
              <v-spacer></v-spacer>
              <div>
                <h2 class="pt-5">Protect your site
                </h2>
                <span style="color: darkslategray">SSL sertificate</span>
              </div>
              <p class="mx-10">
                <img width="200" height="200" src="https://eskiz.uz/assets/images/ssl_img.png" alt="">
              </p>
              <div>
                <p></p>
                <v-btn
                  class="mb-5 tarif_btn"
                  :to="`/${$i18n.locale}/ssl_certificate`"
                  style="color: aliceblue;box-shadow: none;background: darkslategray;border-radius: 20px">
                  low price
                </v-btn>
              </div>
              <v-spacer></v-spacer>

            </v-card>
          </v-col>

          <!--          exclusive sites   -->
          <v-col cols="12" md="4">
            <v-card outlined class="py-10" style="border-radius: 15px">
              <div
                style="position: absolute;top: 0;left: 0;width: 100px;height: 100px; background-color: darkslategray;clip-path: polygon(80% 1%, 0 0, 0 80%);display: grid">
              </div>
              <div
                style="position: absolute;bottom: 0;right: 0;width: 100px;height: 100px; border-radius: 15px; background-color: darkslategray;clip-path: polygon(100% 20%, 20% 100%, 100% 100%)">
              </div>
              <h2 class="pt-5">Exclusive Sites</h2>
              <span>creative approach!</span>
              <p class="py-1">
                <img width="200" height="200" src="https://eskiz.uz/assets/images/site_img.png" alt="">
              </p>
              <v-btn
                class="mb-5 tarif_btn"
                :to="`/${$i18n.locale}/exclusive_sites`"
                style="color: aliceblue;box-shadow: none;background: darkslategray;border-radius: 20px">
                more
              </v-btn>
            </v-card>
          </v-col>

          <v-col cols="12" md="8">
            <v-row>
              <!--          mail   -->
              <v-col cols="12" md="12">
                <v-card class="py-10" outlined style="border-radius: 15px">
                  <div
                    style="position: absolute;top: 0;left: 0;width: 100px;height: 100px; background-color: darkslategray;clip-path: polygon(80% 1%, 0 0, 0 80%);display: grid">
                  </div>
                  <div
                    style="position: absolute;bottom: 0;right: 0;width: 100px;height: 100px; border-radius: 15px; background-color: darkslategray;clip-path: polygon(100% 20%, 20% 100%, 100% 100%)">
                  </div>
                  <h2 class="pt-5">Mail your business</h2>
                  <v-btn
                    class="my-5 tarif_btn"
                    :to="`/${$i18n.locale}/mail`"
                    style="color: aliceblue;box-shadow: none;background: darkslategray;border-radius: 20px">
                    Tariffs
                  </v-btn>
                </v-card>
              </v-col>

              <!--          sms  -->
              <v-col cols="12" md="12">
                <v-card class="py-10" outlined style="border-radius: 15px">
                  <div
                    style="position: absolute;top: 0;left: 0;width: 100px;height: 100px; background-color: darkslategray;clip-path: polygon(80% 1%, 0 0, 0 80%);display: grid">
                  </div>
                  <div
                    style="position: absolute;bottom: 0;right: 0;width: 100px;height: 100px; border-radius: 15px; background-color: darkslategray;clip-path: polygon(100% 20%, 20% 100%, 100% 100%)">
                  </div>
                  <h2 class="pt-5">Sms notifications in Uzbekistan and for foreign countries</h2>
                  <v-btn
                    class="my-5 tarif_btn"
                    :to="`/${$i18n.locale}/sms`"
                    style="color: aliceblue;box-shadow: none;background: darkslategray;border-radius: 20px">
                    From 50 uzs
                  </v-btn>
                </v-card>
              </v-col>
            </v-row>
          </v-col>

        </v-row>
      </v-col>
    </v-row>
    <v-row style="background-color: white;border-top: 2px solid lightgray;border-bottom: 2px solid lightgray">
      <v-col md="8" offset-md="2">
        <v-row class="align-center py-2">
          <v-col style="color: darkred" class="ml-2">PAY EASY !</v-col>
          <v-spacer></v-spacer>
          <v-col v-for="(link) of pay_cards" :key="link">
            <img width="150" height="50" :src="link" alt="">
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row class="mt-10">
      <v-col md="8" offset-md="2" class="px-5">
        <v-row>
          <v-col cols="12" md="6">
            <v-card outlined style="background-color: aliceblue;" class="px-10">
              <h2 class="pt-5">News and Events</h2>
              <div class="my-10 align-center" v-for="n in news" :key="n.text">
                <span style="background-color: darkslategray; padding: 5px;color: aliceblue">{{ n.date }}</span>
                <span class="ml-4">{{ n.text }}</span>
                <hr CLASS="my-5"/>
              </div>
              <p style="text-align: center">
                <v-btn class="tarif_btn mb-5" :to="`${$i18n.locale}/news`"
                       style="color: aliceblue;background-color: darkslategray;border-radius: 20px">all news
                </v-btn>
              </p>
            </v-card>
          </v-col>
          <v-col cols="12" md="6">
            <v-card outlined style="background-color: aliceblue" class="px-10 py-5">
              <div class="d-flex align-center">
                <h2>Video reviews</h2>
                <v-spacer></v-spacer>
                <v-btn style="background-color: transparent;box-shadow: none;color: darkred" @click="showDialog">
                  Send review
                </v-btn>
              </div>
              <v-carousel hide-delimiters height="235" class="videos my-8">
                <v-carousel-item
                  v-for="(item) in videos"
                  :key="item.img"
                  :src="item.img"
                >
                  <v-sheet style="text-align: center;background-color: darkslategray;color: aliceblue">
                    <span>{{ item.name }} : </span>
                    <span>{{ item.profession }}</span>
                  </v-sheet>

                  <v-icon style="top: 30%; left: 48%; background-color: darkslategray;padding: 10px;border-radius: 50%"
                          class="iconvideo">mdi-play
                  </v-icon>
                </v-carousel-item>
              </v-carousel>
              <p class="text-center">
                <v-btn style="background-color: darkslategray;color: aliceblue" class="tarif_btn"
                       :to="`${$i18n.locale}/reviews`">all
                </v-btn>
              </p>
            </v-card>
          </v-col>
        </v-row>


        <v-dialog
          v-model="dialog"
          width="500"
          persistent
        >
          <v-card
            outlined
            style="background-color: darkslategray;color: aliceblue"
          >
            <p style="background-color: aliceblue;color: darkslategray" class="text-center py-2">
              Send review
            </p>
            <!--        forms    -->
            <div class="mx-5">
              <span>Full Name</span>
              <v-text-field
                label="Full Name"
                color="white"
                solo
                outlined
                dense
              ></v-text-field>
              <span>Email</span>
              <v-text-field
                label="Email"
                color="white"
                solo
                outlined
                dense
              ></v-text-field>
              <span>Company</span>
              <v-text-field
                label="Company"
                color="white"
                solo
                outlined
                dense
              ></v-text-field>
            </div>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn style="background-color: aliceblue;color: darkslategray;border-radius: 20px"
                     @click="dialog = false">back
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn style="background-color: aliceblue;color: darkslategray;border-radius: 20px">send</v-btn>
              <v-spacer></v-spacer>
            </v-card-actions>
          </v-card>

        </v-dialog>


      </v-col>
    </v-row>
  </div>
</template>

<script>
import Modal from "@/layouts/send_modal";

export default {
  data() {
    return {
      pay_cards: [
        'https://eskiz.uz/assets/images/logo/yandex_money_en.png',
        'https://eskiz.uz/assets/images/logo/visa.png',
        'https://eskiz.uz/assets/images/logo/mastercard_en.jpg',
        'https://eskiz.uz/assets/images/logo/the_bank.png'
      ],
      videos: [
        {
          img: 'https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__340.jpg',
          name: 'Hamidullayev Fahrullo',
          profession: 'Chief editor upl.uz'
        },
        {
          img: 'https://static.toiimg.com/photo/72975551.cms',
          name: 'Konstantin Vazlin',
          profession: 'OOO Texnodor (Russia, Moscow)'
        },
        {
          img: 'https://image.shutterstock.com/image-photo/white-transparent-leaf-on-mirror-260nw-1029171697.jpg',
          name: 'Maxmudov Jaloliddin',
          profession: "Director of 'Pumpkin Web' LLC"
        }
      ],
      news: [
        {date: '20 Oct, 2019', text: "We are lunching an updated version"},
        {date: '30 Sep, 2019', text: "We are lunching an updated version"},
        {date: '10 Sep, 2019', text: "We are lunching an updated version"},
      ],
      dialog: false,
      rules: [val => (val || '').length > 0 || `${this.$t('index_page.search_requires')}`]
    }
  },
  components: {Modal},
  methods: {
    showDialog() {
      this.dialog = true
    }
  }
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

.videos:hover {
  cursor: pointer;
}
</style>
