<template>
  <v-container>
    <h3>List of your decks</h3>

    <ul class="decks-list">
      <li>
        <nuxt-link to="/decks/1">
          <v-card class="deck-card">
            <v-row>
              <v-col md="3" cols="12">
                <v-img src="https://www.w3schools.com/w3css/img_lights.jpg" alt="Thumbnail card" height="150px" />
              </v-col>
              <v-col md="9" cols="12">
                <v-card-title>
                  Title card
                </v-card-title>
                <v-card-text>
                  Description card
                </v-card-text>
              </v-col>
            </v-row>
          </v-card>
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/decks/1">
          <v-card class="deck-card">
            <v-row>
              <v-col md="3" cols="12">
                <v-img src="https://www.w3schools.com/w3css/img_lights.jpg" alt="Thumbnail card" height="150px" />
              </v-col>
              <v-col md="9" cols="12">
                <v-card-title>
                  Title card
                </v-card-title>
                <v-card-text>
                  Description card
                </v-card-text>
              </v-col>
            </v-row>
          </v-card>
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/decks/1">
          <v-card class="deck-card">
            <v-row>
              <v-col md="3" cols="12">
                <v-img src="https://www.w3schools.com/w3css/img_lights.jpg" alt="Thumbnail card" height="150px" />
              </v-col>
              <v-col md="9" cols="12">
                <v-card-title>
                  Title card
                </v-card-title>
                <v-card-text>
                  Description card
                </v-card-text>
              </v-col>
            </v-row>
          </v-card>
        </nuxt-link>
      </li>
    </ul>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
    }
  }
}
</script>

<style scoped>
  .decks-list li {
    margin-bottom: 1rem;
  }

  .decks-list li:last-child {
    margin-bottom: 0;
  }

  .deck-card {
    display: flex;
    flex-direction: row;
    height: 150px;
  }

  h3 {
    text-align: center;
  }
</style>
