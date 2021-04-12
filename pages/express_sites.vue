<template>
  <div>
    <v-tabs centered color="#033">
      <v-tab>Express Sites</v-tab>
      <v-tab>Catalog</v-tab>
      <v-tab-item>

        <pages_header
          title="Express sites"
          text="ACTIVATE A SITE FOR 4 DAYS! SINGLE PRICE – 850.000 UZS"
        />
        <v-row>
          <v-col md="6" offset-md="3">
            <v-row>
              <v-col cols="12" md="6" sm="6" class="text-center">
                <v-icon style="color: #8b0000;font-size: 200px">mdi-laptop</v-icon>
              </v-col>
              <v-col cols="12" md="6" sm="6" class="text-center">
                <p><span><v-icon color="#8B0000">mdi-check-underline-circle-outline </v-icon></span> <span>No need to prepare terms of reference</span>
                </p>
                <p><span><v-icon color="#8B0000">mdi-check-underline-circle-outline </v-icon></span> <span>No need to prepare terms of reference</span>
                </p>
                <p><span><v-icon color="#8B0000">mdi-check-underline-circle-outline </v-icon></span> <span>No need to prepare terms of reference</span>
                </p>
                <p><span><v-icon color="#8B0000">mdi-check-underline-circle-outline </v-icon></span> <span>No need to prepare terms of reference</span>
                </p>
                <p><span><v-icon color="#8B0000">mdi-check-underline-circle-outline </v-icon></span> <span>No need to prepare terms of reference</span>
                </p>
              </v-col>
            </v-row>
          </v-col>
        </v-row>

        <v-row>
          <v-col cols="12" md="12" sm="12" class="text-center">
            <h2>EXPRESS SITES</h2>
            <p>Customize any visuals, texts, menu categories and color palettes</p>
            <v-row class="px-5 my-5">
              <v-col cols="12" md="3" sm="3">
                <div class="card">
                  <v-img
                    src="https://picsum.photos/510/300?random"
                    aspect-ratio="1.7"
                  >
                    <p class="transparentColor">
                    </p>
                    <span class=" px-2 py-1 priceInCard">850000 UZS</span>
                    <p class="category px-2 py-2">
                      <span>Business</span>
                    </p>
                    <p class="viewbtn">
                      <v-btn color="#8B0000" outlined style="color: aliceblue">view</v-btn>
                    </p>
                  </v-img>
                </div>
              </v-col>
              <v-col cols="12" md="3" sm="3">
                <div class="card">
                  <v-img
                    src="https://picsum.photos/510/300?random"
                    aspect-ratio="1.7"
                  >
                    <p class="transparentColor">
                    </p>
                    <span class=" px-2 py-1 priceInCard">900000 UZS</span>
                    <p class="category px-2 py-2">
                      <span>Services</span>
                    </p>
                    <p class="viewbtn">
                      <v-btn color="#8B0000" outlined style="color: aliceblue">view</v-btn>
                    </p>
                  </v-img>
                </div>
              </v-col>
              <v-col cols="12" md="3" sm="3">
                <div class="card">
                  <v-img
                    src="https://picsum.photos/510/300?random"
                    aspect-ratio="1.7"
                  >
                    <p class="transparentColor">
                    </p>
                    <span class=" px-2 py-1 priceInCard">850000 UZS</span>
                    <p class="category px-2 py-2">
                      <span>Sport</span>
                    </p>
                    <p class="viewbtn">
                      <v-btn color="#8B0000" outlined style="color: aliceblue">view</v-btn>
                    </p>
                  </v-img>
                </div>
              </v-col>
              <v-col cols="12" md="3" sm="3">
                <div class="card">
                  <v-img
                    src="https://picsum.photos/510/300?random"
                    aspect-ratio="1.7"
                  >
                    <p class="transparentColor">
                    </p>
                    <span class=" px-2 py-1 priceInCard">850000 UZS</span>
                    <p class="category px-2 py-2">
                      <span>Legal Services</span>
                    </p>
                    <p class="viewbtn">
                      <v-btn color="#8B0000" outlined style="color: aliceblue">view</v-btn>
                    </p>
                  </v-img>
                </div>
              </v-col>
            </v-row>
            <v-btn class="my-5 buttonall" color="#8b0000" style="color: aliceblue">view all <span class="icon"><v-icon>mdi-chevron-right</v-icon></span>
            </v-btn>
            <hr>
            <h2 class="my-10">ALL EXPRESS SITES INCLUDE FOLLOWINGS</h2>
            <v-row class="text-center">
              <v-col md="8" offset-md="2">
                <v-row >
                  <v-col cols="12" md="4" sm="4" >
                    <v-card class="text-center py-2" >
                      <img src="https://eskiz.uz/assets/images/icon-domain.png" width="100" height="100" alt="">
                      <p>New domain in the .UZ zone</p>
                    </v-card>
                  </v-col>   <v-col cols="12" md="4" sm="4" >
                    <v-card class="text-center py-2" >
                      <img src="https://eskiz.uz/assets/images/icon-hosting.png" width="100" height="100" alt="">
                      <p>New domain in the .UZ zone</p>
                    </v-card>
                  </v-col>
                  <v-col cols="12" md="4" sm="4">
                    <v-card class="text-center py-2" >
                      <img src="https://eskiz.uz/assets/images/icon-email.png" width="100" height="100" alt="">
                      <p>New domain in the .UZ zone</p>
                    </v-card>
                  </v-col>
                </v-row>
                <share-with-friends />
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-tab-item>
      <v-tab-item>
        <Catalog />
      </v-tab-item>
    </v-tabs>
  </div>
</template>

<script>
import Pages_header from "../layouts/pagesHeader";
import ShareWithFriends from "../layouts/shareWithFriends";
import Catalog from "./catalog";

export default {
  name: "express_sites",
  data: () => ({}),
  components: {Catalog, ShareWithFriends, Pages_header}
}
</script>

<style scoped>
.priceInCard {
  background-color: #8b0000;
  top: 20px;
  left: 0;
  position: absolute;
  color: aliceblue;
  letter-spacing: 5px
}

.card {
  overflow: hidden;
}

.card:hover {
  cursor: pointer;

}

.category {
  transition: all .5s ease-in-out;
  position: absolute;
  width: 100%;
  height: 20%;
  bottom: 15%;
  background-color: #8b0000;
  color: aliceblue;
  letter-spacing: 5px;
}

.transparentColor {
  transition: all .5s ease-in-out;
}

.card:hover .transparentColor {
  transition: all .5s ease-in-out;
  background: rgba(139, 0, 0, .5);
  position: absolute;
  width: 100%;
  height: 100%;
}

.card:hover .category {
  height: 80%;
  transition: all .5s ease-in-out;
}

.viewbtn {
  transition: all .5s ease-in-out;
  position: absolute;
  width: 100%;
  color: aliceblue;
  opacity: 0;
  bottom: 0;
  /*display: none;*/
}

.card:hover .viewbtn {
  opacity: 1;
  transition: all .5s ease-in-out;
  bottom: 20px;
}

.icon {
  transition: all .3s ease-in-out;
}

.buttonall {
  border-radius: 20px;
}

.buttonall:hover .icon {
  margin-left: 10px;
}
</style>
