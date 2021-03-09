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
      <li v-for="deck in decks" :key="deck._id">
        <DeckList :deck="deck" />
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
import DeckList from '~/components/Decks/DeckList'

export default {
  components: {
    DeckList
  },
  data () {
    return {
      decks: [
        {
          _id: 1,
          name: 'Learn English',
          description: 'Fast Track Your English Fluency. Learn to Speak English Confidently with an Expert Tutor. The Proven Way to English Fluency with Certified Tutors Rated 5* by Learners.',
          thumbnail: 'https://wallstreetenglish.edu.vn/wp-content/uploads/2020/10/logo-new.jpg'
        },
        {
          _id: 2,
          name: 'Learn English',
          description: 'Fast Track Your English Fluency. Learn to Speak English Confidently with an Expert Tutor. The Proven Way to English Fluency with Certified Tutors Rated 5* by Learners.',
          thumbnail: 'https://wallstreetenglish.edu.vn/wp-content/uploads/2020/10/logo-new.jpg'
        },
        {
          _id: 3,
          name: 'Learn English',
          description: 'Fast Track Your English Fluency. Learn to Speak English Confidently with an Expert Tutor. The Proven Way to English Fluency with Certified Tutors Rated 5* by Learners.',
          thumbnail: 'https://wallstreetenglish.edu.vn/wp-content/uploads/2020/10/logo-new.jpg'
        },
        {
          _id: 4,
          name: 'Learn English',
          description: 'Fast Track Your English Fluency. Learn to Speak English Confidently with an Expert Tutor. The Proven Way to English Fluency with Certified Tutors Rated 5* by Learners.',
          thumbnail: 'https://wallstreetenglish.edu.vn/wp-content/uploads/2020/10/logo-new.jpg'
        },
        {
          _id: 5,
          name: 'Learn English',
          description: 'Fast Track Your English Fluency. Learn to Speak English Confidently with an Expert Tutor. The Proven Way to English Fluency with Certified Tutors Rated 5* by Learners.',
          thumbnail: 'https://wallstreetenglish.edu.vn/wp-content/uploads/2020/10/logo-new.jpg'
        },
        {
          _id: 6,
          name: 'Learn English',
          description: 'Fast Track Your English Fluency. Learn to Speak English Confidently with an Expert Tutor. The Proven Way to English Fluency with Certified Tutors Rated 5* by Learners.',
          thumbnail: 'https://wallstreetenglish.edu.vn/wp-content/uploads/2020/10/logo-new.jpg'
        }
      ]
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

  .modal_body {
    background: #ffffff;
    padding: 1rem;
    width: 500px;
  }
</style>
