<template>
  <v-app :style="{background:$vuetify.theme.themes.light.colors.primary}">
    <v-main>
      <NavBare/>
      <v-container fluid>
        <v-row>
          <!-- Left Panel -->
          <v-col cols="12" md="3">
            <v-expansion-panels v-model="selectedOption" >
              <v-expansion-panel  title="click here to show cars " >
                <v-expansion-panel-text>
                  <v-list lines="one">
                    <v-list-item
                    v-for="(car, index) in cars"
                      :key="index"
                      @click="selectCar(car)">
                        <div class="car-item"  style="display: flex;">
                          <v-list-item-avatar :style="{ width: '100px', heigh: '100px' }">
                          <v-img :src="car.smallImage" contain  max-height="100"  max-width="100" ></v-img>
                        </v-list-item-avatar>
                          <v-list-item-content class="ml-4 ">
                            <v-list-item-title>{{ car.name }}</v-list-item-title>
                            <v-list-item-subtitle>{{ car.model }}</v-list-item-subtitle>
                          </v-list-item-content>
                        </div>
                      </v-list-item>
                  </v-list>
                </v-expansion-panel-text>
              </v-expansion-panel>
            </v-expansion-panels>
          </v-col>

          <!-- Right Panel -->
          <v-col cols="12" md="9">
            <v-img :src="selectedCar.image" cover class="mx-auto" max-height="500"></v-img>
          </v-col>
        </v-row>

      </v-container>

    </v-main>

  </v-app>
  
</template>


<script >
 import NavBare from '@/components/NavBare.vue';
 export default {
  components: {
  NavBare,
},
data() {
    return {
      selectedOption: null,
      cars: [
        { name: 'Aventador', model: 'LP 700-4', image: 'car (1).jpg', smallImage: 'avt (3).png' },
        { name: 'Huracan', model: 'EVO', image: 'car (4).jpg', smallImage: 'avt (4).jpg' },
        { name: 'Urus', model: 'SSUV', image: 'car (5).jpg', smallImage: '6.png' }
      ],
      selectedCar: {}
    };
  },
  watch: {
    selectedOption(newVal) {
      this.selectedCar = this.cars[newVal];
    }
  },
  methods: {
    selectCar(car) {
      this.selectedCar = car;
    }
  }
};
</script>

<style>
  .changa-color:hover{
    background-color: blueviolet;
    
  }
</style>
