<template>
  <div class="nav-hero">
    <!-- <h2>ID Gamer</h2>
    <p>melhor</p> -->
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
// import { Todo, Meta } from './models';

export default defineComponent({
  name: 'heroComponent',
  setup() {
    return {};
  },
});
</script>
<style scoped>
.nav-hero {
  background-image: url('../assets/img/para-hero.jpg');
  background-size: cover;
  height: 92vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  box-sizing: border-box;
  position: relative;
  font-family: 'Open Sans', sans-serif;
}
h2 {
  color: white;
}
</style>
