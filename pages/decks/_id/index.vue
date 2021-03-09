<template>
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
      <v-col v-for="card in cards" :key="card._id" md="3" cols="12">
        <v-card>
          <div class="font-card">
            <img :src="card.picture" alt="Thumbnail card" height="150px">
          </div>
          <div class="back-card text-center">
            {{ card.keyword }}
          </div>
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
</template>

<script>
export default {
  // validate ({ params }) {
  //   return /^[0-9]{9,12}$/.test(params.id)
  // }
  data () {
    return {
      cards: [
        {
          _id: 1,
          picture: 'https://miro.medium.com/max/10944/0*8pRlX_ascchkNaKq',
          keyword: 'Road'
        },
        {
          _id: 2,
          picture: 'https://images.unsplash.com/photo-1494548162494-384bba4ab999?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8ZGF3bnxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80',
          keyword: 'abc'
        },
        {
          _id: 3,
          picture: 'https://images.unsplash.com/photo-1494548162494-384bba4ab999?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8ZGF3bnxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80',
          keyword: 'abc'
        },
        {
          _id: 4,
          picture: 'https://images.unsplash.com/photo-1494548162494-384bba4ab999?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8ZGF3bnxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80',
          keyword: 'abc'
        },
        {
          _id: 5,
          picture: 'https://images.unsplash.com/photo-1494548162494-384bba4ab999?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8ZGF3bnxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80',
          keyword: 'abc'
        }
      ]
    }
  },
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
