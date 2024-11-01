<template>
    <div class="anime-card">
        <img src="../assets/img/colaciones.jpg" class="card-img-top" alt="Imagen del Producto">
        <div class="card-body">
            <h5 class="card-title">{{ nombre }}</h5>
            <p class="card-text">{{ descripcion }}</p>
        </div>
        <ul class="list-group list-group-flush">
            <li class="list-group-item">Precio: ${{ precio }}</li>
            <li class="list-group-item">Cantidad: {{ cantidad }}</li>
        </ul>
        <div class="card-footer">
            <a href="#" class="card-link">Ver más</a>
            <a href="#" class="card-link">Comprar</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Productos',
    props: ['nombre', 'descripcion', 'precio', 'cantidad']
}
</script>

<style scoped>
.anime-card {
    background: linear-gradient(145deg, #f8f9fa, #e0e0e0);
    border-radius: 15px;
    box-shadow: 10px 10px 20px rgba(0, 0, 0, 0.2), -10px -10px 20px rgba(255, 255, 255, 0.5);
    overflow: hidden;
    width: 300px;
    height: 480px; /* Adjusted height to accommodate footer */
    margin: 20px auto;
    text-align: center;
    transition: transform 0.3s ease;
}

.anime-card:hover {
    transform: scale(1.05);
}

.card-img-top {
    width: 100%;
    height: 180px; /* Fixed height for uniformity */
    object-fit: cover;
    border-bottom: 3px solid #ff9f1c;
}

.card-body {
    padding: 15px;
    background-color: #fefefe;
    height: 160px; /* Adjusted height to fit footer */
    overflow: hidden;
}

.card-title {
    font-family: 'Comic Sans MS', sans-serif;
    font-size: 1.4rem;
    color: #ff6b6b;
    text-shadow: 1px 1px #ffd43b;
    margin-bottom: 5px;
}

.card-text {
    font-size: 1rem;
    color: #333;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap; /* Prevents text wrapping */
}

.list-group-item {
    background-color: #fffae6;
    border: none;
    color: #ff6b6b;
    font-weight: bold;
}

.card-footer {
    padding: 10px;
    background-color: #fefefe;
}

.card-link {
    display: inline-block;
    color: #6a4c93;
    text-decoration: none;
    font-weight: bold;
    margin: 0 5px;
    padding: 8px 16px;
    border: 2px solid #ff6b6b;
    border-radius: 10px;
    transition: background-color 0.3s, color 0.3s;
}

.card-link:hover {
    background-color: #ff6b6b;
    color: #fff;
}
</style>
