<template>
  <v-menu offset-y transition="slide-x-transition" open-on-hover>
    <template v-slot:activator="{ on, attrs }">
      <v-btn
        class="menuBtn ml-5"
        v-bind="attrs"
        v-on="on"
        dense
      >
        {{ $t('hosting') }}
        <v-icon right class="iconRight">{{ icons.mdiChevronRight }}</v-icon>
      </v-btn>
    </template>
    <v-list style="padding: 10px">
      <v-list-item class="dropdownList">
        <v-icon class="icon" large>{{ icons.mdiSale }}</v-icon>
        <span class="iconText">{{ $t('hosting_menu.textdisco') }}</span>
      </v-list-item>
      <v-list-item class="dropdownList">
        <v-icon class="icon" large>{{ icons.mdiPageNextOutline }}</v-icon>
        <span class="iconText">{{ $t('hosting_menu.sharehosting') }}</span>
      </v-list-item>
      <v-list-item class="dropdownList">
        <v-icon class="icon" large>{{ icons.mdiServerNetwork }}</v-icon>
        <span class="iconText">{{ $t('hosting_menu.vps') }}</span>
      </v-list-item>
      <v-list-item class="dropdownList">
        <v-icon class="icon" large>{{ icons.mdiServer }}</v-icon>
        <span class="iconText">{{ $t('hosting_menu.server') }}</span>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script>
import {
  mdiChevronRight,
  mdiPageNextOutline,
  mdiServerNetwork,
  mdiServer,
  mdiSale
} from "@mdi/js";

export default {
  name: "hosting_menu",
  data: () => ({
    icons: {
      mdiChevronRight,
      mdiPageNextOutline,
      mdiServerNetwork,
      mdiServer,
      mdiSale
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
</style>

