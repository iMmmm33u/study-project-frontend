<template>
    <div>
        <div>
            欢迎{{ store.auth.user.username }}进入学习平台
        </div>
        <div>
            <el-button @click="logout" type="danger">退出登录</el-button>
        </div>
    </div>
</template>

<script setup>
import { get } from '@/net';
import { useStore } from '@/stores';
import { ElMessage } from 'element-plus';
import { useRouter } from 'vue-router';

const router = useRouter()
const store = useStore()

const logout = () => {
    get('/api/auth/logout', (message) => {
        ElMessage.success(message)
        store.auth.user = null
        router.push('/')
    })
}
</script>

<style scoped></style>