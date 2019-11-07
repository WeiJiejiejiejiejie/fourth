<template>
    <div>
        <van-tabs @click="onClick">
            <van-tab title="账号登录">内容1</van-tab>
            <van-tab title="验证码登录">内容 2</van-tab>
        </van-tabs>
    </div>
</template>

<script>
    import {Tab} from 'vant';
    import {Tabs} from 'vant';
    // import { Field } from 'vant';
    export default {
        name: "login",
        methods: {
            onClick(name, title) {
                this.$toast(title);
            }
        },
        components:{
            "van-tabs":Tab,
            "van-tab":Tabs,
            // "van-cell-group":Field,
            // "van-field":Field
        }

    }
</script>

<style scoped>

</style>