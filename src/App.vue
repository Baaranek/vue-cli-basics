<template>
  <h1 v-if="!isHide">Title</h1>
  <Header titleFromProps="hello" @hide="toggleTitle">
    <h1>A slot form App.vue</h1>
    <template v-slot:slotslot>
      <div>
        <p>Hello It's a slot ffrom App.vue</p>
      </div>
    </template>
  </Header>
</template>

<script>
import Header from './components/Header.vue';

export default {
  name: 'App',
  components: { Header },
  data() {
    return {
      isHide: false
    };
  },
  methods: {
    toggleTitle() {
      this.isHide = !this.isHide;
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
