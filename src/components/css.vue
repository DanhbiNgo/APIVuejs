<template>
    <div>
        <div class="vuong" :class="{do: done}" @click="done =!done"></div>
        <div class="vuong" :class="{do: done}" ></div>
        <div class="vuong" :class="{do: done}" ></div>
        <div class="vuong" :class="[color,{do: done}]"></div>
        <input type="text" v-model="color">
    </div>
</template>
<script>


export default {
   data(){
       return{
           done:false,
           color:'xanhcay'
       }
   },
   computed:{
      
   },
   methods: {
      
   }
}
</script>
<style scoped>
.vuong{

    width: 100px;
    height: 100px;
    background: #cccc;
    margin: 5px;
}
.do{
    background: red;
}
.xanhcay{
    background: green;
}
.xanhduong{
    background: blue;
}
</style>