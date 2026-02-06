<template>
    <div :class="baseClass">
        <slot/>
    </div>
</template>

<script>

export default {
    props: ['variant', 'text'],
    computed: {
        baseClass() {
            return [
                'alert', 
                this.variant ? `alert-${this.variant}`: ''
            ];
        }
    }
}
</script>

<style scoped>
    .alert {
        background-color: bisque;
        padding: 1rem;
        font-weight: bold;
        border-radius: 0.5rem;
    }

    .alert-success {
        background-color: green;
        color: #FFF;
    }

    .alert-danger {
        background-color: red;
        color: #FFF;
    }
</style>