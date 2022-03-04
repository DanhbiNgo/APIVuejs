<template>
  <div id="app">
    <input type="text" v-model="newtask">
    <button @click="addtask()">Them</button>
    <div v-for="(task,index) in tasks" :key="index">
      <input type="checkbox" v-model="task.done" >
      <span :class="{done: task.done}">{{task.todo}}</span>
    </div>
    <hr>
    <test/>
    <hr>
    <money/>
    <hr>
    <bind/>

    <v-once/>
    <pushHTML/>
    <v-onst/>
    <keyup/>
    <bind-2/>
    <css/>
  </div>
</template>

<script>
import Money from './components/money.vue';
import test  from './components/test.vue';
import bind from './components/Bind.vue';
import VOnce from './components/V-once.vue';
import pushHTML from './components/pushHTML.vue';
import vOnst from './components/v-onst.vue';
import keyup from './components/keyup.vue';
import Bind2 from './components/bind2.vue';
import Css from './components/css.vue';

export default {
  components: {test, Money, bind, VOnce ,pushHTML,vOnst, keyup,
    Bind2,
    Css,
  },
  data(){
    return{
      newtask:'',
    tasks:[
      {
        todo:'di cho',done:false
      }
    ]
    }
  },
  methods: {
    addtask: function(){
      this.tasks.push({
        todo: this.newtask,
        done: false
      });
    }
  },
  watch:{
    newtask: function(){
      
    }
  }
}
</script>

<style>
.done{
  text-decoration: line-through;
}
</style>
