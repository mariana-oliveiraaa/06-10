
</template>

<script>
  import GenerosApi from ''../api/genero';
  const GenerosApi = new GenerosApi()

  export default {
    data() {
      return {
        generos: []

      }
   },
   async created () {
    this.generos= await generosApi.buscarTodosOsGeneros()
   },
   methods:{
    buscarFilmesDir(id) {
      return `/fimes/${id}`
    }
   }
  }

</script>
<template>
  <nav class="navbar navbar-expand-lg navbar-blue bg-dark">
    <div class="container-fluid p-3">
      <a class="navbar-brand p-1">Megaflix</a>
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav">
          <li class="nav-item p-1">
            <RouterLink to="/" class="nav-link links">Home</RouterLink>
          </li>
          <li class="nav-item p-1">
            <RouterLink to="/filmes" class="nav-link links">Filmes</RouterLink>
          </li>
          <li class="nav-item p-1">
            <RouterLink to="/series" class="nav-link links">Séries</RouterLink>
          </li>
        </ul>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Classificacao
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <li v-for="genero of generos" :key="genero.id">
            <router-link class="dropdown-item" :to='buscarFilmesDir'(genero.id)'> {{genero.name}}</router-link>'
        
            <li> <RouterLink> </RouterLink></li>
            <li> <RouterLink></RouterLink></li>
            <li><RouterLink> </RouterLink></li>
            <li><RouterLink> </RouterLink></li>
          </ul>
        </li>
      </div>
    </div>
  </nav>
</template>
