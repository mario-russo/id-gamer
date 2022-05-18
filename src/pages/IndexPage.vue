<template>
  <q-page class="row items-center justify-evenly">
    <HeroComponent></HeroComponent>
    <cardComponent></cardComponent>
    <parallax></parallax>
    <footerPage></footerPage>
  </q-page>
</template>

<script lang="ts">
import { Meta } from 'components/models';
import Hero from 'components/heroComp.vue';
import Card from 'components/cardComponent.vue';
import Parallax from 'components/parallaxComponent.vue';
import FooterPage from 'components/footerPage.vue';
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  components: {
    HeroComponent: Hero,
    cardComponent: Card,
    parallax: Parallax,
    footerPage: FooterPage,
  },
  setup() {
    const meta = ref<Meta>({
      totalCount: 1200,
    });
    return { meta };
  },
});
</script>
<style scoped>
.items-center {
  font-family: 'Open Sans', sans-serif;
  color: #333;
}
</style>
