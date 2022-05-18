<template>
  <q-parallax class="parallax">
    <template v-slot:media>
      <img src="../assets/img/parallax.jpg" />
    </template>
    <h4 class="text-white">Arthur Scott comanda as lives na Twitch!</h4>
  </q-parallax>
  <section class="divisao">
    <div class="card-social">
      <h4>Youtube</h4>
      <p>
        Vídeo novo no canal toda semana. Dicas de varios jogos diferente,
        tutorias, e lives de todos os tipos de jogos.
      </p>
    </div>
    <div class="card-social">
      <h4>FaceBook</h4>
      <p>Aqui você varios conteúdo das principais plataforma de streaming</p>
    </div>
    <div class="card-social">
      <h4>Twitch</h4>
      <p>
        Na Twitch os jogos são diversos, desde de RPG até SHOOTER. alguns jogos
        com CS:GO, Apex Legends, Warface, S.T.A.L.L.K.E.R Destiny 2. Arthur
        Scott comanda as lives na Twitch! .
      </p>
    </div>
  </section>
  <q-parallax class="parallax">
    <template v-slot:media>
      <img src="../assets/img/parallax2.jpg" />
    </template>
  </q-parallax>
</template>
<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  setup() {
    return {};
  },
});
</script>
<style scoped>
.parallax {
  margin-top: 15px;
}
.divisao {
  height: 50vh;
  width: 80%;
  margin: auto;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.card-social {
  width: 32%;
  /* background-color: beige; */
  height: 300px;
  border-radius: 10px;
  padding: 10px;
  transform: 0.5ms;
}
.card-social:hover {
  box-shadow: 2px 2px 2px 4px rgba(0, 0, 0, 0.1);
}
</style>
