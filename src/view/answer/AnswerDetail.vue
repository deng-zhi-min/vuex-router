<template>
    <div>
        <h2>回答的详情页</h2>
        {{id}}的博客
    </div>
</template>

<script>
export default {
    props:['id'],
    computed:{
        routerInfo(){
            const{fullPath,path,title,params,query,meta}=this.$router;
            return {
                fullPath,path,title,params,query,meta
            }; 
        }
    }
}
</script>