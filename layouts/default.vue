<template>
  <v-app>
    <v-layout row justify-center>
      <v-main>
        <Navbar />

        <v-subheader>Today</v-subheader>
        <v-divider></v-divider>

        <v-container fluid>
          <Card />
        </v-container>

      </v-main>
    </v-layout>
  </v-app>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import Card from "../components/Card.vue";
export default {
  name: "DefaultLayout",
  components: { Navbar, Card },
};
</script>
