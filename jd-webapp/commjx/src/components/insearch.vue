<template>
    <div>
        <van-search
                placeholder="请输入搜索关键词"
                show-action
                shape="round"
                @search="onSearch"
        >
            <div slot="action" @click="onSearch">搜索</div>
        </van-search>
        <hr style="border: 0.02rem solid #ccc;margin:0 auto">
        <p class="indentxx">大家都在搜</p>
        <p class="vcricle">魅族Pop2</p><p class="vcricle">魅族Max</p><p class="vcricle">魅族16pro</p>
        <hr style="border: 0.02rem solid #ccc;margin:0.3rem auto">
        <p class="indentxx">历史记录</p>
        <hr style="border: 0.005rem solid #ccc;margin:0.1rem auto">
        <p class="indentxxt">暂无搜索记录</p>
        <a  href="#/list?id='+index"><van-button type="primary" size="large" class="foootbut">返回首页</van-button></a>
    </div>
</template>

<script>
    import { Search } from 'vant';
    import { Button } from 'vant';
    export default {
        name: "vinsearch",
        methods:{
            onSearch(){
               this.value='http://www.baidu.com'
            }
        },
        components:{
            "van-search":Search,
            "van-button":Button
        }
    }
</script>

<style scoped>
    div .indentxx{
        width:100%;
        font-size: 0.16rem;
        margin-top: 0.1rem;
        margin-bottom: 0;
        text-indent: 0.2rem;
    }
    div .vcricle{
        margin-left: 0.2rem;
        width:0.8rem;
        text-align: center;
        height: 0.3rem;
        line-height: 0.3rem;
        margin-top: 0.01rem;
        margin-bottom: 0rem;
        font-size: 0.12rem;
        border: 0.005rem solid #ccc;
        border-radius: 0.1rem;
    }
    div .indentxxt{
        width:100%;
        margin: 0.1rem auto;
        font-size: 0.14rem;
        text-align: center;
    }
    div .foootbut{
        position: fixed;
        bottom: 0rem;
        height: 0.6rem;
        background-color: #cccccc;
        border: none;
    }

</style>