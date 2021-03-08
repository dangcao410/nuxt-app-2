<template>
  <section>
    <v-row>
      <v-container>
        <h3>Deck #{{ $route.params.id }}: abc.</h3>

        <div class="tools">
          <button class="btn btn_success">
            Start now
          </button>
          <button class="btn btn_primary">
            Create a card
          </button>
        </div>

        <hr class="divide">

        <v-row>
          <v-col md="3" cols="12">
            <v-card>
              <div class="font-card">
                <img src="~/assets/images/deck.jpeg" alt="Thumbnail card" />
              </div>
              <div class="back-card">
              </div>
            </v-card>
          </v-col>
          <v-col md="3" cols="12">
            <v-card>
              <div class="font-card">
                <img src="~/assets/images/deck.jpeg" alt="Thumbnail card" />
              </div>
              <div class="back-card">
              </div>
            </v-card>
          </v-col>
          <v-col md="3" cols="12">
            <v-card>
              <div class="font-card">
                <img src="~/assets/images/deck.jpeg" alt="Thumbnail card" />
              </div>
              <div class="back-card">
              </div>
            </v-card>
          </v-col>
          <v-col md="3" cols="12">
            <v-card>
              <div class="font-card">
                <img src="~/assets/images/deck.jpeg" alt="Thumbnail card" />
              </div>
              <div class="back-card">
              </div>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-row>
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
  }

  .font-card img {
    height: 150px;
    width: auto;
  }
</style>
