<template>
  <div>
    <v-app-bar
      color="surface"
      height="80"
      class="el"
      :style="{
        padding: $vuetify.breakpoint.mdAndUp ? '0px 100px' : '',
      }"
      app
    >
      <v-toolbar-title
        @click="$router.push('/')"
        class="text-md-h5 font-weight-bold pointer"
        >VueJS e-Commerce</v-toolbar-title
      >
      <v-spacer />

      <v-btn nuxt to="/products" class="mr-md-2" icon>
        <v-icon size="20">mdi-store-outline</v-icon>
      </v-btn>


      <v-divider vertical class="mx-md-5 mx-2" />
      <v-btn @click="toggleTheme" icon>
        <v-icon size="20">mdi-brightness-7</v-icon>
      </v-btn>
    </v-app-bar>
  </div>
</template>

<script>

</script>

<style></style>
