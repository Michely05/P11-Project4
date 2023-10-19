<script>
  import Header from "./components/Header.svelte";
  import MovieList from "./components/MovieList.svelte";
</script>

<Header />

<MovieList
  url="https://api.themoviedb.org/3/movie/now_playing?language=es&page=1"
/>

<MovieList
  url="https://api.themoviedb.org/3/movie/top_rated?language=en-US&page=1"
/>

<MovieList
  url="https://api.themoviedb.org/3/movie/upcoming?language=en-US&page=1"
/>

<MovieList
  url="https://api.themoviedb.org/3/movie/popular?language=en-US&page=1"
/>
