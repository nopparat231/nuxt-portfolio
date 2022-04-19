<template>
  <div class="pt-3">
    <v-subheader>Today</v-subheader>
    <v-divider class="pb-3"></v-divider>
    <div class="pb-3" v-for="(item, i) in items" :key="i">
      <v-hover v-slot="{ hover }">
        <v-card
          @click="ShowId(item.id)"
          :elevation="hover ? 12 : 2"
          class="mx-auto rounded"
          color="#F9FFFF"
        >
          <v-list-item three-line>
            <v-list-item-content>
              <div class="text-overline mb-4">
                <v-btn icon>
                  <v-icon>mdi-heart</v-icon>
                </v-btn>
                {{ item.artist }}
              </div>
              <v-list-item-title class="text-h5">
                {{ item.title }}
              </v-list-item-title>
              <v-list-item-subtitle>
                Greyhound divisely hello coldly fonwderfully
              </v-list-item-subtitle>
            </v-list-item-content>

            <v-list-item-avatar size="125" tile
              ><v-img :src="item.src"></v-img
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
    items: [
      {
        id: 1,
        color: "#1F7087",
        src: "https://cdn.vuetifyjs.com/images/cards/foster.jpg",
        title: "Supermodel",
        artist: "Foster the People",
      },
      {
        id: 2,
        color: "#952175",
        src: "https://cdn.vuetifyjs.com/images/cards/halcyon.png",
        title: "Halcyon Days",
        artist: "Ellie Goulding",
      },
      {
        id: 3,
        color: "#3892DB",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        title: "Unlimited music",
        artist: "Best airlines",
      },
    ],
  }),
  methods: {
    ShowId(id) {
      alert(id);
    },
  },
};
</script>

<style></style>
