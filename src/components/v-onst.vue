<template>
    <div @mouseover="showone">{{x}}/{{y}}
<div @mouseove.stop="">stop</div>
    </div>
    
</template>
<script>
// 
export default {
  data(){
      return{
          x:0,
          y:0
      }
  },
  methods:{
      showone: function(event){
        this.x =event.clientX;
        this.y = event.clientY;
        return this.x,this.y;
      }
  }
}
</script>

<style scoped>

</style>