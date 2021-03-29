<template>
  <v-menu offset-y transition="slide-x-transition" open-on-hover>
    <template v-slot:activator="{ on, attrs }">
      <v-btn
        class="menuBtn ml-5"
        v-bind="attrs"
        v-on="on"
        dense
      >
        {{ $t('website') }}
        <v-icon right class="iconRight">{{ icons.mdiChevronRight }}</v-icon>
      </v-btn>
    </template>
    <v-list style="padding: 10px">
      <nuxt-link to="/express_sites" class="nuxt_link">
        <v-list-item class="dropdownList">
          <v-icon class="icon" large>{{ icons.mdiApplication }}</v-icon>
          <span class="iconText">{{ $t('website_menu.express') }}</span>
        </v-list-item>
      </nuxt-link>
      <nuxt-link to="/exclusive_sites" class="nuxt_link">
        <v-list-item class="dropdownList">
          <v-icon class="icon" large>{{ icons.mdiViewCompactOutline  }}</v-icon>
          <span class="iconText">{{ $t('website_menu.exclusive') }}</span>
        </v-list-item>
      </nuxt-link>
    </v-list>
  </v-menu>

</template>

<script>
import {
  mdiChevronRight,
  mdiApplication,
  mdiViewCompactOutline
} from "@mdi/js";

export default {
  name: "website_menu",
  data: () => ({
    icons: {
      mdiChevronRight,
      mdiApplication,
      mdiViewCompactOutline
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
