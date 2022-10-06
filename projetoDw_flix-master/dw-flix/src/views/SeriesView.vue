<script>
import CardSerie from "../components/séries/CardSerie.vue";

export default {
  components: { CardSerie },
  data() {
    return {
      series: [
        {
          id: 7,
          imagem: new URL("../assets/img/oi.jpg", import.meta.url).href,
          autor: "Fulano",
        },
        {
          id: 8,
          imagem: new URL("../assets/img/filme5.jpg", import.meta.url).href,
          autor: "Beltrano",
        },
        {
          id: 9,
          imagem: new URL("../assets/img/oii.jpg", import.meta.url).href,
        },
      ],
    };
  },
};
</script>
<template>
  <h2 class="fs-1 text-light text-center p-2">Continuar Assistindo</h2>
  <div class="card-group card-filmes">
    <CardSerie v-for="serie of series" :key="serie.id" :serie="serie" />
  </div>
  <h2 class="fs-1 text-light text-center p-2">Top 3</h2>
  <div class="card-group card-filmes">
    <CardSerie v-for="serie of series" :key="serie.id" :serie="serie" />
  </div>
</template>
