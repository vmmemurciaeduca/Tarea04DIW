<template>
    <div class="header">
        <Logo />

        <Navigation />

        <HeaderButtons />
    </div>
</template>

<script>
import Logo from './Logo.vue';
import Navigation from './Navigation.vue';
import HeaderButtons from './HeaderButtons.vue';

export default {
    components: {
        Logo,
        Navigation,
        HeaderButtons
    }
}
</script>

<style>
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    align-content: center;
}


</style>