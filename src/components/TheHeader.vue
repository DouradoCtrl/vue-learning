<template>
    <header class="header">
        <!-- Otters Sl  -->
        <h1 
            class="title" 
            v-if="$slots.title"
        >
            <slot name="title"/>
        </h1>
        <div class="description">
            <slot name="description"/>
        </div>
        <div class="content">
            <slot/>
        </div>
    </header>
</template>

<script>
    export default {
        mounted() {
            console.log(this.$el);
            console.log(this.$slots);
        }
    }
</script>

<style>
    .header {
        background-color: gray;
        padding: 20px;
        color: #FFFFFF;
        text-align: center;
        border-radius: 1rem;
    }
</style>