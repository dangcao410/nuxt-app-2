<template>
  <v-container>
    <div class="" style="margin: 10px;">
      <h3 class="text-center">
        List of your decks
      </h3>
      <v-col class="text-right">
        <v-btn color="success" @click.prevent="openModal">
          Create a Deck
        </v-btn>
      </v-col>
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

    <!-- Modal-->
    <v-modal name="CreateDeckModal">
      <div class="modal_body">
        <h2>Create a new Deck</h2>
        <v-form>
          <v-text-field
            label="Name"
            required
          />
          <v-textarea
            label="Description"
            required
          />
          <v-file-input
            label="Thumbnail"
            required
          />
          <v-row>
            <v-col class="text-left" md="6" cols="12">
              <v-btn color="success" @click.prevent="createDeck">
                Create
              </v-btn>
            </v-col>
            <v-col class="text-right" md="6" cols="12">
              <v-btn color="secondary" class="text-right" @click.prevent="closeModal">
                Close
              </v-btn>
            </v-col>
          </v-row>
        </v-form>
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
      this.$modal.open({ name: 'CreateDeckModal' })
    },
    closeModal () {
      this.$modal.close({ name: 'CreateDeckModal' })
    },
    createDeck () {
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

  .modal_body {
    background: #ffffff;
    padding: 1rem;
    width: 500px;
  }
</style>
