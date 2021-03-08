<template>
  <v-container>
    <div class="d_flex justify_content_between" style="margin: 10px;">
      <h3>List of your decks</h3>
      <v-btn color="success" @click.prevent="openModal">
        Create a Deck
      </v-btn>
    </div>
    <ul class="decks-list">
      <li>
        <nuxt-link to="/decks/1">
          <v-card class="deck-card">
            <v-row>
              <v-col md="3" cols="12">
                <img src="~/assets/images/lights.jpg" alt="Thumbnail card" height="150px" width="100%">
              </v-col>
              <v-col md="9" cols="12">
                <v-card-title>Title card</v-card-title>
                <v-card-text>Description card</v-card-text>
              </v-col>
            </v-row>
          </v-card>
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/decks/2">
          <v-card class="deck-card">
            <v-row>
              <v-col md="3" cols="12">
                <img src="~/assets/images/lights.jpg" alt="Thumbnail card" height="150px" width="100%">
              </v-col>
              <v-col md="9" cols="12">
                <v-card-title>Title card</v-card-title>
                <v-card-text>Description card</v-card-text>
              </v-col>
            </v-row>
          </v-card>
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/decks/3">
          <v-card class="deck-card">
            <v-row>
              <v-col md="3" cols="12">
                <img src="~/assets/images/lights.jpg" alt="Thumbnail card" height="150px" width="100%">
              </v-col>
              <v-col md="9" cols="12">
                <v-card-title>Title card</v-card-title>
                <v-card-text>Description card</v-card-text>
              </v-col>
            </v-row>
          </v-card>
        </nuxt-link>
      </li>
    </ul>

    <v-modal name="test">
      <div class="test_body">
        <h1>Test modal</h1>
        <v-btn color="secondary" @click.prevent="closeModal">
          Close Modal
        </v-btn>
      </div>
    </v-modal>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
    }
  },
  methods: {
    openModal () {
      this.$modal.open({ name: 'test' })
    },
    closeModal () {
      this.$modal.close({ name: 'test' })
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

<style scoped>
  .test_body {
    background: #ffffff;
    padding: 1rem;
  }
</style>
