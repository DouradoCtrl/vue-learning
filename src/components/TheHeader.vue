<template>
    <header class="header">
        Header Component
    </header>
</template>

<script>
    export default {
        beforeUnmount() {
            console.log('beforeUnmount');
        },

        unmounted() {
            console.log('unmounted');
        },
    }
</script>

<style>
    .header {
        background-color: #000000;
        padding: 20px;
        color: #FFFFFF;
        text-align: center;
        font-size: 24px;
        font-weight: bold;
    }
</style>