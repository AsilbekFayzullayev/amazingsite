<template>
  <div>
    <Pages_header
      title="Video reviews"
      text="About our service"
    />
    <v-row class="mt-10">
      <v-col md="8" offset-md="2">
        <v-row>
          <v-col cols="12" md="4" sm="4" v-for="(item,i) of videos" :key="i">
            <v-card outlined class="py-4 px-4 text-center" style="cursor: pointer;" @click="clickPlay(item)">
              <v-img :src="item.img">
                <v-row>
                  <v-col md="6" offset-md="3" class="text-center my-15 py-15">
                    <v-icon
                      style="color: aliceblue; background-color: darkslategray;padding: 10px;border-radius: 50%"
                    >mdi-play
                    </v-icon>

                  </v-col>
                </v-row>
              </v-img>
              <h2 style="color: darkred">{{ item.name }}</h2>
              <span>{{ item.profession }}</span>
            </v-card>
          </v-col>
        </v-row>
        <ShareWithFriends/>
      </v-col>
    </v-row>

    <!--    video dialog-->
    <v-dialog
      v-model="dialogvideos"
      width="500"
      persistent
    >
      <v-card
        outlined
        style="background-color: darkslategray;color: aliceblue"
      >
        <v-card-actions>
          <span>{{ selectedVideo.name }} : </span>
          <span class="mx-5">{{ selectedVideo.profession }}</span>
          <v-spacer></v-spacer>
          <v-btn style="background-color: aliceblue;color: darkslategray;border-radius: 20px"
                 @click="dialogvideos = false"
                 icon
          >
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-card-actions>
        <iframe width="100%" height="400" :src="selectedVideo.src"
                class="px-2"
                title="YouTube video player" frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen></iframe>

      </v-card>

    </v-dialog>

  </div>
</template>
<script>
import Pages_header from "@/layouts/pagesHeader";
import ShareWithFriends from "@/layouts/shareWithFriends";

export default {
  name: "reviews",
  data: () => ({
    dialogvideos: false,
    selectedVideo: {},
    videos: [
      {
        img: 'https://eskiz.uz/uploads/reviews/1_11337a078c5ccf2fc0dd27a4aead088c.jpg',
        name: 'Hamidullayev Fahrullo',
        profession: 'Chief editor upl.uz',
        src: 'https://www.youtube.com/embed/IQw-4JABPCM'
      },
      {
        img: 'https://eskiz.uz/uploads/reviews/3_316d230e03f37a8704e34d4dc3e29766.jpg',
        name: 'Konstantin Vazlin',
        profession: 'OOO Texnodor (Russia, Moscow)',
        src: 'https://www.youtube.com/embed/FWQSuskE5UA'
      },
      {
        img: 'https://eskiz.uz/uploads/reviews/4_7e4f481787a51b99062a9f3efd89ea59.jpg',
        name: 'Maxmudov Jaloliddin',
        profession: "Director of 'Pumpkin Web' LLC",
        src: 'https://www.youtube.com/embed/0wHyoBPc6zs'

      }
    ],
  }),
  methods: {
    clickPlay(item) {
      this.dialogvideos = true
      this.selectedVideo = {...item}

    }
  },
  components: {ShareWithFriends, Pages_header},
}
</script>

<style scoped>

</style>
