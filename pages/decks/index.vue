<template>
  <div>
    <h1>Decks, enter number of deck to show</h1>

    <v-row>
      <v-col cols="12" sm="6">
        <v-text-field v-model="deckId" label="Enter Deck ID"></v-text-field>
      </v-col>
      <v-col>
        <v-btn @click="showDeck">Go to Deck</v-btn>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data () {
    return {
      deckId: '1'
    }
  },
  methods: {
    showDeck () {
      this.$router.push(`/decks/${this.deckId}`)
    }
  }
}
</script>
