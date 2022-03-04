<template>
    <div v-once>{{one}}-{{showone()}}
        <p v-html="mahtml"></p>
    </div>
</template>
<script>
// đẩy data html
export default {
  data(){
      return{
          one:"day la tao",
          mahtml:'<a href="">link</a>'
      }
  },
  methods:{
      showone: function(){
          this.one = 'tao la ai';
          return this.one;
      }
  }
}
</script>

<style scoped>

</style>