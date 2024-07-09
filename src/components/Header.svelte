<script>
  import Logo from "./Logo.svelte";
  import Link from "./Link.svelte";
</script>

<header>
  <Logo />

  <nav>
    <Link text="Inicio" />
    <Link text="Películas" />
    <Link text="Series" />
    <Link text="Colecciones" />
    <Link text="Festivales" />
    <Link text="Más" />
  </nav>

  <div class="right-container">
    <button class="button-1">SUSCRÍBETE</button>
    <button class="button-2">INICIAR SESIÓN</button>
    <!-- <img
      class="magnifier-icon"
      src="../src/assets/lupita1.svg"
      alt="Icono de una lupa"
    /> -->
  </div>
</header>

<style>
  header {
    display: flex;
    align-items: center;
    width: 100%;
    margin: 20px 40px;
    gap: 20px;
  }

  .right-container {
    display: flex;
    gap: 20px;
    align-items: center;
    margin-left: 810px;
  }
  .button-1 {
    height: 32px;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    font-weight: 750;
    padding: 0px 10px;
    background-color: #02ffa1;
    border-radius: 5px;
    border: none;
    cursor: pointer;
  }

  .button-1:hover {
    background-color: #00965f;
    color: #ffff;
  }

  .button-2 {
    height: 32px;
    padding: 0 10px;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    font-weight: 750;
    background-color: #141426;
    color: white;
    border-color: white;
    border-radius: 5px;
    cursor: pointer;
  }

  .button-2:hover {
    background-color: #00965f;
    color: #ffff;
  }

  .magnifier-icon {
    width: 30px;
  }
</style>
