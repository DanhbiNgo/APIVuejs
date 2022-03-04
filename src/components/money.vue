<template>
    <div class="money">
        <div v-for="(product,index) in products" :key="index">
            <input type="checkbox" v-model="product.selected" @change="total" >
            <span>{{product.Name}}</span>
            <br>
            <span>{{product.Gia | chage}}</span>
            
        </div>
        <div>Total:{{money | chage}}</div>
    </div>
</template>
<script>
export default {
data(){
    return{
        money:0,
        products:[{
            Name:'giay',Gia:100000,selected:false
        },
        {Name:'tất',Gia:200000,selected:false},
        {Name:'áo',Gia:100000,selected:false}
        ]

        
    }
    
},
methods: {
  total: function(){
     var total = 0;
     this.products.forEach(element => {
         if(element.selected == true){
    total += (element.Gia);
         }
  });
    return this.money = total;
  }
},
filters:{
    chage: function(tt){
        return tt.toFixed(2).replace(/\d(?=(\d{3})+\.)/g, '$&,') + 'vnđ';
    }
}
}

</script>
<style lang="sass" scoped>
.money{
    color:red;
}
</style>