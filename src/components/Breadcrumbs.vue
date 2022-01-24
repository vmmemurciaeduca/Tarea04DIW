<template>
  <h2>{{ breadcrumbs }}</h2>
</template>

<script>
export default {
    props: {
        path: Array,
    },
    computed: {
        breadcrumbs: function() {
            return this.path.join(' > ');
        },
    },

}
</script>

<style>

</style>