<script>
  export let pelicula = {};
</script>

<style>
  .title {
    font-weight: bold;
  }
  .card {
    background-color: #fdebc9;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    border-radius: 5px;
    transition: 0.3s;
    padding: 10px;
    margin: 10px;
  }

  .card:hover {
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.4);
  }

  input {
    background-color: inherit;
    padding: 10px;
    font-size: 14px;
    color: black;
    border: 0;
    outline: none;
    margin-left: 5px;
    margin-bottom: 4px;
    max-width: 140px;
  }

  input:focus {
    background-color: wheat;
  }

  input:required:invalid,
  input:focus:invalid {
    background-color: lightpink;
  }
</style>

<div class="card">
  <input bind:value={pelicula.nombre} placeholder="Nombre" class="title" />
  <input bind:value={pelicula.genero} placeholder="Genero" class="title" />  
  <input bind:value={pelicula.calificacion} placeholder="Calificación" class="title" />
  <input bind:value={pelicula.director} placeholder="Director" class="title" />
  <slot />
</div>
