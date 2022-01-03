<template>
  <v-app>
    <v-app-bar
      app
      color="blue darken-4 "
      dark
      class="d-flex justify-md-center align-md-center justify-end align-end"
    >
    <v-toolbar-items dark  class="hidden-xs-only" style="height:70%">
        <!-- <div class="text-center">
          <v-menu
            open-on-hover
            top
            offset-y
          >
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                color="primary"
                dark
                v-bind="attrs"
                v-on="on"
              >
                Dropdown
              </v-btn>
            </template>

            <v-list>
              <v-list-item
                v-for="(item, index) in items"
                :key="index"
              >
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </div> -->
        <!-- btn group -->
         <v-btn
           v-for="item in nav"
           :key="item.text"
           to="#"
           :title="item.title"
           depressed
           class="white--text "
           :class="item.text!=='home'?' blue darken-4':'blue accent-1'"
         >{{ item.text }}<v-icon v-if="item.text==='product'">mdi-chevron-down</v-icon>
         </v-btn>
        </v-toolbar-items> 
          <v-toolbar-items class="d-md-none d-flex justify-end align-end">
                <v-app-bar-nav-icon dark slot="activator" class="justify-self-end"></v-app-bar-nav-icon>
          </v-toolbar-items>
    </v-app-bar>
<!-- carausel -->
    <v-carousel v-model="model" cycle
    height="600" hide-delimiters :show-arrows="false">
      <v-carousel-item
        v-for="color in colors"
        :key="color"
      >
        <v-sheet
          :color="color"
          height="100%"
          tile
        >
          <v-row
            class="fill-height"
            align="center"
            justify="center"
          >

            <!-- <div class="text-h2">
              Slide {{ i + 1 }}
            </div> -->
            <v-img
            class="white--text align-end"
            height="100%"
            src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
          >
          </v-img>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
    <v-container class="d-flex align-center justify-space-between flex-wrap" >  
        <v-card
          max-width="300"
          class="xs-12 mt-4 mx-auto"
        >
          <v-img
            class="white--text align-end"
            height="200px"
            src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
          >
          </v-img>

          <v-card-title class="pb-0 text-center flex justify-center font-weight-bold">
            <p>Number 10</p>
          </v-card-title>

          <v-card-text class="text--primary text-center mx-auto mt-1">
            <div>Whitehaven Beach</div>

          </v-card-text>

          <v-card-actions class="flex justify-space-between">
            <v-btn
              class="orange accent-4 white--text"
              text
            >
              Share
            </v-btn>

            <v-btn
              class="orange accent-4 white--text"
              text
            >
              Explore
            </v-btn>
          </v-card-actions>
        </v-card>
        <v-card
          class="xs-12 mt-4 mx-auto"
          max-width="300"
        >
          <v-img
            class="white--text align-end"
            height="200px"
            src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
          >
          </v-img>

          <v-card-title class="pb-0 mx-auto flex justify-center font-weight-bold">
           <p>Number 10</p>
          </v-card-title>

          <v-card-text class="text--primary text-center mx-auto mt-1">
            <div>Whitehaven Beach</div>
          </v-card-text>

          <v-card-actions class="flex justify-space-between">
            <v-btn
              class="orange accent-4 white--text"
              text
              depressed
            >
              Share
            </v-btn>

            <v-btn
              
              class="orange accent-4 white--text"
              text
              depressed
            >
              Explore
            </v-btn>
          </v-card-actions>
        </v-card>
    </v-container>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    // HelloWorld,
  },

  data: () => ({
     nav: [
        {
          
          text: 'home',
         
        },
        {
          
          text: 'product',
          
        },
        {
         
          text: 'solution',
          
        },
        {
          text: 'support',
          
        },
        {
          text: 'contact',
          
        },
        {
          
          text: 'about',
        }
      ],
       colors: [
          '1',
          '2',
          '3',
          '4',
          '5',
        ],
        model: 0,
         items: [
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me 2' },
      ],
  }),
};
</script>

