<template>
  <div class="pt-3">
    <v-subheader>Today</v-subheader>
    <v-divider class="pb-3"></v-divider>
    <div class="pb-3" v-for="(item, i) in news" :key="i">
      <v-hover v-slot="{ hover }">
        <v-card
          :elevation="hover ? 12 : 2"
          class="mx-auto rounded"
          color="#F9FFFF"
        >
          <v-list-item three-line>
            <v-list-item-content>
              <div class="text-overline mb-4">
                <v-btn icon>
                  <v-icon>mdi-heart-outline</v-icon>
                </v-btn>
                {{ item.source.name }}
              </div>
              <v-list-item-title class="text-h5">
                <a :href="item.url" target="_blank"  >{{ item.title }}</a>
              </v-list-item-title>
              <v-list-item-subtitle>
                {{ item.description }}
              </v-list-item-subtitle>
            </v-list-item-content>

            <v-list-item-avatar size="125" tile
              ><v-img :src="item.urlToImage"></v-img
            ></v-list-item-avatar>
          </v-list-item>
        </v-card>
      </v-hover>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    news: [],
  }),
  methods: {
    ShowId(id) {
      alert(id);
    },
  },
  async created() {
    const url =
      "https://newsapi.org/v2/top-headlines/?" +
      "country=th&" +
      "apiKey=00f58deabf7c48e58244c46bbdd8ccaf";
    const news = await this.$axios.$get(url);
    this.news = news.articles;
  },
};
</script>

<style></style>
