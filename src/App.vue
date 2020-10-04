<template>
  <section id="main">
    <Avatar />
    <HackerTyper>
      <h1>Hello, I'm Cameron</h1>
    </HackerTyper>
    <HackerTyper msg="A software engineering student at Lancaster University" el="p" delay="900" />
    <SocialLinks />

    <p class="title mt-4">🎧 Now playing on Spotify</p>
    <a href="https://now-playing-profile.incognitojam.vercel.app/now-playing?open">
      <img src="https://now-playing-profile.incognitojam.vercel.app/now-playing?dark=true&width=450" width="450" height="64" alt="Now playing">
    </a>
  </section>

  <section id="footer">
    <BitcoinMiner />
    <BuildTimestamp />
  </section>
</template>

<script>
import Avatar from './components/Avatar.vue';
import BitcoinMiner from './components/BitcoinMiner.vue';
import BuildTimestamp from './components/BuildTimestamp.vue';
import HackerTyper from './components/HackerTyper.vue';
import SocialLinks from './components/SocialLinks.vue';

export default {
  name: 'App',
  components: {
    Avatar,
    BitcoinMiner,
    BuildTimestamp,
    HackerTyper,
    SocialLinks,
  },
};
</script>

<style lang="scss">
#main {
  text-align: center;
}

#footer {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  margin: 12px;

  .build-timestamp {
    position: absolute;
    right: 0;
  }
}
</style>
