<template>
  <section>
    <div class="r">
      <div class="ct text_center">
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
        <div class="r">
          <div class="c_3">
            <div class="card">
              <div class="font-card">
                <img src="https://images.unsplash.com/photo-1494548162494-384bba4ab999?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1100&q=80" alt="Thumbnail card">
              </div>
              <div class="back-card">
              </div>
            </div>
          </div>
          <div class="c_3">
            <div class="card">
              <div class="font-card">
                <img src="https://images.unsplash.com/photo-1494548162494-384bba4ab999?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1100&q=80" alt="Thumbnail card">
              </div>
              <div class="back-card">
              </div>
            </div>
          </div>
          <div class="c_3">
            <div class="card">
              <div class="font-card">
                <img src="https://images.unsplash.com/photo-1494548162494-384bba4ab999?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1100&q=80" alt="Thumbnail card">
              </div>
              <div class="back-card">
              </div>
            </div>
          </div>
          <div class="c_3">
            <div class="card">
              <div class="font-card">
                <img src="https://images.unsplash.com/photo-1494548162494-384bba4ab999?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1100&q=80" alt="Thumbnail card">
              </div>
              <div class="back-card">
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
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

  .card {
    padding: 1rem;
  }

  .card img {
    width: 60%;
  }
</style>
