<template>
    <div>
        <div class="product">
            <h2>{{ product.name }}</h2>
            <h3>{{ product.price }} €</h3>
            <p>{{ product.description }}</p>
            <iframe width="560" height="315" :src="product.video" 
                frameborder="0" 
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
                allowfullscreen>
            </iframe>
            <InputCantidad />
            <div class="add-cart">
                <Button text=" Añadir al carrito" icon="cart-plus" /> 
            </div>
            
        </div>
    </div>

</template>

<script>
import InputCantidad from './InputCantidad.vue'
import Button from './Button.vue'

export default {
    components: {
        InputCantidad,
        Button
    },
    props: {
        product: Object,
    },
}
</script>

<style scoped>
.product {
    margin-left: 30px;
    width: 600px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-content: flex-start;
    align-items: flex-start;
}

.add-cart {
    margin: 10px;
}

h2 {
    font-family: 'Courier New', Courier, monospace;
    font-weight: 800;
    font-size: 2em;
    color: #111111;
}

h3 {
    font-size: 1.5em;
    color: #111111;
}

iframe {
    margin: 10px 0;
}
</style>