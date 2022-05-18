<template>
  <footer class="footer">
    <div class="footerCard">
      <div>
        <h5>ID Gamer</h5>
        <p>
          Gameplay ,Curiosidades, noticia, informação tudo sobre o mercado game
          do brasil...
        </p>
      </div>
      <div>
        <h5>Links</h5>
        <p><a href="https://www.twitch.tv/arthur_scott">TWITCH TV</a></p>
        <p>
          <a href="https://www.youtube.com/channel/UCP6oZeKFDzbJs-038BNYUUQ"
            >YOUTUBE</a
          >
        </p>
        <p><a href="">FACEBOOK</a></p>
      </div>
    </div>
  </footer>
</template>
<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  setup() {
    return {};
  },
});
</script>
<style>
footer {
  height: 50vh;
  background-color: #212121;
  width: 100%;
  display: flex;
  flex-direction: row;
}
.footerCard {
  display: flex;
  flex-direction: row;
  width: 80%;
  margin: auto;
  justify-content: space-between;
}
.footerCard div {
  width: 40%;
  padding: 10px;
  font-size: 1.1rem;
  color: white;
}
.footerCard a {
  text-decoration: none;
  color: white;
  padding: 0 20px;
  font-size: 1rem;
}
</style>
