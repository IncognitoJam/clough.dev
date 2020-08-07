<template>
  <component :is="el">{{ text }}</component>
</template>

<script>
export default {
  name: 'HackerTyper',
  props: {
    el: {
      type: String,
      default: 'span',
    },
    msg: String,
    speed: {
      type: Number,
      default: 45,
    },
    delay: {
      type: Number,
      default: 0,
    },
  },
  data() {
    return {
      text: '',
    };
  },
  methods: {
    type() {
      if (this.text.length === this.msg.length)
        return;

      this.text += this.msg[this.text.length];
      setTimeout(this.type, this.speed);
    },
  },
  mounted() {
    setTimeout(this.type, this.delay);
  },
};
</script>
