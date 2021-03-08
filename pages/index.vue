<template>
  <v-container>
    <div class="banner">
      <div class="thumbnail-banner">

      </div>
    </div>
    <div class="popular-decks">
      <h3>3 Popular Decks</h3>
      <v-row>
        <v-col md="4" cols="12">
          <v-card>
            Deck 1
          </v-card>
        </v-col>
        <v-col md="4" cols="12">
          <v-card>
            Deck 2
          </v-card>
        </v-col>
        <v-col md="4" cols="12">
          <v-card>
            Deck 3
          </v-card>
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>

<script>
export default {}
</script>

<style>
  .banner {
    height: 220px;
    margin-top: 2rem;
  }

  .thumbnail-banner {
    height: inherit;
    background: url("~/assets/images/banner.jpg") center center;
    background-size: cover;
  }

  .popular-decks h3 {
    text-align: center;
  }
</style>
