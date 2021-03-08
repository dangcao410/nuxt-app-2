<template>
  <div class="ct">
    <div class="banner">
      <div class="thumbnail-banner">

      </div>
    </div>
    <div class="popular-decks">
      <h3 class="text_center my_3">3 Popular Decks</h3>
      <div class="r">
        <div class="c_4">
          <div class="card">
            Deck 1
          </div>
        </div>
        <div class="c_4">
          <div class="card">
            Deck 2
          </div>
        </div>
        <div class="c_4">
          <div class="card">
            Deck 3
          </div>
        </div>
      </div>
    </div>
  </div>
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
</style>
