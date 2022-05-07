<template>
    <div class="title">{{ userStore.name }}</div>
</template>

 <script lang="ts" setup>
import { useUserStore } from '@/store/user';
import API from '@/api';

const requestRes = async () => {
    let result = await API.login('zhangsan', '123456');
};

const userStore = useUserStore();
setTimeout(() => {
    userStore.name = 'lxc';
}, 2000);
</script>

<style lang="less" scoped>
.title {
    font-weight: bold;
}
</style>