<script>
import CardMovie from "../components/filmes/CardMovie.vue";

export default {
  components: { CardMovie },
  data() {
    return {
      movies: [
        {
          id: 1,
          imagem: new URL("../assets/img/corra.jpg", import.meta.url).href,
          autor: ".",
        },
        {
          id: 2,
          imagem: new URL("../assets/img/divergente.jpg", import.meta.url)
            .href,
          autor: ".",
        },
        {
          id: 3,
          imagem: new URL("../assets/img/pulp.jpg", import.meta.url).href,
        },
      ],
    };
  },
};
</script>
<template>
  <h2 class="fs-1 text-light text-center p-2">Continuar Assistindo</h2>
  <div class="card-group card-filmes">
    <CardMovie v-for="movie of movies" :key="movie.id" :filme="movie" />
  </div>
  <h2 class="fs-1 text-light text-center p-2">Top 3</h2>
  <div class="card-group card-filmes">
    <CardMovie v-for="movie of movies" :key="movie.id" :filme="movie" />
  </div>
</template>
