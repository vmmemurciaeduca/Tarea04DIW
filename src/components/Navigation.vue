<template>
    <div class="navigation">
        <ul>
            <li>HARWARE RV</li>
            <li>SOFTWARE RV</li>
            <li>ACCESORIOS RV</li>
            <li>SERVICIOS RV</li>
        </ul>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.navigation ul {
    list-style-type: none;
}

.navigation li {
    float: left;
    border: 3px solid white;
    font-size: 1.4rem;
    margin: 0.5rem 1rem;
    padding: 0.5rem 2rem;
}

.navigation li:hover {
    background-color: #FFD55E;
    color: black;
    border: 3px solid black;
    border-radius: 0.4em;
}
</style>