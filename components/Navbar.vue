<template>
  <v-app-bar
    :clipped-left="clipped"
    style="background-color: aliceblue;color: darkslategray; box-shadow: none;border-top: 1px solid lightgray"
    fixed
    dark
    app
  >
    <v-spacer></v-spacer>
    <v-menu offset-y transition="slide-x-transition" open-on-hover>
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          class="menuBtn"
          v-bind="attrs"
          v-on="on"
          dense
        >
          Dropdown
          <v-icon right class="iconRight">{{ icons.mdiChevronRight }}</v-icon>
        </v-btn>
      </template>

    </v-menu>
    <v-spacer></v-spacer>

  </v-app-bar>
</template>

<script>
import {mdiChevronRight} from "@mdi/js";
import {mdiHomeFloorA} from "@mdi/js";

export default {
  name: "Navbar",
  data() {
    return {
      clipped: false,
      icons: {
        mdiChevronRight,
        mdiHomeFloorA
      },
      items: [
        '1',
        '1',
        '1'
      ]
    }
  }
}
</script>

<style scoped>
.menuBtn {
  background-color: aliceblue !important;
  color: darkslategray !important;
  box-shadow: none !important;
}

.menuBtn:hover .iconRight {
  transform: rotateZ(90deg);
}
</style>
