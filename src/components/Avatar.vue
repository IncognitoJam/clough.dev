<template>
  <div id="avatar" />
</template>

<script>
export default {
  name: 'Avatar',
};
</script>

<style lang="scss">
#avatar {
  border: 4px solid #4dd05b;
  border-radius: 50%;
  height: 10em;
  width: 10em;
  margin: 2em auto;

  background-image: url('/keith.webp');
  background-repeat: no-repeat;
  background-size: cover;
  -webkit-transition: background .2s;
  -moz-transition: background .2s;
  -o-transition: background .2s;
  transition: background .2s;
}

#avatar:hover {
  background-image: url('/keith2.webp');
}
</style>
