<script setup>
const props = defineProps(["pessoa"]);

</script>

<template>

    <tr>
        <td>{{ pessoa.nome }}</td>
        <td>{{ pessoa.cpf }}</td>
        <td>{{ pessoa.email }}</td>
    </tr>

</template>