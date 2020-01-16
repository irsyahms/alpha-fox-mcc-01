<template>
  <button
    v-on:click="voteMe">
      VoteMe {{ click }}
  </button>
</template>

<script>
export default {
  data() {
    return {
      click: 0
    }
  },
  methods: {
    voteMe() {
      this.click += 1
    }
  }
}
</script>

<style lang="css" scoped>
</style>
