<template>
<div>
  <v-system-bar
    style="color: black; background-color: aliceblue; font-weight: bold!important"
    height="100"
    app
    window
  >
    <v-spacer></v-spacer>
    <div style="color: darkslategray" class="mr-5">
      <h2>Zuccotech</h2>
      <span class="ml-5">IT company</span>
    </div>

    <div class="ml-5 mt-2" style="width: 200px; color: darkslategray">
      <p class="my-4">{{ $t('net') }}</p>
    </div>

    <div class="mx-5" style="color: darkslategray">
      <p style="margin-bottom: 0">
        <phone-icons fill-color="darkslategrey" class="mr-2"/>
        +99891 257 17 70
      </p>
      <p style="margin-bottom: 0" class="telegramUrl">
        <telegram-icons fill-color="darkslategrey" class="mr-2"/>
        @zuccotech
      </p>
    </div>
    <v-btn :to="`/${$i18n.locale}/sale`" style="color: darkslategray;border-radius: 15px" class="aksiyaBtn mr-5" outlined>
      {{ $t('discount') }}
    </v-btn>
    <div style="align-items: center;display: flex; cursor: pointer">
      <password-icons fill-color="darkslategrey"/>
      <div class="ml-4 mt-4">
        <span style="color: darkslategray">{{ $t('cabinet') }}</span>
        <p>{{ $t('panel') }} </p>
      </div>
    </div>
    <div class="mx-5 mt-5">
      <v-select
        :items="items"
        style="width: 90px;color: darkslategray!important;border-radius: 20px"
        v-model="lang"
        outlined
        dense
      ></v-select>
    </div>

    <v-spacer></v-spacer>

  </v-system-bar>
<!--  <v-navigation-drawer-->
<!--    style="z-index: 1000"-->
<!--    v-model="drawer"-->
<!--    :clipped="true"-->
<!--    fixed-->

<!--  >-->
<!--    <v-list>-->
<!--      <v-list-item-->
<!--        v-for="(item) in items"-->
<!--        :key="item"-->
<!--        router-->
<!--        exact-->
<!--      >-->

<!--        <v-list-item-action>-->
<!--        </v-list-item-action>-->
<!--        <v-list-item-content>-->
<!--          <v-list-item-title v-text="item" />-->
<!--        </v-list-item-content>-->
<!--      </v-list-item>-->
<!--    </v-list>-->
<!--  </v-navigation-drawer>-->
</div>
</template>

<script>
import img from "static/Screenshot (22).png";
import PhoneIcons from "vue-material-design-icons/Phone.vue"
import TelegramIcons from "vue-material-design-icons/Telegram.vue"
import PasswordIcons from "vue-material-design-icons/Lock.vue"


export default {
  name: "Header",
  data() {
    return {
      clipped: true,
      drawer: true,
      fixed: false,
      img: img,
      lang: this.$i18n.locale,
      items: [
        'en', 'uz', 'ru'
      ]
    }
  },
  components: {
    PhoneIcons,
    TelegramIcons,
    PasswordIcons
  },
  watch: {
    lang(lang) {
      this.$router.push(this.switchLocalePath(`${lang}`)
      )
    }
  }
}
</script>

<style scoped>
.telegramUrl {
  cursor: pointer;
}

.aksiyaBtn {
  margin: 0 15px;
  transform: scale(1);
  transition: all .4s ease-in-out;
}

.aksiyaBtn:hover {
  transform: scale(1.05);
  box-shadow: 0 2px 4px gray;
  background-color: darkslategray;
  color: white !important;
  border: none;
}

</style>
