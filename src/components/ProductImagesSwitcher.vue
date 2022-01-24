<template>
    <div>
        <div class="images">
            <button @click="prevImage">
                <i class="fas fa-chevron-left"></i>
            </button>
            
            <img :src="currentImage" :alt="currentAlt">
            
            <button @click="nextImage">
                <i class="fas fa-chevron-right"></i>
            </button>
        </div>
        <div class="minis">
            <img :src="image" v-for="(image, index) in images" :key="index" :alt="alternatives[index]" @click="setCurrentIndex(index)">
        </div>
    </div>
</template>

<script>
export default {
    props: {
        images: Array,
        alternatives: Array,
    },
    data() {
        return {
            currentIndex: 0
        }
    },
    computed: {
        currentImage: function() {
            return this.images[this.currentIndex];
        },
        currentAlt: function() {
            return this.alternatives[this.currentIndex];
        },
    },
    methods: {
        nextImage() {
            this.currentIndex = (this.currentIndex + 1) % this.images.length;
        },
        prevImage() {
            this.currentIndex = (this.currentIndex - 1 + this.images.length) % this.images.length;
        },
        setCurrentIndex(index) {
            this.currentIndex = index;
        },
    }
}
</script>

<style scoped>
.images {
    display: flex;
    justify-content: center;
    align-content: center;
    align-items: center;
}

.minis {
    margin-top: 20px;
    display: flex;
    justify-content: center;
    align-content: center;
    align-items: center;
}

.minis img {
    cursor: pointer;
    width: 50px;
    height: 50px;
    margin: 0 10px;
    border: none;
}

img {
    width: 600px;
    height: 600px;
    border: 2px solid black;
    border-radius: 10px;
    margin: 0 20px;
}

button {
    cursor: pointer;
    height: 32px;
    width: 32px;
    font-size: 1.2em;
    background: black;
    border-radius: 50%;
    color: #FFD55E;
    text-align: center;
}
</style>