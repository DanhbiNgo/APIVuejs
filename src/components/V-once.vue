<template>
    <div v-once>{{one}}-{{showone()}}</div>
</template>
<script>
// v-once: giá trị đầu không thay đổi
export default {
  data(){
      return{
          one:"day la tao"
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