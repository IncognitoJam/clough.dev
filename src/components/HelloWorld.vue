<template>
  <h1>{{ text }}</h1>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    speed: {
      type: Number,
      default: 60,
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
    this.type();
  },
};
</script>
