<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="nav">
      <q-toolbar>
        <q-toolbar-title>
          <img src="../assets/img/id-gamer.jpg" alt="id gamer" />
        </q-toolbar-title>
        <q-tabs class="navbar">
          <q-item
            v-for="link in essentialLinks"
            :key="link.title"
            clickables
            tag="a"
            target="_blank"
            :href="link.link"
          >
            <q-item-label>{{ link.title }}</q-item-label>
          </q-item>
        </q-tabs>
        <q-btn
          class="btn-menu"
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" bordered>
      <q-list>
        <q-item-label header>
          <img
            src="../assets/img/id-gamer1.jpg"
            alt="id gamer"
            class="img-logo"
          />
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import EssentialLink from 'components/EssentialLink.vue';

const linksList = [
  {
    title: 'Home',
    caption: 'Início',
    icon: '',
    link: '',
  },
  {
    title: 'Vídeo',
    caption: 'Siga Nosso Canal',
    icon: '',
    link: 'https://www.youtube.com/channel/UCP6oZeKFDzbJs-038BNYUUQ',
  },
  {
    title: 'Plataforma',
    caption: 'Todas as lives',
    icon: '',
    link: 'https://www.twitch.tv/arthur_scott',
  },
  {
    title: 'Sobre',
    caption: 'Conheça mais sobre o projeto',
    icon: '',
    link: '',
  },
];

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink,
  },

  setup() {
    const leftDrawerOpen = ref(false);
    function toggleLeftDrawer() {
      leftDrawerOpen.value = !leftDrawerOpen.value;
    }
    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer,
    };
  },
});
</script>
<style scoped>
img {
  width: 150px;
}
.img-logo {
  width: 100px;
  height: 80px;
  border-radius: 50%;
  margin: 0 25%;
}
.navbar {
  align-items: center;
  justify-content: center;
}
.nav {
  background-color: white;
  color: black;
}
.btn-menu {
  display: none;
}
@media only screen and (max-width: 800px) {
  .btn-menu {
    display: flex;
  }
  .navbar {
    display: none;
  }
}
</style>
