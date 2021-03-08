<template>
  <section>
    <v-container>
      <h3>Deck #{{ $route.params.id }}: abc.</h3>

      <div class="tools">
        <v-btn color="success">
          Start now
        </v-btn>
        <v-btn color="primary">
          Create a card
        </v-btn>
      </div>

      <hr class="divide">

      <v-row>
        <v-col md="3" cols="12">
          <v-card>
            <div class="font-card">
              <img src="~/assets/images/deck.jpeg" alt="Thumbnail card">
            </div>
            <div class="back-card" />
          </v-card>
        </v-col>
        <v-col md="3" cols="12">
          <v-card>
            <div class="font-card">
              <img src="~/assets/images/deck.jpeg" alt="Thumbnail card">
            </div>
            <div class="back-card" />
          </v-card>
        </v-col>
        <v-col md="3" cols="12">
          <v-card>
            <div class="font-card">
              <img src="~/assets/images/deck.jpeg" alt="Thumbnail card">
            </div>
            <div class="back-card" />
          </v-card>
        </v-col>
        <v-col md="3" cols="12">
          <v-card>
            <div class="font-card">
              <img src="~/assets/images/deck.jpeg" alt="Thumbnail card">
            </div>
            <div class="back-card" />
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  // validate ({ params }) {
  //   return /^[0-9]{9,12}$/.test(params.id)
  // }
}
</script>

<style scoped>
  section {
    padding-top: 3rem;
  }

  .divide {
    margin: 2rem 0;
  }

  .font-card {
    text-align: center;
    padding: 5px;
  }

  .font-card img {
    width: 70%;
  }

  h3, .tools {
    text-align: center;
  }
</style>
