<template>
    <div>
        <input type="text" v-model="name">
        <span>{{name}}</span>
    </div>
</template>
<script>

// v-bind: xử lí link
export default {
    data(){
        return {
             name:'ok'  
            
        }
    }
}
</script>
<style scoped>

</style>