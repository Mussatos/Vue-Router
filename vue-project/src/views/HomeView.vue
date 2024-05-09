<script setup>
import Tabela from '@/components/Tabela.vue'
import { ref } from 'vue';


const pessoas = ref([JSON.parse(localStorage.getItem('dados'))]);

</script>

<template>
<RouterLink to="/add">Adicionar</RouterLink>

  <main>

    <Tabela :pessoas="pessoas"/>

  </main>
</template>
