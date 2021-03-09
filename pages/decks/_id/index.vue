<template>
  <section>
    <v-container>
      <h3>Deck #{{ $route.params.id }}: abc.</h3>

      <div class="tools">
        <v-btn color="success">
          Start now
        </v-btn>
        <v-btn color="primary" @click.prevent="openModal">
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

      <!-- Modal -->
      <v-modal name="CreateCardModal">
        <div class="modal_body">
          <h2>Create a new Card</h2>
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
                <v-btn color="success" @click.prevent="createCard">
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
  </section>
</template>

<script>
export default {
  // validate ({ params }) {
  //   return /^[0-9]{9,12}$/.test(params.id)
  // }
  methods: {
    openModal () {
      this.$modal.open({ name: 'CreateCardModal' })
    },
    closeModal () {
      this.$modal.close({ name: 'CreateCardModal' })
    },
    createCard () {}
  }
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

  .modal_body {
    background: #ffffff;
    padding: 1rem;
    width: 500px;
  }
</style>
