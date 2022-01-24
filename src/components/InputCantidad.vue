<template>
    <div>
        <Button icon="minus" @click="cantidad--"/>
        <input type="number" v-model="cantidad">
        <Button icon="plus" @click="cantidad++"/>
    </div>
</template>

<script>
import Button from './Button.vue'

export default {
    components : {
        Button,
    },
    data() {
        return {
            cantidad: 1,
        }
    },
}
</script>

<style scope>
button {
    font-size: 1.2em;
    padding: 0 10px;
}
input {
    margin: 0 10px;
    font-size: 1.2em;
    width: 50px;
    text-align: center;
}
</style>