<template>
  <div modal="true">
    <div>
      <div v-if="visible" :data-modal="name" class="modal">
        <div aria-modal="true" data-reach-dialog-content="true" tabindex="-1" class="modal__mask">
          <div class="modal__body">
            <slot :payload="payload" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VModal from './handle'
export default {
  props: {
    name: {
      type: String,
      require: true
    }
  },
  data () {
    return {
      payload: null,
      visible: false
    }
  },
  beforeMount () {
    // Open event
    VModal.EventBus.$on('open', (params) => {
      if (this.name === params.name) {
        this.open(params)
      }
    })

    // Close event
    VModal.EventBus.$on('close', (params) => {
      if (this.name === params.name) {
        this.close(params)
      }
    })
  },
  methods: {
    close () {
      this.visible = false
    },
    open (params) {
      this.visible = true
      // To do something
    }
  }
}
</script>

<style scoped>
  .modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    max-width: unset;
    height: 100vh;
    overflow-y: auto;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: rgba(18, 18, 18, .8);
    z-index: 999;
    padding: 10px 0px;
  }

  /*.modal__body {*/
  /*  background: #ffffff;*/
  /*}*/
</style>
