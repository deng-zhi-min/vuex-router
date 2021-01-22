<template>
    <div>
        <h2>回答列表页</h2>
        <router-link :to="{name:'answerView',params:{id:'zhangsan'}}">张三的回答</router-link>
        <br />
        <br />
        <router-link :to="{ name: 'answerView', params: { id: 'lisi' } }">李四的回答</router-link>
    </div>
</template>

<script>
export default {
    name:'answerList',
    props:['id'],
    computed:{
        touteInfo(){
            const{fullPath,path,title,params,query,meta}=this.$route;
            return {
                fullPath,path,title,params,query,meta
            };
        }
    }
}
</script>