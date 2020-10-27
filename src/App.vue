<template>
  <section id="header">
    <BuildTimestamp />
  </section>

  <section id="main">
    <Avatar />
    <HackerTyper>
      <h1>Hello, I'm Cameron</h1>
    </HackerTyper>
    <HackerTyper msg="A software engineering student at Lancaster University" el="p" delay="900" />
    <HackerTyper msg="Working on forumm.events" el="p" delay="3400" />
    <SocialLinks />

    <p class="spotify">🎧 Now playing on Spotify</p>
    <a href="https://now-playing-profile.incognitojam.vercel.app/now-playing?open">
      <img src="https://now-playing-profile.incognitojam.vercel.app/now-playing?dark=true&width=450" width="450" height="64" alt="Now playing">
    </a>
  </section>

  <section id="footer">
    <SSHKey />
    <br />
    <BitcoinMiner />
  </section>
</template>

<script>
import Avatar from './components/Avatar.vue';
import BitcoinMiner from './components/BitcoinMiner.vue';
import BuildTimestamp from './components/BuildTimestamp.vue';
import HackerTyper from './components/HackerTyper.vue';
import SocialLinks from './components/SocialLinks.vue';
import SSHKey from './components/SSHKey.vue';

export default {
  name: 'App',
  components: {
    Avatar,
    BitcoinMiner,
    BuildTimestamp,
    HackerTyper,
    SocialLinks,
    SSHKey,
  },
};
</script>

<style lang="scss">
#header {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  margin: 12px;

  .build-timestamp {
    position: absolute;
    right: 0;
  }
}

#main {
  text-align: center;

  .spotify {
    margin-top: 64px;
  }
}

#footer {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  margin: 12px;

  .ssh-key {
    position: absolute;
    bottom: 32px;
  }
}
</style>
