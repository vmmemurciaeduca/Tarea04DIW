<template>
  <button>
        <i :class="iconClass"></i>
        <span>{{text}}</span>
    </button>
</template>

<script>
export default {
    props: {
        text: String,
        icon: String,
    },
    computed: {
        iconClass() {
            return `fas fa-${this.icon}`;
        },
    },
}
</script>

<style scoped>
button {
    cursor: pointer;
    background: #FBCA1F;
    font-family: inherit;
    padding: 0.6em 1.3em;
    font-weight: 900;
    font-size: 18px;
    border: 3px solid black;
    border-radius: 0.4em;
    box-shadow: 0.1em 0.1em;
    margin-right: 10px;
}

</style>