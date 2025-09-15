<script setup>
import { useRouter } from 'vue-router';
import { get } from './net';
import { useStore } from './stores';

const store = useStore()
const router = useRouter()

if (store.auth.user == null) {
    get('/api/user/me', (message) => {
        store.auth.user = message
        router.push('/index')
    }, () => {
        store.auth.user = null
    })
}


</script>

<template>
    <router-view />
</template>

<style scoped></style>