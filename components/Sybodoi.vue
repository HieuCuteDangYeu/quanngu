<template>
  <v-container>
    <!-- v-tabs -->
    <v-tabs slider-size="0" height="67px" class="pa-20" v-model="tab">
      <v-tab class="tab mx-5 px-11 rounded-lg">Work</v-tab>
      <v-tab class="tab mx-5 px-11 rounded-lg">Hire</v-tab>
      <v-tab class="tab mx-5 px-11 rounded-lg">Both</v-tab>
    </v-tabs>

    <!-- v-tabs-items -->
    <v-tabs-items class="pt-10 pa-5" v-model="tab">
      <v-tab-item>
        <v-card class="rounded-xl">
          <v-card-title>
            <v-container class="pa-5">
              <h2>Work</h2>
              <p class=" font-weight-medium grey--text">
                Be the Architect of Your Life. Work when you want, for whom you want, and maintain your independence.
              </p>
              <v-btn elevation="2" class="warning">Learn more</v-btn>
            </v-container>
          </v-card-title>
          <v-card-text>
            <v-img src="/img/anhne1.png" alt="Image 1" class="mb-4"/>
            <v-img src="/img/anhne.png" alt="Image 2" class="mb-4"/>
          </v-card-text>
        </v-card>
      </v-tab-item>

      <v-tab-item>
        <v-card class="rounded-xl">
          <v-card-title>
            <v-container class="pa-5">
              <h2>Hire</h2>
              <p class="text-h6 font-weight-medium grey--text">
                Find and hire the best professionals for your needs.
              </p>
              <v-btn elevation="2" class="warning">Learn more</v-btn>
            </v-container>
          </v-card-title>
          <v-card-text>
            <v-img src="/img/anhne1.png" alt="Image 1" class="mb-4"/>
            <v-img src="/img/anhne.png" alt="Image 2" class="mb-4"/>
          </v-card-text>
        </v-card>
      </v-tab-item>

      <v-tab-item>
        <v-card class="rounded-xl">
          <v-card-title>
            <v-container class="pa-5">
              <h2>Both</h2>
              <p class="text-md-body-1  grey--text">
                Combine the benefits of both work and hire options.
              </p>
              <v-btn elevation="2" class="warning">Learn more</v-btn>
            </v-container>
          </v-card-title>
          <v-card-text>
            <v-img width="425" aspect-ratio="1" src="/img/anhne1.svg" alt="SVG Image"/>
            <v-img class="image" width="280" height="500" src="/img/anhne.png" alt="Image"/>
          </v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-container>
  
        
</template>

<script>
export default {
  data() {
    return {
      tab: 0 // Use 0 to initialize the first tab as active
    };
  }
};
</script>

<style>
.tab {
  border: 1px solid black;
  max-width: 300px;
}

#container-v-sheet {
  max-width: 500px;
}

.image {
  display: block;
  margin: 0 auto; 
  max-width: 100%;
}

.sy {
  border: 1px solid transparent;
  overflow: hidden;
  box-shadow: 0 2px 10px 0 #0000000f;
}
.v-application .text-h6 { font-size: 10px !important;}
</style>
