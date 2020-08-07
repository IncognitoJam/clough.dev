<template>
  <div id="social-links">
    <template v-for="link in links">
      <a :href="link.url" :title="link.title">
        <svg><path :d="link.icon"/></svg>
      </a>
    </template>
  </div>
</template>

<script>
import {
  mdiEmail as Email,
  mdiGithub as GitHub,
  mdiTwitter as Twitter,
} from '@mdi/js';

export default {
  name: 'SocialLinks',
  data: () => ({
    links: [
      { title: 'GitHub', icon: GitHub, url: 'https://github.com/IncognitoJam' },
      { title: 'Twitter', icon: Twitter, url: 'https://twitter.com/cameronjclough' },
      { title: 'Email', icon: Email, url: 'mailto:cameronjclough@gmail.com' },
    ],
  }),
};
</script>

<style lang="scss">
svg {
  width: 32px;
  height: 32px;

  path {
    fill: white;
  }
}
</style>
