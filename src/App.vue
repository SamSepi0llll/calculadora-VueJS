<script setup>
  import { reactive } from 'vue';
  import Header from './components/Header.vue'
  import Formulario from './components/Formulario.vue'

  const estado = reactive({
    filtro: 'adicao',
    numero1: 0,
    numero2: 0
  })

  const adicao = ({numero1, numero2} = estado) => {
    return Number(numero1) + Number(numero2)
  }

  const subtracao = ({numero1, numero2} = estado) => {
    return numero1 - numero2
  }

  const multiplicacao = ({numero1, numero2} = estado) => {
    return numero1 * numero2
  }

  const divisao = ({numero1, numero2} = estado) => {
    return numero1 / numero2
  }

  const getResultado = () => {
    const {numero1, numero2, filtro} = estado

      if(numero1, numero2){
        switch(filtro) {
      case 'adicao': 
        return adicao()
      case 'subtracao':
        return subtracao()
      case 'multiplicacao':
        return multiplicacao()
      case 'divisao':
        return divisao()
    }
      }
  }

</script>

<template>
  <div class="container bg-light">
    <Header :select="evento => estado.filtro = evento.target.value" />
    <Formulario 
    :numero1="evento => estado.numero1 = evento.target.value"
    :numero2="evento => estado.numero2 = evento.target.value"
    :resultado="getResultado()"
      />
  </div>
</template>
