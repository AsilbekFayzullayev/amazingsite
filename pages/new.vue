<template>
  <div>
    <Pages_header
      title="News and Events"
      text="ALL IMPORTANT NEWS AND EVENTS OF OUR COMPANY"
    />
    <v-row class="mt-10">
      <v-col md="8" offset-md="2">
        <v-row>
          <v-col v-for="n of sliceNews" :key="n.id" cols="12" md="6" sm="6" lg="6" @click="insideNew(n)">
            <v-card outlined class="py-5 px-5 newsCard">
              <span style="background-color: darkred;color: aliceblue;border-radius: 50%"
                    class="px-2 py-1">{{ n.id }}</span>
              <span style="background-color: darkslategray; padding: 5px;color: aliceblue">{{ n.date }}</span>
              <span class="ml-4">{{ n.text }}</span>
            </v-card>
          </v-col>
        </v-row>
        <div class="text-center my-5">
          <v-pagination
            v-model="page"
            :length="Math.ceil((news.length)/10)"
            color="#033"
            circle
          ></v-pagination>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>

import Pages_header from "@/layouts/pagesHeader";
export default {
  name: "new",
  components: {Pages_header},
  data() {
    return {
      page: 1,
      sliceNews: [],
      news: [
        {
          id: 1,
          date: '20 Oct, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans, no but like",
          showDescription: false
        },
        {
          id: 2,
          date: '30 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 3,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 4,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 5,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 6,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 7,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 8,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 9,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 10,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 11,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 12,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 13,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 15,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 16,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 17,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 18,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 19,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 20,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 21,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 22,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 23,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 24,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 25,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 26,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 27,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 28,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 29,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 30,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 31,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 32,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 33,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 34,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 35,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 36,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
        {
          id: 37,
          date: '10 Sep, 2019',
          text: "We are lunching an updated version",
          description: "I am a thing. But like most politicans",
          showDescription: false
        },
      ],
    }
  },
  created() {
    this.sliceNews = this.news.slice((this.page - 1) * 10, 10)
  },
  methods:{
    insideNew(item){
      this.$router.push(`news/${item.id}`)

      this.$store.state.newItem = {...item}
    }
  },
  watch: {
    page(page) {
      const filter = this.news.slice((page - 1) * 10, page * 10)
      this.sliceNews = filter
    }
  }
}
</script>

<style scoped>
.newsCard{
  transition: all 0.3s ease-in-out;
}
.newsCard:hover{
  cursor: pointer;
  background-color: darkslategray;
  color: aliceblue;
  transform: scale(1.01);
}
</style>
