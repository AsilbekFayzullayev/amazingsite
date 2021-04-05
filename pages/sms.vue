<template>
  <div>
    <Pages_header
      title="SMS newsletter service"
      text="SINGLE PRICE FOR SMS REGARDLESS OF THEIR AMOUNT"
    />
    <v-row>
      <v-col md="8" offset-md="2">
        <h2 class="text-center">Reliable SMS notification service in Uzbekistan</h2>
      </v-col>
    </v-row>
    <v-row style="background-color: antiquewhite" >
      <v-col md="8" offset-md="2">
        <v-row>
          <v-col class="px-10">
            <div
              class="text-center"
            >
              <v-icon color="white" class="py-10 px-10" style="background-color: darkred">mdi-email-send-outline
              </v-icon>
              <p class="px-10">
                Complete registration or restore access to users on your site via SMS
              </p>
            </div>
          </v-col>
          <v-col class="px-10">
            <div
              class="text-center"
            >
              <v-icon color="white" class="py-10 px-10" style="background-color: darkred">mdi-bell-ring-outline
              </v-icon>
              <p class="px-10">
                Remind the customer of his queue, upcoming payment or contract renewal
              </p>
            </div>
          </v-col>
          <v-col class="px-10">
            <div
              class="text-center"
            >
              <v-icon color="white" class="py-10 px-10" style="background-color: darkred">mdi-calendar-clock-outline
              </v-icon>
              <p class="px-10">
                Complete registration or restore access to users on your site via SMS
              </p>
            </div>
          </v-col>
          <v-col class="px-10">
            <div
              class="text-center"
            >
              <v-icon color="white" class="py-10 px-10" style="background-color: darkred">mdi-handshake-outline
              </v-icon>
              <p class="px-10">
                <span class="font-weight-bold">Congratulate</span> costumers with Holidays or Birthdays
              </p>
            </div>
          </v-col>
        </v-row>

        <div class="py-4 px-4 mt-16" style="position: relative;border: 2px solid darkred">
          <h4  style="background-color: antiquewhite;position: absolute;top: -10px;margin-left: 30%;margin-right: 30%">
            CONVINIENT PRICES
            ALL AROUND UZBEKISTAN
          </h4>
          <div class="text-center mt-10">
              <span v-for="btn of buttons" :key="btn.id">
                 <v-btn
                   @click="selectbtn(btn)"
                   :style="btn.isSelected ? 'background-color: darkred!important;color: aliceblue':''"
                   class="mt-10 buttons"
                   small
                 >{{ btn.text }}</v-btn>
              </span>

            <div>
              <h3 class=" my-5">{{ selectedItem.dataInside.title }}</h3>
              <span>{{ selectedItem.dataInside.text }}</span>
              <p class="mt-5"
                 style="color: darkred;cursor: pointer">
                {{ selectedItem.dataInside.span || selectedItem.dataInside.btntext }}</p>
            </div>
          </div>
        </div>
        <div class="text-center mt-4">
          <p>* the service is provided only for legal entities</p>
          <p>
            ** One SMS consists of 160 Latin and 70 Cyrillic characters
          </p>
          <p>
            *** Alpha-name approval by mobile operators takes 1-2 month
          </p>
        </div>
      </v-col>
    </v-row>

    <v-row>
      <v-col md="8" offset-md="2" class="text-center py-5">
        <span><v-icon style="color: darkred;font-size: 50px">mdi-email-mark-as-unread </v-icon></span>
        <h4 class="my-2">WAYS TO SEND SMS MESSAGES</h4>
        <hr>
        <v-row class="my-5">
          <v-col cols="12" md="6" sm="6">
            <v-card
              style="outline: 2px dotted darkred"
              height="300"
            >
              <span><v-icon color="green" style="font-size: 100px">mdi-account </v-icon></span>
              <h4 class="my-4">PERSONAL CABINET</h4>
              <hr class="mx-16">
              <p class="my-5">Simple, functional and secure personal account for SMS mailings</p>

              <v-btn style="color: darkred;background-color: transparent" class="buttons mb-5" small>Sign up</v-btn>
            </v-card>
          </v-col>
          <v-col cols="12" md="6" sm="6">
            <v-card
              style="outline: 2px dotted darkred"
              height="300"
            >
              <span><v-icon color="green" style="font-size: 100px">mdi-api </v-icon></span>
              <h4 class="my-4">Api</h4>
              <hr class="mx-16">
              <p class="my-5">Via HTTP, HTTPS protocols </p>
              <v-btn style="color: darkred;background-color: transparent" class="buttons mb-5" small>Developer's guide
              </v-btn>
            </v-card>
          </v-col>
        </v-row>

        <v-row class="mt-16">
          <v-col></v-col>
          <v-col></v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row style="background-color: antiquewhite">
      <v-col md="8" offset-md="2">
        <v-row class="text-center">
          <v-col cols="12" md="6" sm="6">
            <v-row>
              <v-col cols="12" md="12" sm="12">
                <h2 style="border-bottom: 1px solid darkred;background-color: aliceblue">OPPORTUNITIES</h2>
              </v-col>
              <v-col cols="12" md="6" sm="6">
                <p>
                  <v-icon style="font-size: 50px;color: darkred">mdi-text-box</v-icon>
                </p>
                <span>Sending SMS to more one people at the same time</span>
              </v-col>
              <v-col cols="12" md="6" sm="6">
                <p>
                  <v-icon style="font-size: 50px;color: darkred">mdi-text-box</v-icon>
                </p>
                <span>Scheduled mailings</span>
              </v-col>
              <v-col cols="12" md="6" sm="6">
                <p>
                  <v-icon style="font-size: 50px;color: darkred">mdi-text-box</v-icon>
                </p>
                <span>Editing contact lists</span>
              </v-col>
              <v-col cols="12" md="6" sm="6">
                <p>
                  <v-icon style="font-size: 50px;color: darkred">mdi-text-box</v-icon>
                </p>
                <span>Creating templates of ready messages</span>
              </v-col>

            </v-row>
          </v-col>
          <v-col cols="12" md="6" sm="6">
            <v-row>
              <v-col cols="12" md="12" sm="12">
                <h2 style="border-bottom: 1px solid darkred;background-color: aliceblue">ADVANTAGES</h2>
              </v-col>
              <v-col cols="12" md="6" sm="6">
                <p>
                  <v-icon style="font-size: 60px;color: darkred">mdi-arrow-up-bold</v-icon>
                </p>
                <span>Convenient interface</span>
              </v-col>
              <v-col cols="12" md="6" sm="6">
                <p>
                  <v-icon style="font-size: 60px;color: darkred">mdi-arrow-up-bold</v-icon>
                </p>
                <span>High speed sms mailings</span>
              </v-col>
              <v-col cols="12" md="6" sm="6">
                <p>
                  <v-icon style="font-size: 60px;color: darkred">mdi-arrow-up-bold</v-icon>
                </p>
                <span>No subscription fee</span>
              </v-col>
              <v-col cols="12" md="6" sm="6">
                <p>
                  <v-icon style="font-size: 60px;color: darkred">mdi-arrow-up-bold</v-icon>
                </p>
                <span>Support costumers</span>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-col>
    </v-row>

    <v-row>
      <v-col md="8" offset-md="2" class="text-center mt-5">
        <p>
          <v-icon style="color: darkred;font-size: 50px">mdi-email-mark-as-unread</v-icon>
        </p>
        <span
          style="border-bottom: 1px solid darkred;font-weight: bold">TYPES OF SPHEREIS THAT CAN USE SMS SENDING</span>
        <v-row class="mt-5">
          <v-col cols="12" md="3" sm="3" v-for="i of services">
            <span><v-icon style="font-size: 60px;color: darkred">{{ i.icon }}</v-icon></span>
            <p>{{ i.text }}</p>
          </v-col>
        </v-row>
      </v-col>
    </v-row>

    <v-row style="background-color: antiquewhite" class="py-5">
      <v-col md="8" offset-md="2" class="text-center">
        <span style="border-bottom: 1px solid darkred">CHOOSE US</span>
        <v-row class="mt-5">
          <v-col class="ml-10">
            <v-img width="120" height="100" src="https://eskiz.uz/assets/images/sms/clients/zebra.png"></v-img>
          </v-col>
          <v-col class="ml-10">
            <v-img width="150" height="100" src="https://eskiz.uz/assets/images/sms/clients/Assorti.png"></v-img>
          </v-col>
          <v-col class="ml-10">
            <v-img width="150" height="100" src="https://eskiz.uz/assets/images/sms/clients/Bahor.png"></v-img>
          </v-col>
          <v-col class="ml-10">
            <v-img width="150" height="100" src="https://eskiz.uz/assets/images/sms/clients/Asmald.png"></v-img>
          </v-col>
          <v-col class="ml-10">
            <v-img width="150" height="100" src="https://eskiz.uz/assets/images/sms/clients/Mato.png"></v-img>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row>
      <v-col md="8" offset-md="2">
        <share-with-friends/>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Pages_header from "../layouts/pagesHeader";
