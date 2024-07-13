<script setup>
    const props = defineProps(["select"])
</script>

<template>
    <header>
    <div class="row">
        <div class="col">
            <h1 class="mt-5 text-center">Calculadora aritmética</h1>
            <p class="text-center mb-5">Escolha a operação aritmética que deseja fazer</p>
            <div class="row">
            <div class="col-sm-2 text-center select">
                <select @change="props.select" class="form-control text-center">
                <option value="adicao">Adição</option>
                <option value="subtracao">Subtração</option>
                <option value="multiplicacao">Multiplicação</option>
                <option value="divisao">Divisão</option>
            </select>
            </div>
        </div>
        </div>
    </div>
    </header>
</template>

<style scoped>
    .select{
    margin: 0 auto 16px;
    }
</style>