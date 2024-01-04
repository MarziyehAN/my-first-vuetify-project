<template>
    <v-system-bar color="#1f1f1f">
      <span>Welcome to my website</span>
      <v-spacer></v-spacer>
      <v-icon icon="mdi mdi-facebook" class="ms-2"></v-icon>
      <v-icon icon="mdi mdi-linkedin" class="ms-2"></v-icon>
      <v-icon icon="mdi mdi-pinterest" class="ms-2"></v-icon>
      <v-icon icon="mdi mdi-instagram" class="ms-2"></v-icon>
      <v-icon icon="mdi mdi-youtube" class="ms-2"></v-icon>
    </v-system-bar>
 

    <v-app-bar dense floating color="#1f1f1f">
      <v-app-bar-title><h3> Dashboard</h3></v-app-bar-title>
      <v-spacer></v-spacer>
      <v-text-field hide-details label="search" density="compact" single-line
      class="mr-2">
      <template v-slot:prepend-inner>
        <v-icon x-large  color="purple">mdi-magnify</v-icon>
      </template>
      </v-text-field>
      
      <v-btn icon>
        <v-icon  color="purple">mdi-heart</v-icon>
      </v-btn>

      <v-divider vertical inset class="mx-3"></v-divider>

      <v-btn icon>
        <v-icon  color="purple">mdi mdi-lock-open-outline</v-icon>
      </v-btn>

      <v-divider vertical inset class="mx-3"></v-divider>

      <v-btn icon>
        <v-icon color="purple">mdi mdi-shopping-outline</v-icon>
      </v-btn>

      <v-divider vertical inset class="mx-3"></v-divider>

      <v-btn icon>
          <v-icon color="purple">mdi-dots-vertical</v-icon>
        </v-btn>
    </v-app-bar>
    <v-app-bar flat color="#191919">
      <v-btn variant="text" to="/">Home
        <v-menu activator="parent" transition="scale-transition"  open-on-hover>
        <v-list>
          <v-list-item
            v-for="(item, index) in items"
            :key="index"
            :value="index"
          >
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
      </v-btn>
      <v-btn variant="text" to="/vue-router">Vue-Router</v-btn>
      <v-btn variant="text">Vuex</v-btn>
      <v-btn variant="text">Vue3.js</v-btn>
      
    </v-app-bar>
    <v-tabs
      bg-color="purple"
      center-active
    >
      <v-tab>Jalpa</v-tab>
      <v-tab>LM002</v-tab>
      <v-tab>Countach</v-tab>
      <v-tab>Silhouette</v-tab>
      <v-tab>Diablo</v-tab>
      <v-tab>Murciélago</v-tab>
      <v-tab>Gallardo</v-tab>
      <v-tab>Aventador</v-tab>
      <v-tab>350 GT</v-tab>
      <v-tab>400 GT</v-tab>
      <v-tab>Miura</v-tab>
      <v-tab>Espada</v-tab>
      <v-tab>Islero</v-tab>
      <v-tab> Jarama</v-tab>
      <v-tab>Urraco</v-tab>
      <v-tab>Lamborghini</v-tab>
    </v-tabs>
  </template>
  
  
  <script>
  export default {

    data : () =>({
      items: [
        {title: 'item1'},
        {title: 'item1'},
        {title: 'item1'},
        {title: 'item1'}
      ]
    })
  }

  </script>
  
  <style>
  
  </style>