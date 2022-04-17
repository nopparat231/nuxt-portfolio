<template>
  <v-row>
    <v-col
      md="6"
      class="pl-6 pr-6"
      offset-md="3"
      v-for="(item, i) in items"
      :key="i"
    >
      <v-hover v-slot="{ hover }" disabled>
        <v-card
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
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        color: "#1F7087",
        src: "https://cdn.vuetifyjs.com/images/cards/foster.jpg",
        title: "Supermodel",
        artist: "Foster the People",
      },
      {
        color: "#952175",
        src: "https://cdn.vuetifyjs.com/images/cards/halcyon.png",
        title: "Halcyon Days",
        artist: "Ellie Goulding",
      },
      {
        color: "#3892DB",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        title: "Unlimited music",
        artist: "Best airlines",
      },
    ],
  }),
};
</script>

<style></style>
