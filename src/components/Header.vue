<template>
  <h2>{{ titleSecond }}</h2>
  <h3>{{ titleThird }}</h3>
  <h4 @click="hideTitle">{{ titleFromProps }}</h4>
  <slot></slot>
  <slot name="slotslot"></slot>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      titleSecond: 'Title Two',
      titleThird: 'Title Three'
    };
  },
  props: ['titleFromProps'],
  methods: {
    hideTitle() {
      this.$emit('hide');
    }
  }
};
</script>
