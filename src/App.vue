<template>
  <v-app>
    <v-app-bar
      app
      color="black"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Arknights Logo"
          class="shrink mr-2"
          contain
          src="https://webusstatic.yo-star.com/ark_us_web/pc/img/logo02.924e2f2a.png"
          transition="scale-transition"
          height="50"
          position="left"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://docs.google.com/spreadsheets/d/e/2PACX-1vS5yhjGa6F9UtgTceIUyyqUVSzo7-JwRk3W7BfgJ4ZEikuFDVG1y_MfUic3hYn5Gdh2wymjMm_SoXfj/pubhtml#"
        target="_blank"
        text
      >
        <span class="mr-2">Lookup</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
