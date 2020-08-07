<template>
  <Avatar />
  <HelloWorld msg="Hello, I'm Cameron" />
  <SocialLinks />
  <span class="timestamp">Last updated: {{ buildTimestamp }}</span>
</template>

<script>
import Avatar from './components/Avatar.vue';
import HelloWorld from './components/HelloWorld.vue';
import SocialLinks from './components/SocialLinks.vue';

export default {
  name: 'App',
  components: {
    Avatar,
    HelloWorld,
    SocialLinks,
  },
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
};
</script>

<style lang="scss">
.timestamp {
  font-size: 14px;
  position: absolute;
  bottom: 12px;
  right: 12px;
}
</style>
