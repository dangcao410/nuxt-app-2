<template>
  <div>
    <!--    <h1>Decks, enter number of deck to show</h1>-->

    <!--    <v-row>-->
    <!--      <v-col cols="12" sm="6">-->
    <!--        <v-text-field v-model="deckId" label="Enter Deck ID"></v-text-field>-->
    <!--      </v-col>-->
    <!--      <v-col>-->
    <!--        <v-btn @click="showDeck">Go to Deck</v-btn>-->
    <!--      </v-col>-->
    <!--    </v-row>-->
    <div class="ct">
      <h3>List of your decks</h3>

      <ul class="decks-list">
        <li>
          <div class="card deck-card">
            <img src="https://www.w3schools.com/w3css/img_lights.jpg" alt="Thumbnail card">
            <div class="card_body">
              <h3>Title card</h3>
              <p>Description card</p>
            </div>
          </div>
        </li>
        <li>
          <div class="card deck-card">
            <img src="https://www.w3schools.com/w3css/img_lights.jpg" alt="Thumbnail card">
            <div class="card_body">
              <h3>Title card</h3>
              <p>Description card</p>
            </div>
          </div>
        </li>
        <li>
          <div class="card deck-card">
            <img src="https://www.w3schools.com/w3css/img_lights.jpg" alt="Thumbnail card">
            <div class="card_body">
              <h3>Title card</h3>
              <p>Description card</p>
            </div>
          </div>
        </li>
      </ul>
    </div>
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

<style>
  .decks-list {
    list-style: none;
  }

  .decks-list li {
    margin-bottom: 1rem;
  }

  .decks-list li:last-child {
    margin-bottom: 0;
  }

  .deck-card {
    display: flex;
    flex-direction: row;
    height: 250px;
  }

  .deck-card img {
    width: 250px;
    height: auto;
  }
</style>
