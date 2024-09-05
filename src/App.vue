<template>
  <main>
    <div>
      <button v-on:click="increment">Click {{ state.count }}</button>
      <h1>Hello</h1>
    </div>
  </main>
</template>

<script>
import { reactive } from 'vue'

export default {
  setup() {
    const state = reactive({
      count: 0
    })

    const increment = () => {
      state.count++
    }

    return {
      state,
      increment
    }
  }
}
</script>

<style scoped></style>
