<template>
  <div class="card-container">
    <div class="titulo">
      <span class="line"></span>
      <h3>Stalker</h3>
      <span></span>
    </div>
    <q-card class="my-card">
      <q-img class="img-1">
        <div class="absolute-bottom text-h6">
          S.T.A.L.K.E.R.: CALL OF Pripyat
        </div>
      </q-img>

      <q-card-section>
        O terceiro jogo da série, Call of Pripyat acontece logo após os eventos
        de Shadow of Chernobyl. Tendo descoberto o caminho aberto para o centro
        da Zona, o governo decide controlá-lo através da "Operação Fairway"
      </q-card-section>
      <q-separator />
      <q-card-actions>
        <q-btn
          flat
          outline
          target="_blanck"
          href="https://www.youtube.com/watch?v=QsaeSP8fqrg&list=PLa2rM52nzkHGJ8DUDohsJGeXK3DMPtsTw"
          >Ir para a playlista</q-btn
        >
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-img class="img-2">
        <div class="absolute-bottom text-h6">S.T.A.L.K.E.R.: Clear Sky</div>
      </q-img>

      <q-card-section>
        O jogador assume o papel de Scar, um mercenário veterano. O único
        sobrevivente após uma enorme emissão de energia em que foi pego enquanto
        guiava um grupo de cientistas pela Zona,
      </q-card-section>
      <q-separator class="mt" />
      <q-card-actions class="">
        <q-btn
          flat
          outline
          target="_blanck"
          href="https://www.youtube.com/watch?v=DKgZqMp6sl0&list=PLa2rM52nzkHEgXOBvKOyzx4osXUK_IN2C"
          >Ir para a playlista</q-btn
        >
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-img class="img-3">
        <div class="absolute-bottom text-h6">
          S.T.A.L.K.E.R.: Shadow of Chernobyl
        </div>
      </q-img>

      <q-card-section>
        No primeiro jogo da série, o jogador assume o papel de um stalker
        amnésico conhecido como "O Marcado", que tem a tarefa de matar outro
        stalker chamado Strelok. No decorrer do jogo, o protagonista descobre
        pistas sobre seu passado e sua
      </q-card-section>
      <q-separator />
      <q-card-actions>
        <q-btn
          flat
          outline
          target="_blanck"
          href="https://www.youtube.com/watch?v=7n_bZTVCGVk&list=PLa2rM52nzkHEIbpSYnkV1YEhjl_mjfk-g"
          >Ir para a playlista</q-btn
        >
      </q-card-actions>
    </q-card>
  </div>

  <section class="card-destiny">
    <h3>Destiny 2: Caça Fantamas</h3>
    <q-card class="">
      <q-card-section horizontal>
        <q-img class="col-5" src="../assets/img/destiny.jpg" />
        <q-card-section>
          O jogador assume o papel de um Guardião, protetores da última cidade
          segura da Terra, enquanto exercem um poder chamado Luz para proteger a
          Última Cidade de diferentes raças alienígenas. Uma dessas raças, a
          Cabal, liderada pelo senhor da guerra Dominus Ghaul, se infiltra na
          Última Cidade e retira todos os Guardiões da Luz. O jogador parte em
          uma jornada para recuperar sua Luz e encontrar uma maneira de derrotar
          Ghaul e seu exército da Legião Vermelha e recuperar a última cidade.
          Como o Destiny original, o jogo apresenta pacotes de expansão que
          promovem a história e adicionam novos conteúdos e missões.
          <q-card-actions>
            <q-btn flat>Assista como pegar as almas de forma rapida</q-btn>
          </q-card-actions>
        </q-card-section>
      </q-card-section>
    </q-card>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { Card } from './models';
const cards: Card[] = [
  {
    content:
      'O terceiro jogo da série, Call of Pripyat acontece logo após os eventos de Shadow of Chernobyl. Tendo descoberto o caminho aberto para o centro da Zona, o governo decide controlá-lo através da "Operação Fairway" ',
    title: 'S.t.a.l.k.e.r.: CALL OF Pripyat ',
    url: '/assets/img/stallKerCall.jpg',
  },
  {
    content:
      'O jogador assume o papel de Scar, um mercenário veterano. O único sobrevivente após uma enorme emissão de energia em que foi pego enquanto guiava um grupo de cientistas pela Zona, ',
    title: 'S.t.a.l.k.e.r.: Clear Sky ',
    url: '~assets/img/stallKerCall.jpg',
  },
  {
    content:
      'No primeiro jogo da série, o jogador assume o papel de um stalker amnésico conhecido como "O Marcado", que tem a tarefa de matar outro stalker chamado Strelok. No decorrer do jogo, o protagonista descobre pistas sobre seu passado e sua ',
    title: 'S.T.A.L.K.E.R.: Shadow of Chernobyl ',
    url: '../assets/img/stallKerCall.jpg',
  },
];
export default defineComponent({
  name: 'cardComponent',
  setup() {
    return {
      cards: cards,
    };
  },
});
</script>
<style scoped>
.card-container {
  width: 80%;
  margin: auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  box-sizing: border-box;
}
.titulo {
  width: 100%;
  text-align: center;
}
.titulo .line {
  background-color: black;
  width: 100px;
}
.my-card {
  width: 32%;
  height: auto;
  align-items: center;
}
.card-destiny {
  width: 80%;
  margin: auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  box-sizing: border-box;
}
.mt {
  margin-top: 20px;
}
.img-1 {
  background-image: url('../assets/img/stallKerCall.jpg');
  background-size: cover;
}
.img-2 {
  background-image: url('../assets/img/stalkerClear.jpg');
  background-size: cover;
}
.img-3 {
  background-image: url('../assets/img/stalkerShadow.jpg');
  background-size: cover;
}
</style>
