<template>
  <v-app>
    <v-container fluid>
          <Navbar />
      <v-layout row justify-center>
    

        <v-main>
          <v-col md="6" offset-md="3">
            <Nuxt />
          </v-col>
        </v-main>
        
      </v-layout>
    </v-container>
  </v-app>
</template>

<script>
import Navbar from "../components/Navbar.vue";

export default {
  name: "DefaultLayout",
  components: { Navbar },
};
</script>
