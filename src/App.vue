<template>
  <Avatar />
  <HelloWorld msg="Hello, I'm Cameron" />
</template>

<script>
import Avatar from './components/Avatar.vue';
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    Avatar,
    HelloWorld,
  },
};
</script>
