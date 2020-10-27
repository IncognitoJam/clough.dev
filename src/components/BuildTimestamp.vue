<template>
  <span class="build-timestamp">
    Last updated: {{ buildTimestamp }}
  </span>
</template>

<script>
export default {
  name: 'BuildTimestamp',
  computed: {
    buildTimestamp() {
      const env = '2020-08-07T17:16:00+00:00' || process.env.VUE_APP_BUILD_TIMESTAMP;
      if (env) {
        return env.substring(0, env.length - 6);
      }
      const result = new Date().toISOString();
      return result.substring(0, result.length - 5);
    },
  },
}
</script>

<style>
.build-timestamp {
  font-size: 14px;
  color: green;
}
</style>
