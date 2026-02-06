<template>
    <div :class="['alert', {
        'alert-sucess': variant === 'success', 
        'alert-danger': variant === 'danger',
        }]">
        Formulário enviado com sucesso
    </div>
</template>

<script>

export default {
    props: ['variant'],
    methods: {

    }
}
</script>

<style>
    .alert {
        background-color: bisque;
        padding: 1rem;
        font-weight: bold;
        border-radius: 0.5rem;
    }

    .alert-sucess {
        background-color: green;
        color: #FFF;
    }

    .alert-danger {
        background-color: red;
        color: #FFF;
    }
</style>