import ShareWithFriends from "../layouts/shareWithFriends";

export default {
  name: "sms",
  components: {ShareWithFriends, Pages_header},
  data: () => ({
    selectedItem: {},
    services: [
      {id: 1, icon: 'mdi-silverware', text: 'Catering'},
      {id: 2, icon: 'mdi-car', text: 'Auto'},
      {id: 3, icon: 'mdi-desktop-mac-dashboard ', text: 'E-commerce'},
      {id: 4, icon: 'mdi-school', text: 'Education'},
      {id: 5, icon: 'mdi-tools', text: 'Daily services and service'},
      {id: 6, icon: 'mdi-medical-bag', text: 'The medicine'},
      {id: 7, icon: 'mdi-alpha-f-box ', text: 'Fashion and beauty'},
      {id: 8, icon: 'mdi-alpha-t-box', text: 'Tourism'},
    ],
    buttons: [
      {
        id: 1, isSelected: true, text: "all around uzbekistan", dataInside: {
          title: 'Single price for SMS regardless of their amount and no subscription fee',
          text: "FOR 1 SMS 50 SO'M ***",
          span: 'With a monthly volume of more than 10,000 SMS, a discount is provided',
        }
      },
      {
        id: 2, isSelected: false, text: "foreign countries", dataInside: {
          title: 'INTERNATIONAL SMS NOTIFICATIONS TO FOREIGN COUNTRIES',
          text: "Send SMS from any place in the world!\n",
          btntext: 'see price >',
        }
      }
    ]
  }),
  created() {
    this.selectedItem = {...this.buttons[0]}
  },
  methods: {
    selectbtn(item) {
      this.selectedItem = {...item}
      item.isSelected = true
      this.buttons.map(m => {
        if (m.id !== item.id) {
          m.isSelected = false
        }
      })
    }
  }
}
</script>

<style scoped>
.buttons {
  border: 1px solid darkred;
  box-shadow: none;
  background-color: transparent !important;
  border-radius: 30px
}

.buttons:active {
  background-color: darkred !important;
  color: aliceblue;
}


</style>
