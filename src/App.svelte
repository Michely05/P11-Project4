<script>
  import Header from "./components/Header.svelte";
  import MovieList from "./components/MovieList.svelte";
</script>

<Header />

<div class="welcome-panel">
  <h1>Descubre el cine que lo cambia todo</h1>
  <div class="subtitle">
    <h2>
      Con nuestra suscripción, accede a obras maestras , clásicos, cine
      independiente, series exclusivas, documentales y mucho más.
    </h2>
  </div>
  <p class="email-message">
    Para iniciar tu suscripción, introduce tu email aquí
  </p>
  <input type="text" placeholder="Tu email" />
  <button class="start-button">COMENZAR</button>
  <p class="final-message">
    Más de 10.000 películas y series. Cancela cuando quieras.
  </p>
</div>

<p class="list-title">Nuestros estrenos exclusivos</p>
<MovieList
  url="https://api.themoviedb.org/3/movie/now_playing?language=es&page=1"
/>
<p class="list-title">Cada martes, una nueva película</p>
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
    font-size: 25px;
    margin-left: 45px;
    margin-top: 80px;
  }

  .welcome-panel {
    text-align: center;
    height: 350px;
    margin: 100px;
  }

  h1 {
    font-size: 70px;
    font-weight: bold;
    color: white;
  }

  .subtitle {
    width: 1000px;
    margin: auto;
    font-size: 20px;
    color: white;
  }

  .email-message {
    color: white;
    margin-top: 50px;
    font-size: 20px;
  }

  input {
    width: 420px;
    height: 35px;
    background-color: #141426;
    border-radius: 5px;
    border-color: gray;
    outline: 0;
    margin-right: 2px;
    padding-left: 10px;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    font-size: 1rem;
    color: gray;
  }

  input::placeholder {
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    font-size: 1rem;
  }

  .start-button {
    height: 40px;
    width: 140px;
    padding: 0 20px;
    border-radius: 5px;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    font-weight: 750;
    background-color: #02ffa1;
    border: none;
    cursor: pointer;
  }

  .start-button:hover {
    background-color: #00965f;
    color: #ffff;
  }

  .final-message {
    color: gray;
  }
</style>
