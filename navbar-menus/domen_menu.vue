<template>
  <v-menu offset-y transition="slide-x-transition" open-on-hover>
    <template v-slot:activator="{ on, attrs }">
      <v-btn
        class="menuBtn ml-5"
        v-bind="attrs"
        v-on="on"
        dense
      >
        {{ $t('domain') }}
        <v-icon right class="iconRight">{{ icons.mdiChevronRight }}</v-icon>
      </v-btn>
    </template>
    <v-list style="padding: 10px">
      <nuxt-link :to="`/${$i18n.locale}/sale`"   class="nuxt_link">
        <v-list-item class="dropdownList">
          <v-icon class="icon" large>{{ icons.mdiSale }}</v-icon>
          <span class="iconText">{{ $t('domain_menus.textdisco') }}</span>
        </v-list-item>
      </nuxt-link>
      <nuxt-link :to="`/${$i18n.locale}/domain`"  class="nuxt_link">
        <v-list-item class="dropdownList">
          <v-icon class="icon" large>{{ icons.mdiWan }}</v-icon>
          <span class="iconText">{{ $t('domain_menus.searchdomain') }}</span>
        </v-list-item>
      </nuxt-link>
      <nuxt-link :to="`/${$i18n.locale}/transfer_domain`"  class="nuxt_link">
        <v-list-item class="dropdownList">
          <v-icon class="icon" large>{{ icons.mdiCached }}</v-icon>
          <span class="iconText">{{ $t('domain_menus.changereg') }}</span>
        </v-list-item>
      </nuxt-link>
      <nuxt-link :to="`/${$i18n.locale}/change_ownership`"  class="nuxt_link">
        <v-list-item class="dropdownList">
          <v-icon class="icon" large>{{ icons.mdiAccountSwitch }}</v-icon>
          <span class="iconText">{{ $t('domain_menus.changeowner') }}</span>
        </v-list-item>
      </nuxt-link>
    </v-list>
  </v-menu>
</template>

<script>
import {
  mdiSale,
  mdiChevronRight,
  mdiWan,
  mdiCached,
  mdiAccountSwitch
} from "@mdi/js";

export default {
  name: "domen_menu",
  data: () => ({
    icons: {
      mdiChevronRight,
      mdiSale,
      mdiWan,
      mdiCached,
      mdiAccountSwitch
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
.nuxt_link{
  text-decoration: none;
}

</style>
