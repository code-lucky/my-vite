<script setup lang="ts">
import { ref } from 'vue';

const formState = ref({
    username:'',
    password:'',

})
</script>

<template>
    <div>
        <h3>会议室预定系统</h3>
        <a-form
            :model="formState"
            name="basic"
            :label-col="{ span: 8 }"
            :wrapper-col="{ span: 16 }"
            autocomplete="off"
        >
            <a-form-item
            label="邮箱"
            name="username"
            :rules="[{ required: true, message: 'Please input your username!' }]"
            >
                <a-input v-model:value="formState.username" />
            </a-form-item>

            <a-form-item
            label="验证码"
            name="username"
            :rules="[{ required: true, message: 'Please input your username!' }]"
            >
                <a-input v-model:value="formState.username" />
            </a-form-item>

            <a-form-item
            label="密码"
            name="password"
            :rules="[{ required: true, message: 'Please input your password!' }]"
            >
                <a-input-password v-model:value="formState.password" />
            </a-form-item>

            <a-form-item
            label="确认密码"
            name="password"
            :rules="[{ required: true, message: 'Please input your password!' }]"
            >
                <a-input-password v-model:value="formState.password" />
            </a-form-item>

            <a-form-item :wrapper-col="{ offset: 8, span: 16 }">
                <a-button type="primary" html-type="submit">修改</a-button>
            </a-form-item>
        </a-form>
    </div>
</template>

<style scoped>

</style>