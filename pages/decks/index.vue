<template>
  <div>
    <h1>Decks, enter number of deck to show</h1>
    <input v-model="deckId" type="text" placeholder="Enter Deck ID">
    <button @click="showDeck">
      Go to Deck
    </button>
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
