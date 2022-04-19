<template>
  <v-card flat tile>
    <v-toolbar dark height="70" color="teal lighten-3">
      <v-toolbar-title>
        <NuxtLink to="/" class="text-decoration-none">
          <v-btn text x-large> Medogem</v-btn>
        </NuxtLink>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <NuxtLink to="/news/2" class="text-decoration-none">
        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>
      </NuxtLink>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-toolbar>
  </v-card>
</template>

<script>
export default {};
</script>

<style></style>
