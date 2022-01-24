<template>
    <div class="product">
        <ProductImagesSwitcher :images="images" :alternatives="alternatives"/>
        <ProductDetail :product="product" />
    </div> 
</template>

<script>

import ProductImagesSwitcher from './ProductImagesSwitcher.vue'
import ProductDetail from './ProductDetail.vue'

export default {
    components: {
        ProductImagesSwitcher,
        ProductDetail,
    },  
    data() {
        return {
            images: [
                'imgs/rift1.jpg',
                'imgs/rift2.jpg',
                'imgs/rift3.jpg',
            ],
            alternatives: [
                '1',
                '2',
                '3',
            ],
            product: {
                name: "Oculus Rift VR",
                price: 599,
                description: "Gafas de VR de alta calidad, lo mejor del mercado si señor",
                video: "https://www.youtube.com/embed/Y24pPbZ9DZs"
            }
        }
    }
}
</script>

<style>
.product {
    margin: 50px auto;
    display: flex;
    justify-content: center;
    align-content: center;
    align-items: flex-start;
}
</style>