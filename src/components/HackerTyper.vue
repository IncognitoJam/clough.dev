<template>
  <span class="hacker-typer">
    <component :is="tag">{{ text }}</component>
  </span>
</template>

<script>
export default {
  name: 'HackerTyper',
  props: {
    speed: {
      type: Number,
      default: 45,
    },
    delay: {
      type: Number,
      default: 0,
    },
    msg: String,
  },
  data() {
    return {
      tag: 'h5',
      target: '',
      text: '',
    };
  },
  methods: {
    type() {
      if (this.text.length === this.target.length)
        return;

      this.text += this.target[this.text.length];
      setTimeout(this.type, this.speed);
    },
  },
  mounted() {
    console.log('');
    console.log(typeof this.$slots.default);
    if (typeof this.$slots.default !== 'function') {
      this.target = this.msg;
    } else {
      console.log(this.$slots.default()[0]);
      const slot = this.$slots.default()[0];
      this.tag = slot.type;
      this.target = slot.children;
    }
    setTimeout(this.type, this.delay);
  },
};
</script>
