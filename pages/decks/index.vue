<template>
  <div>
    <div class="ct">
      <h3>List of your decks</h3>

      <ul class="decks-list">
        <li>
          <nuxt-link class="deck" to="/decks/1">
            <div class="card deck-card">
              <img src="https://www.w3schools.com/w3css/img_lights.jpg" alt="Thumbnail card">
              <div class="card_body">
                <h3>Title card</h3>
                <p>Description card</p>
              </div>
            </div>
          </nuxt-link>
        </li>
        <li>
          <nuxt-link class="deck" to="/decks/2">
            <div class="card deck-card">
              <img src="https://www.w3schools.com/w3css/img_lights.jpg" alt="Thumbnail card">
              <div class="card_body">
                <h3>Title card</h3>
                <p>Description card</p>
              </div>
            </div>
          </nuxt-link>
        </li>
        <li>
          <nuxt-link class="deck" to="/decks/3">
            <div class="card deck-card">
              <img src="https://www.w3schools.com/w3css/img_lights.jpg" alt="Thumbnail card">
              <div class="card_body">
                <h3>Title card</h3>
                <p>Description card</p>
              </div>
            </div>
          </nuxt-link>
        </li>
      </ul>
    </div>
  </div>
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

  .deck-card img {
    height: 148px;
    width: auto;
  }

  .deck {
    display: block;
  }
</style>
