<template>
    <div class="test">
      <input type="text" v-model="newlgs">
      <button @click="Add()">Thêm</button>
      <div v-for="(lg,index) in lgs" :key="index" @click="lg.selected = !lg.selected" :class="{selected:lg.selected}">
      <span>{{lg.content}}</span>
      </div>
    </div>
</template>
<script>
export default {
  data(){
    return{
      newlgs:'',
     lgs:[
       {
         content:'php',selected:false
       },
       {
         content:'js',selected:false
       }
     ]

    
    }
  },
  methods:{
    Add: function(){
      this.lgs.push({
        content:this.newlgs,selected:false
      });
    }
  }
}
</script>
<style scoped>
.test div{
  display: inline-block;
  border: 1px solid black;
  border-radius: 5px;
  margin: 5px 5px;
  padding: 5px;
}
.selected{
  background: greenyellow;
}
</style>