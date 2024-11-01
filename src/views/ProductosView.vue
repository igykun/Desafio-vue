<template>
    <div>
      <section class="container">
        <h1 class="text-center">
            Productos
        </h1>
        <div class="row my-5">
          <div class="col-md-3 my-3" v-for="producto in productos" :key="productos.id">
            <Productos
              :nombre="producto.nombre"
              :descripcion="producto.descripcion"
              :precio="producto.precio"
              :cantidad="producto.cantidad"
            />
          </div>
        </div>
      </section>
      <div class="d-flex justify-content-center w-100 text-center">
        <RouterLink to="/">
            <span class="m-4 badge text-bg-primary text-wrap fs-2">Volver</span>
        </RouterLink>
      </div>
    </div>
  </template>
  
  <script>
  import { RouterLink } from "vue-router";
  import Productos from "../components/Productos.vue";
  
  export default {
    components: {
      RouterLink,
      Productos,
    },
    data() {
      return {
        productos: [
          {
            id: 0,
            nombre: "Pastel de Choclo",
            descripcion:
              "Un pastel de choclito",
            precio: 12000,
            cantidad: "1 persona",
          },
          {
            id: 1,
            nombre: "Estofado de carne",
            descripcion:
              "Un estado de carne con arroz para acompañar",
            precio: 10000,
            cantidad: "1 persona",
          },
          {
            id: 2,
            nombre: "Costillar",
            descripcion:
              "Un trozo de costilla de cerdo acompañado de papas fritas y 2 acompañamientos a eleccion",
            precio: 17000,
            cantidad: "2 personas",
          },
          {
            id: 3,
            nombre: "Sufle de papas",
            descripcion:
              "No se que poner ya",
            precio: 11000,
            cantidad: "1 persona",
          },
          {
            id: 4,
            nombre: "Papas fritas",
            descripcion:
              "Un plato grande de papas fritas para compartir",
            precio: 10000,
            cantidad: "2 personas",
          },
          {
            id: 5,
            nombre: "Platon pasta",
            descripcion:
              "Un plato gigante de pasta para compartir",
            precio: 27000,
            cantidad: "4 personas",
          },
          {
            id: 6,
            nombre: "Papas rellenas",
            descripcion:
              "Algo descriptivo de papas rellenas",
            precio: 12100,
            cantidad: "1 personas",
          },
          {
            id: 7,
            nombre: "Caldillo de pescado",
            descripcion:
              "Pos es un caldillode pescado",
            precio: 25000,
            cantidad: "4 personas",
          },
          {
            id: 8,
            nombre: "Churrasco",
            descripcion:
              "Un churrasco",
            precio: 10000,
            cantidad: "1 personas",
          },
        ],
      };
    },
  };
  </script>