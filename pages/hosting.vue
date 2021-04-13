<template>
  <div>
    <pages_header
      title="Hosting"
      text="FOR ALL TYPES OF SITES AND CMS: WORDPRESS, JOOMLA, DRUPAL, SHOPIFY AND OTHERS"
    />
    <v-row>
      <v-col md="8" offset-md="2">
        <h4 class="my-5 text-center">Tariff for hosting</h4>
        <v-btn-toggle v-model="plan1" color="#8b0000" mandatory>
          <v-btn class="button" value="plesk">
            Plesk
          </v-btn>
          <v-btn class="button" value="cpanel">
            CPanel
          </v-btn>
        </v-btn-toggle>

        <v-btn color="#8b0000" style="color: aliceblue" :to="`/${$i18n.locale}/free_hosting`">go to free hostings</v-btn>
        <br>
        <v-row class="my-10 text-center">
          <p class="text-center" v-if="selectedPlan.length === 0">no data</p>
          <v-col cols="12" md="3" sm="3" v-for="i of selectedPlan" :key="i.id">
            <v-card outlined style="border-radius: 30px">
              <h4 class="py-2" style="background-color: aquamarine;font-size: 20px">Host-{{ i.host_plan }}</h4>
              <h4 style="color: orangered;letter-spacing: 8px;transform: skew(-10deg);font-size: 30px"
                  class="font-weight-bold">{{ i.category }}</h4>
              <div class="d-flex mx-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">STORAGE</span>
                <v-spacer></v-spacer>
                <span class="text-right font-weight-bold">{{ i.storage }}</span>
              </div>
              <div class="d-flex mx-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">SITE</span>
                <v-spacer></v-spacer>
                <span class="text-right font-weight-bold">{{ i.site }}</span>
              </div>
              <div class="d-flex mx-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">DATABASE MYSQL</span>
                <v-spacer></v-spacer>
                <span class="text-right font-weight-bold">{{ i.database }}</span>
              </div>
              <div class="d-flex mx-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">MAILBOX</span>
                <v-spacer></v-spacer>
                <span class="text-right font-weight-bold">{{ i.mailbox }}</span>
              </div>
              <div class="d-flex mx-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">RAM</span>
                <v-spacer></v-spacer>
                <span class="text-right font-weight-bold">{{ i.ram }}</span>
              </div>
              <div class="d-flex px-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">DOMAIN TO GIFT *</span>
                <v-spacer></v-spacer>
                <span class="text-right font-weight-bold"><v-icon style="color: darkred">mdi-checkbox-multiple-marked-circle-outline </v-icon></span>
              </div>
              <div class="d-flex px-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">FREE SSL SERTIFICATE</span>
                <v-spacer></v-spacer>
                <span class="text-right font-weight-bold"><v-icon style="color: darkred">mdi-checkbox-multiple-marked-circle-outline </v-icon></span>
              </div>
              <div class="d-flex px-5 py-2" style="border-bottom: 1px solid antiquewhite">
                <span class="text-left">IN TAS-IX ZONE</span>
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

        <p>It is provided only when paid for a year and is valid for one year *</p>

        <h4 class="my-5">ALL RATES CONTAIN FOLLOWINGS</h4>

        <v-row class="text-center">
          <v-col cols="12" sm="4" md="4">
            <ul>
              <li><p>Control panel Cpanel</p></li>
              <li><p>PHP 7, MySQL 5.6, phpMyAdmin</p></li>
              <li><p>FTP-connect</p></li>
              <li><p>Unlimited amount FTP-accounts</p></li>
            </ul>
          </v-col>
          <v-col cols="12" sm="4" md="4">
            <ul>
              <li><p>Unlimited traffic</p></li>
              <li><p>Control CronTab (tasks on schedule)</p></li>
              <li><p>Control of DNS-records</p></li>
              <li><p>POP3, IMAP, SMTP for work with mail</p></li>
            </ul>
          </v-col>
          <v-col cols="12" sm="4" md="4">
            <ul>
              <li><p>Automatic reserve copying</p></li>
              <li><p>Control of web-server journals</p></li>
              <li><p>Operational technical support</p></li>
              <li><p>Quick and stable carrying channel</p></li>
            </ul>
          </v-col>
        </v-row>

        <share-with-friends/>

        <h2 class="text-center my-5">SUPPORT MOST POPULAR CMS</h2>
        <v-row class="my-10">
          <v-col>
            <v-img width="100" height="100" src="https://eskiz.uz/assets/images/cms/01.png"></v-img>
          </v-col>
          <v-col>
            <v-img width="100" height="100" src="https://eskiz.uz/assets/images/cms/01.png"></v-img>
          </v-col>
          <v-col>
            <v-img width="100" height="100" src="https://eskiz.uz/assets/images/cms/01.png"></v-img>
          </v-col>
          <v-col>
            <v-img width="100" height="100" src="https://eskiz.uz/assets/images/cms/01.png"></v-img>
          </v-col>
          <v-col>
            <v-img width="100" height="100" src="https://eskiz.uz/assets/images/cms/01.png"></v-img>
          </v-col>
          <v-col>
            <v-img width="100" height="100" src="https://eskiz.uz/assets/images/cms/01.png"></v-img>
          </v-col>
        </v-row>

        <hr/>

        <h2 class="text-center my-5">THE ADVANTAGE OF HOSTING FROM ESKIZ</h2>
        <v-row class="my-5">
          <v-col cols="12" md="6" sm="6">
            <p><span><v-icon>mdi-server-network</v-icon></span> Free hosting in Tas-ix for 30-days trial</p>
            <p><span><v-icon>mdi-server-network</v-icon></span> Free hosting in Tas-ix for 30-days trial</p>
            <p><span><v-icon>mdi-server-network</v-icon></span> Free hosting in Tas-ix for 30-days trial</p>
            <p><span><v-icon>mdi-server-network</v-icon></span> Free hosting in Tas-ix for 30-days trial</p>
            <p><span><v-icon>mdi-server-network</v-icon></span> Free hosting in Tas-ix for 30-days trial</p>
          </v-col>
          <v-col cols="12" md="6" sm="6">
            <p><span><v-icon>mdi-server-network</v-icon></span>Technical support in Uzbek and Russian languages</p>
            <p><span><v-icon>mdi-server-network</v-icon></span> Free hosting in Tas-ix for 30-days trial</p>
            <p><span><v-icon>mdi-server-network</v-icon></span> Free hosting in Tas-ix for 30-days trial</p>
            <p><span><v-icon>mdi-server-network</v-icon></span> Free hosting in Tas-ix for 30-days trial</p>
            <p><span><v-icon>mdi-server-network</v-icon></span> Free hosting in Tas-ix for 30-days trial</p>
          </v-col>
        </v-row>
        <h4 class="text-center">
          <v-btn color="#8b0000" class="text-center my-5" style="color: aliceblue">we are trusted</v-btn>
        </h4>

        <v-row>
          <v-col>
            <v-img width="200" height="200" src="https://eskiz.uz/uploads/clients/2.png"></v-img>
          </v-col>
          <v-col>
            <v-img width="200" height="200" src="https://eskiz.uz/uploads/clients/2.png"></v-img>
          </v-col>
          <v-col>
            <v-img width="200" height="200" src="https://eskiz.uz/uploads/clients/2.png"></v-img>
          </v-col>
          <v-col>
            <v-img width="200" height="200" src="https://eskiz.uz/uploads/clients/2.png"></v-img>
          </v-col>
          <v-col>
            <v-img width="200" height="200" src="https://eskiz.uz/uploads/clients/2.png"></v-img>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Pages_header from "../layouts/pagesHeader";
import card from "../fake_services/hosting_services.json";
import ShareWithFriends from "../layouts/shareWithFriends";

export default {
  name: "hosting",
  components: {ShareWithFriends, Pages_header},
  data: () => ({
    selectedPlan: [],
    items: [
      {text: 'for 1 month', value: '1'},
      {text: 'for 3 month', value: '3'},
      {text: 'for 6 month', value: '6'},
      {text: 'for 1 year', value: '12'}
    ],
    card: card,
    selectPlan: 1,
    valueSum: {text: 'for 1 month', value: '1'},
    plan1: "Plesk",
    plan2: "Start",
  }),
  watch: {
    "plan1"(val) {
      let array = []
      this.card.map(i => {
        if (i.category.toLowerCase() === val) {
          array.push(i)
        }
      })
      this.selectedPlan = [...array]
    },
    valueSum(value) {
      this.selectPlan = value
    }
  }
}
</script>

<style lang="scss">
.button {
  letter-spacing: 10px;
}
</style>
