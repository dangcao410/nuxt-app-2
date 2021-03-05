<template>
  <h1>Deck {{ $route.params.id }}</h1>
</template>

<script>
export default {
  validate ({ params }) {
    return /^[0-9]{9,12}$/.test(params.id)
  }
}
</script>
