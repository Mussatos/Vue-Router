<script setup>
import Linha from './Linha.vue'

const props = defineProps(["pessoas"]);


</script>


<template>
    <table>
        <thead>
            <th>Nome</th>
            <th>CPF</th>
            <th>E-mail</th>
        </thead>

        <tbody>

            <Linha v-for="pessoa in pessoas" 
            :pessoa="pessoa"
            />

        </tbody>
    </table>
</template>