<script setup>
import { ref } from 'vue';
import { useRoute,useRouter } from 'vue-router';

const router = useRouter();

const nome = ref('');
const cpf = ref('');
const email = ref('');

const onSubmit = () => {
    const pessoa = {
        nome: nome.value,
        cpf: cpf.value,
        email: email.value
    };
    localStorage.setItem("dados", JSON.stringify(pessoa));
    router.push('/');
}

</script>

<template>
    <form @submit.prevent="onSubmit">
        <div>
            <label for="nome">Nome</label>
            <input v-model="nome" type="text" id="nome">
        </div>

        <div>
            <label for="cpf">CPF</label>
            <input v-model="cpf" type="text" id="cpf">
        </div>

        <div>
            <label for="email">E-mail</label>
            <input v-model="email" type="text" id="email">
        </div>

        <button>Salvar</button>

    </form>
</template>