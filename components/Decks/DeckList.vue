<template>
  <nuxt-link :to="`/decks/${deck._id}`">
    <v-card class="deck-card">
      <v-row>
        <v-col md="3" cols="12">
          <img :src="deck.thumbnail" :alt="`Thumbnail of ${deck.name}`" height="150px" width="100%">
        </v-col>
        <v-col md="9" cols="12">
          <v-card-title>{{ deck.name }}</v-card-title>
          <v-card-text>{{ deck.description }}</v-card-text>
        </v-col>
      </v-row>
    </v-card>
  </nuxt-link>
</template>

<script>
export default {
  props: [
    'deck'
  ]
}
</script>

<style scoped>
  .deck-card {
    display: flex;
    flex-direction: row;
    height: 150px;
  }
</style>
