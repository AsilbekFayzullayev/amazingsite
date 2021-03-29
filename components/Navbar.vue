<template>
  <v-app-bar
    :clipped-left="clipped"
    style="background-color: aliceblue;color: darkslategray; box-shadow: 0 4px 5px darkslategray;border-top: 1px solid lightgray"
    fixed
    dark
    app
  >
    <v-spacer></v-spacer>
    <v-btn icon :to="`/${$i18n.locale}`">
      <v-icon class="icon" large style="">{{ icons.mdiHomeFloorA }}
      </v-icon>
    </v-btn>

    <domen_menu/>
    <hosting_menu/>
    <ssl_menu/>

    <v-btn class="btn ml-5" :to="`/${$i18n.locale}/mail`">
      {{ $t('mail') }}
    </v-btn>
    <website_menu />
    <v-btn class="btn ml-5" :to="`/${$i18n.locale}/sms`">
      {{ $t('sms') }}
    </v-btn>
    <v-btn class="btn ml-5" :to="`/${$i18n.locale}/reseller`">
      {{ $t('partner') }}
    </v-btn>

    <v-spacer></v-spacer>

  </v-app-bar>
</template>

<script>
import {mdiHomeFloorA} from "@mdi/js";
import Domen_menu from "@/navbar-menus/domen_menu";
import Hosting_menu from "@/navbar-menus/hosting_menu";
import Ssl_menu from "@/navbar-menus/ssl_menu";
import Website_menu from "@/navbar-menus/website_menu";

export default {
  name: "Navbar",
  components: {Website_menu, Ssl_menu, Hosting_menu, Domen_menu},
  data() {
    return {
      clipped: false,
      icons: {
        mdiHomeFloorA
      }
    }
  }
}
</script>

<style scoped>
.icon {
  transition: all .5s ease-in-out;
  color: darkslategray !important;
}

.icon:hover {
  background-color: darkslategray;
  color: aliceblue !important;
  border-radius: 50%;
}

.btn {
  transition: all .5s ease-in-out;
  background-color: aliceblue !important;
  color: darkslategray;
  box-shadow: none;
}

.btn:hover {
  background-color: darkslategray !important;
  color: aliceblue;
}
</style>
