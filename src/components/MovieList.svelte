<script>
  import { onMount } from "svelte";

  /*Lista 1*/

  const url =
    "https://api.themoviedb.org/3/movie/now_playing?language=es&page=1";
  const options = {
    method: "GET",
    headers: {
      accept: "application/json",
      Authorization:
        "Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiIxNTg5MTFjOWFiNjkxNDdjNTMwN2RiY2QxZTliMjZhYSIsInN1YiI6IjY1MmZhZTEzZWE4NGM3MDEyZDcxZmI4ZiIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.QVjbVwdOFkdF10DMY9EXX0-JvgDI96JR0_uWV_c8E9E",
    },
  };

  let movies = [];

  onMount(() =>
    fetch(url, options)
      .then((response) => response.json())
      .then((data) => (movies = data.results))
      .catch((err) => console.error(err))
  );

  /*Lista 2*/
</script>

<div>
  {#each movies as movie}
    <img
      alt="Film cover"
      src={`https://image.tmdb.org/t/p/original/${movie.poster_path}`}
    />
  {/each}
</div>

<style>
  div {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 22px;
  }
  img {
    height: 420px;
    object-fit: cover;
  }
</style>
