<template>
  <div>
    <pages_header
      title="Catalog"
      text="MORE THAN 100 READY WEB SITES"
    />
    <v-row>
      <v-col cols="12" md="12" sm="12" class="py-10 text-center">
        <h4>EXPRESS SITES</h4>
        <span>ACTIVATE A SITE FOR 4 DAYS! SINGLE PRICE – 850.000 UZS</span>
        <v-row class="mt-10 px-2">
          <v-col cols="12" md="2" sm="2">
            <v-card outlined style="box-shadow: 0 4px 4px grey">
              <v-list dense>
                <p class="py-2" style="background-color: lightgray">Category</p>
                <v-list-item-group
                  v-model="selected"
                >
                  <v-list-item
                    v-for="(item, i) in itemsCategory"
                    :key="i"
                    class="categoryItem"
                    @click="selectCategory(item)"
                    :style="item.isSelected ? 'background-color: darkred;color: aliceblue!important' : ''"
                  >
                    <v-list-item-content>
                      <v-list-item-title v-text="item.title" style="font-size: 15px"
                      ></v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                </v-list-item-group>
              </v-list>
            </v-card>
          </v-col>
          <v-col cols="12" md="10" sm="10">
            <v-row>
              <v-col cols="12" md="3" sm="3" v-for="item of getItems">
                <v-card outlined class="text-center itemCard">
                  <v-img :src="item.img" height="400">
                    <span class="state">{{ item.category }}</span>
                  </v-img>
                  <h4 class="mt-2">Code {{ item.code }}</h4>
                  <v-btn small class="button my-2 pl-5">more <span><v-icon
                    class="icon">mdi-chevron-right</v-icon></span></v-btn>
                </v-card>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Pages_header from "../layouts/pagesHeader";
import categoryItems from "../fake_services/category_service.json";
import items from "../fake_services/catalog_items.json"

export default {
  name: "catalog",
  components: {Pages_header},
  data: () => ({
    selected: 0,
    selectedItem: "",
    itemsCategory: categoryItems,
    itemsAll: items,
    catalogs: []
  }),
  computed: {
    getItems() {
      return this.catalogs
    }
  },
  created() {
    this.catalogs = this.itemsAll
  },
  methods: {
    async selectCategory(item) {
      this.selectedItem = item.category
      this.itemsCategory.map(i => {
        if (i.id !== item.id) {
          i.isSelected = false
        } else {
          i.isSelected = true
        }
      })
    }
  },
  watch: {
    selectedItem(item) {
      let array = []
      this.itemsAll.map(i => {
        if (item === 'all') {
          array = [...this.itemsAll]
        }
        if (i.category === item) {
          array.push(i)
        }
      })
      this.catalogs = [...array]
    }
  }
}
</script>

<style scoped>
.state {
  position: absolute;
  background-color: darkred;
  color: aliceblue;
  padding: 5px;
  letter-spacing: 5px;
  font-weight: bold;
  top: 10px;
  left: 0;
}
.button {
  background-color: darkred !important;
  color: aliceblue !important;
  border-radius: 20px;
}
.icon {
  transition: all .2s ease-in-out;
}
.button:hover .icon {
  margin-left: 5px;
}
.itemCard{
  transition: all .5s ease-in-out;
}
.itemCard:hover{
  cursor: pointer;
  box-shadow: 0 2px 4px grey;
  transform: scale(1.05);
}
.categoryItem{
  transition: all .5s ease-in-out;
}
.categoryItem:hover{
  transform: scale(1.04);
  color:aliceblue!important;
  background-color: darkred;
}
</style>
