<template>
    <div style="width: 100vw; height: 100vh; overflow: hidden; display: flex">
        <div style="flex: 1; background-color: dodgerblue;">
            <el-image style="width: 100%; height: 100%;" fit="cover"
                src="https://512pixels.net/wp-content/uploads/2025/08/26-Tahoe-Beach-Dawn-thumb.jpeg" />
        </div>
        <div class="welcome-title">
            <div style="font-size: 30px; font-weight: bold;">欢迎来到我们的学习平台</div>
            <div style="margin-top: 10px;">在这里你可以学习如何使用Java，如何搭建网站，并且与Java之父密切交流</div>
        </div>
        <div style="width: 400px; background-color: white;">
            <router-view/>
        </div>
    </div>
</template>

<script setup>
</script>

<style scoped>
    .welcome-title {
        position: absolute;
        bottom: 30px;
        left: 30px;
        color: white;
        text-shadow: 0 0 10px black;
    }
</style>

