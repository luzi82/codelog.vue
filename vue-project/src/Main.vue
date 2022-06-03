<script>
export default {
  data() {
    return {
      count: 0,
      inc: 0
    }
  },
  methods: {
    tick() {
      ++this.inc
    }
  },
  mounted() {
    this.tickTimer = setInterval(this.tick, 1000);
  },
  beforeDestroy() {
    clearInterval(this.tickTimer);
  },
}
</script>

<template>
  <button @click="count++">Count is: {{ count }}</button>
  <div>inc = {{inc}}</div>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>
