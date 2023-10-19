<script>
  import Header from "./components/Header.svelte";
  import MovieList from "./components/MovieList.svelte";
</script>

<Header />

<p class="list-title">Nuestros estrenos exclusivos</p>
<MovieList
  url="https://api.themoviedb.org/3/movie/now_playing?language=es&page=1"
/>
<p class="list-title">Cada martes, una nueva serie</p>
<MovieList
  url="https://api.themoviedb.org/3/movie/top_rated?language=en-US&page=1"
/>
<p class="list-title">Las mejor valoradas por la comunidad</p>
<MovieList
  url="https://api.themoviedb.org/3/movie/upcoming?language=en-US&page=1"
/>
<p class="list-title">Con los mejores canales temáticos</p>
<MovieList
  url="https://api.themoviedb.org/3/movie/popular?language=en-US&page=1"
/>

<style>
  .list-title {
    display: flex;
    color: white;
    font-weight: bold;
    font-size: 30px;
    margin-left: 50px;
    margin-top: 80px;
  }
</style>
