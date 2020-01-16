<template>
  <div>
    <div class="card" style="width: 18rem;">
      <div class="card-body" >
        <h3 class="card-title">{{ task }}</h3>
        <buttonVote></buttonVote>
      </div>
    </div>

    <h1>HELLO WORLD</h1>
  </div>

</template>

<script>
import buttonVote from './buttonVote';

export default {
  props: [ "task" ],
  components: {
    buttonVote
  },
  methods: {
    add() {
      this.task = "aajdfajsdlf"
    }
  }
}
</script>

<style lang="css" scoped>
</style>
