<template>
<v-row>
    <v-col
      v-for="(bar, i) in bars"
      :key="i"
      cols="6"
      sm="12"
      md="12"
      class="my-4"
    >
      <v-card
        color="grey-lighten-4"
        flat
        height="60px"
      >
        <v-toolbar
          :color="bar.class"
          :dark="bar.dark"
        >
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
          <v-toolbar-title>Infused Candles</v-toolbar-title>
          <v-spacer></v-spacer>
          <v-btn icon>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon>mdi-heart</v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </v-toolbar>
      </v-card>
    </v-col>
  </v-row>

  <v-carousel>
  <v-carousel-item
    src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
    cover
  ></v-carousel-item>

  <v-carousel-item
    src="https://cdn.vuetifyjs.com/images/cards/hotel.jpg"
    cover
  ></v-carousel-item>

  <v-carousel-item
    src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
    cover
  ></v-carousel-item>
</v-carousel>

<v-footer
    class="bg-grey-lighten-3 text-center d-flex flex-column"
  >
    <div>
      <v-btn
        v-for="icon in icons"
        :key="icon"
        class="mx-4"
        :icon="icon"
        variant="text"
      ></v-btn>
    </div>

    <div class="pt-0">
      Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit.
    </div>

    <v-divider></v-divider>

    <div>
      {{ new Date().getFullYear() }} — <strong>Infused Candles</strong>
    </div>
  </v-footer>

</template>
<script>
export default {
    data: () => ({
      tab: null,
      show: false,
      bars: [
        { class: 'Black', dark: true },
      ],
    }),
  }
 
</script>

