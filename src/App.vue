<template>
  <section id="main">
    <Avatar />
    <HackerTyper>
      <h1>Hello, I'm Cameron</h1>
    </HackerTyper>
    <HackerTyper msg="A software engineering student at Lancaster University" el="p" delay="900" />
    <SocialLinks />

    <p class="title mt-12">🎧 Now playing on Spotify</p>
    <a href="https://now-playing-profile.incognitojam.vercel.app/now-playing?open">
      <img src="https://now-playing-profile.incognitojam.vercel.app/now-playing?dark=true&width=450" width="450" height="64" alt="Now playing">
    </a>
  </section>

  <section id="footer">
    <BitcoinMiner />
    <BuildTimestamp />
    <v-spacer />
    <span class="caption" @click="copySSHKey">Copy SSH key</span>
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
  methods: {
    async copySSHKey() {
      await navigator.clipboard.writeText('ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCr7F7+EBogt2ELrLAbzc1IL7xORpP1XcuTz3bz+y5kW3l72sGrfFqUusc0LlpJFR3rfTLHJUpg8//iVoTHpxDDOtpAVT7j2X7G4qITllQGZz/Y3lafyipO+aw04MD06z0eSVOejlPlYrp57yMyTCTYTFuYmW4LM2ysgu8ZYdnn46zI/UdPw03jFV3NwsKtpBtr9l2HxRWrX4i7fPlaFALAdaMzILw/LTAIPd/YXP/A1/e/JJuiFDUylbY7B0ryPc54ftosF36IQncCN6kDQrmWtQyadlaJ9Yj/pEeFMGPCp1NniSUe2UPxSvTfa9bcTtn9eLA1k+2egFYvpiuE570IdW/yi/+LvAsSdlAcC7bspdL2IBzNxDfgBHYx0jogUqkv5KUQ6pA1OlrDcWM0W/ZGjkQWEeeuCRNVxz3YSQUtunUU45O6gZuxpOaCMCNN7aNhnm3Cr0sgT2snkj4YoejIK+GPdxCFlVPwEHA2Pvt28UcTHdvgQOK5KXBrrikJZWc= Pixel4XL');
    }
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
