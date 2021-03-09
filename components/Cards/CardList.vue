<template>
  <v-card>
    <div class="font-card">
      <img :src="card.picture" alt="Thumbnail card" height="150px">
    </div>
    <div class="back-card text-center">
      {{ card.keyword }}
    </div>
  </v-card>
</template>

<script>
export default {
  props: ['card']
}
</script>

<style scoped>
  .font-card {
    text-align: center;
    padding: 5px;
  }

  .font-card img {
    width: 70%;
  }
</style>
