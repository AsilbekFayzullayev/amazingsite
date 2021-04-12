<template>
  <v-menu offset-y transition="slide-x-transition" open-on-hover>
    <template v-slot:activator="{ on, attrs }">
      <v-btn
        class="menuBtn ml-5"
        v-bind="attrs"
        v-on="on"
        dense
      >
        {{ $t('ssl') }}
        <v-icon right class="iconRight">{{ icons.mdiChevronRight }}</v-icon>
      </v-btn>
    </template>
    <v-list style="padding: 10px">
      <nuxt-link :to="`/${$i18n.locale}/sale`" class="nuxt_link">
        <v-list-item class="dropdownList">
          <v-icon class="icon" large>{{ icons.mdiSale }}</v-icon>
          <span class="iconText">{{ $t('ssl_menu.textdisco') }}</span>
        </v-list-item>
      </nuxt-link>
      <nuxt-link :to="`/${$i18n.locale}/ssl_certificate`" class="nuxt_link">
        <v-list-item class="dropdownList">
          <v-icon class="icon" large>{{ icons.mdiDomain }}</v-icon>
          <span class="iconText">{{ $t('ssl_menu.domen') }}</span>
        </v-list-item>
      </nuxt-link>
      <nuxt-link :to="`/${$i18n.locale}/subdomain`" class="nuxt_link">
        <v-list-item class="dropdownList">
          <v-icon class="icon" large>{{ icons.mdiDomain }}</v-icon>
          <span class="iconText">{{ $t('ssl_menu.subdomen') }}</span>
        </v-list-item>
      </nuxt-link>
      <nuxt-link :to="`/${$i18n.locale}/certificate_company_name`" class="nuxt_link">
        <v-list-item class="dropdownList">
          <v-icon class="icon" large>{{ icons.mdiDomain }}</v-icon>
          <span class="iconText">{{ $t('ssl_menu.namecompany') }}</span>
        </v-list-item>
      </nuxt-link>
    </v-list>
  </v-menu>
</template>

<script>
import {mdiChevronRight, mdiSale, mdiDomain} from "@mdi/js";

export default {
  name: "ssl_menu",
  data: () => ({
    icons: {
      mdiChevronRight,
      mdiSale,
      mdiDomain
    },
  })
}
</script>

<style scoped>
.menuBtn {
  transition: all 0.5s ease-in-out;
  background-color: aliceblue !important;
  color: darkslategray !important;
  box-shadow: none !important;
}

.menuBtn:hover {
  background-color: darkslategray !important;
  color: aliceblue !important;
}

.menuBtn:hover .iconRight {
  transform: rotateZ(90deg);
}

.dropdownList:hover {
  cursor: pointer;
  background-color: darkslategray;
}

.dropdownList:hover {
  transition: all 0.5s ease-in-out;
}

.iconText {
  color: darkslategray;
  margin: 0 12px;
}

.icon {
  color: darkslategray;
}

.dropdownList:hover .iconText {
  color: aliceblue;
}

.dropdownList:hover .icon {
  color: aliceblue;
}

.nuxt_link {
  text-decoration: none;
}
</style>

