<template>
    <div>
        <input type="text" @keyup.enter="nhap" v-model="dem">
        <button @click="dem++">++</button>
        <button @click="dem--">--</button>
        <span>{{dem > 20 ? 'dem vuot ngưỡng' : 'dem van ok'}}</span>
    </div>
</template>
<script>

// v-bind: xử lí link
export default {
    data(){
        return {
             dem:0
            
        }
    }
    ,methods:{
        nhap: function(){
            alert('endter');
        }
    }
}
</script>
<style scoped>

</style>