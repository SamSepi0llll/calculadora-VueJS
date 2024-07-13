<script setup>
const props = defineProps(["numero1", "numero2", "resultado"])
</script>

<template>
    <form>
    <div class="row">
        <div class="col-md-12 d-flex">
        <input @keyup="props.numero1" class="form-control me-4" type="number" placeholder="Digite o primeiro valor" required>
        <input @keyup="props.numero2" class="form-control" type="number" placeholder="Digite o segundo valor" required>
        </div>
        <p v-if="props.resultado <= 0" class="mt-5 text-center fs-4">O resultado é um Número negativo!</p>
        <p v-else class="mt-5 text-center fs-4">O resultado da operação é: {{ props.resultado }} </p>
    </div>
    </form>
</template>