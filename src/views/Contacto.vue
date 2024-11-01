<template>
    <div>
      <section class="container" id="productos">
        <h1 class="text-center pokemon-title">Contacto</h1>
        <div class="col-md-6 my-5 m-auto contact-form">
          <h4 class="text-primary text-center">¡Contáctanos!</h4>
          <img
            src="https://www.pokemon.com/static-assets/content-assets/cms2/img/pokedex/full/025.png"
            alt="Pikachu"
            class="pokemon-image"
          />
          <form>
            <div class="mb-3">
              <label for="exampleFormControlInput1" class="form-label">Correo</label>
              <input
                type="email"
                class="form-control"
                id="exampleFormControlInput1"
                placeholder="name@example.com"
                required
              />
            </div>
            <div class="mb-3">
              <label for="exampleFormControlTextarea1" class="form-label">Mensaje</label>
              <textarea
                class="form-control"
                id="exampleFormControlTextarea1"
                rows="3"
                required
              ></textarea>
            </div>
            <button type="submit" class="btn btn-pokemon mb-5">Enviar</button>
          </form>
        </div>
      </section>
    </div>
    <div class="d-flex justify-content-center w-100 text-center">
        <RouterLink to="/">
            <span class="m-4 badge text-bg-primary text-wrap fs-2">Volver</span>
        </RouterLink>
      </div>
  </template>
  
  <script>
  import { RouterLink } from "vue-router";
  
  export default {
    components: {
      RouterLink,
    },
  };
  </script>
  
  <style>
  .pokemon-title {
    color: #ffcc00;
    font-family: 'Pokemon Solid', sans-serif;
    margin-bottom: 20px;
  }
  
  .contact-form {
    background-color: #ffffff;
    border-radius: 15px;
    padding: 30px;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
  }
  
  .pokemon-image {
    max-width: 100px;
    display: block;
    margin: 0 auto 20px;
  }
  
  .btn-pokemon {
    background-color: #ffcc00;
    color: #000;
  }
  
  .btn-pokemon:hover {
    background-color: #ff9900;
  }
  </style>
  