<template>
  
  <v-row>
    <v-col
      v-for="(bar, i) in bars"
      :key="i"
      cols="12"
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

  <!-- taps for categories -->

  <v-card>
    <v-tabs
      v-model="tab"
      color="deep-grey-lighten-4"
      align-tabs="center"
    >
      <v-tab :value="1">Sented Candles</v-tab>
      <v-tab :value="2">Glass jar</v-tab>
      <v-tab :value="3">Decor</v-tab>
    </v-tabs>
    <v-window v-model="tab">
      <v-window-item
        v-for="n in 3"
        :key="n"
        :value="n"
      >
        <v-container fluid>
          <v-row>
            <v-col
              v-for="i in 6"
              :key="i"
              cols="12"
              md="4">     

            <v-card
                class="mx-auto"
                max-width="344"
            >
            <v-img
            src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
            height="200px"
            cover
            ></v-img>

            <v-card-title>
            Top western road trips
            </v-card-title>

            <v-card-subtitle>
            1,000 miles of wonder
            </v-card-subtitle>

            <v-card-actions>
                <v-dialog width="500">
            <template v-slot:activator="{ props }">
                <v-btn v-bind="props" text="View Details"> </v-btn>
            </template>

            <template v-slot:default="{ isActive }">
                <v-card title="Dialog">
                <v-card-text>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                </v-card-text>

                <v-card-actions>
                    <v-spacer></v-spacer>

                    <v-btn
                    text="Close Dialog"
                    @click="isActive.value = false"
                    ></v-btn>
                </v-card-actions>
                </v-card>
            </template>
            </v-dialog>
            <v-spacer></v-spacer>

            <v-btn
                :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'"
                @click="show = !show"
            ></v-btn>
            </v-card-actions>

            <v-expand-transition>
            <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
                </v-card-text>
            </div>
            </v-expand-transition>
            </v-card>
            </v-col>
          </v-row>
        </v-container>
      </v-window-item>
    </v-window>
  </v-card>

  <!-- footer section start here -->

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
