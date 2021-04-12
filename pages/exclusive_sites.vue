<template>
  <div>
    <pages_header
      title="Exclusive sites"
      text="CREATIVE APPROACH!"
    />
    <v-row>
      <v-col md="6" offset-md="3" class="text-center">
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
        <h2 class="my-5">OFFERING NEWLY DEVELOPED SITES</h2>
        <p>
          If you need totally unique, thematic sites, online stores or any other websites, we may offer you to develop
          it from scratch: designing and making it up in pages, from integration of CMS with desktop and mobile versions
          to registering a domain, installing it in our hosting.

          Cost of these sites starts from 3 million soums due to the structure, design and required functionality,
          complexity of the CMS system. According to your desire,while developing a site, we can use systems like
          1C-Bitrix or our own thoroughly developed system Eskiz CMS .

          According to the general complexity, web development may take about more than 3 weeks.

          On your request, you can transfer the developed website to any other hosting
        </p>
      </v-col>
    </v-row>
    <hr>

    <v-row>
      <v-col md="6" offset-md="3" class="text-center">
        <h2 class="my-10">EXCLUSIVE SITES</h2>
        <v-row>
          <div v-for="n of 8" :key="n">
            <v-img src="https://picsum.photos/200/300" width="300" height="300" alt="" class="image">
              <div class="site">
                <p class="text">NAC Uzbekistan airwaysNational </p>
                <v-btn class="btnsite" outlined color="white">site</v-btn>
              </div>
            </v-img>
          </div>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Pages_header from "../layouts/pagesHeader";

export default {
  name: "exclusive_sites",
  components: {Pages_header},
  data: () => ({
    sites: []
  })
}
</script>

<style scoped>
.site {
  left: -500px;
  position: absolute;
  padding-top: 150px;
  color: aliceblue;
  width: 100%;
  height: 100%;
  background: rgba(139, 0, 0, 0.5);
  transition: all 0.4s ease-in-out;
}

.text {
  top: 80px;
  position: absolute;
  width: 100%;
  height: 100%;
}

.image:hover .site {
  left: 0;
}

.btnsite {
  transition: all .3s ease-in-out;
  background-color: transparent !important;
}
.btnsite:hover{
  background-color: antiquewhite!important;
  color: darkred!important;
}
</style>
