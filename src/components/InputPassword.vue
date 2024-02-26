<script setup>
import { ref } from 'vue';

const password = ref("");
const showPassword = ref(false);

const  togglePasswordVisibility = () => {
    showPassword.value = !showPassword.value;
}
</script>

<template>

    <div class="container text-center input-password">
        <h1 class="my-3">Exercise Input Password</h1>
        <input :type="showPassword ? 'text' : 'password'" v-model="password" name="password" id="password" class="form-control">
        <div class="d-block">
            <button id="show-password" class="mt-2 btn btn-primary" @click=" togglePasswordVisibility">Show Password</button>
        </div>
    </div>
</template>

<style lang="css" scoped>
    #show-password:hover {
        cursor: pointer;
        user-select: none;
    }
</style>