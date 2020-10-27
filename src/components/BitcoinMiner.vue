<template>
  <span class="bitcoin-miner" title="This isn't actually mining bitcoin">
    Bitcoin mining speed: {{ speed }}MH/s
  </span>
</template>

<script>
export default {
  name: 'BitcoinMiner',
  props: {
    interval: {
      type: Number,
      default: 1000,
    },
  },
  data: () => ({
    speed: 0,
  }),
  methods: {
    calculateSpeed() {
      this.speed = ((1 + Math.sin(Date.now())) * Math.random() * 17).toFixed(2);
    },
  },
  mounted() {
    setInterval(this.calculateSpeed, this.interval);
  },
}
</script>

<style>
.bitcoin-miner {
  font-size: 14px;
  color: green;
}
</style>
