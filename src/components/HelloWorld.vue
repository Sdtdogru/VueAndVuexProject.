<template>
  <div class="hello">

    <p v-if="products.length==0 ">Ürun Listesi Boş</p>
    <div v-else class="producdiv">
      <div v-for="product in products" :key="product.id" class="card" >
        <img alt="Vue logo" src="../assets/logo.png">
        <div class="card-body">
          <h5 class="card-title">{{product.productName}}</h5>
          <p class="card-text">{{product.quantityPerUnit}}Some quick example text to build ...</p>
          <span class="currency">US $</span><span class="num">{{product.unitPrice}}</span>
          <h1>{{ msg }}</h1>
          <router-link class=" btn btn-dark" :to="{path : 'detail/' + product.id}">Detaylar</router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {

    products:Array,

  },
  computed:{

  },
  methods:{

}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .hello{
    text-align: center;
  }

  div{
    margin: 30px;
    padding: 3px;
    display: inline-block;
    float: left;
  }
  .producdiv{
    width:100%;
  }
  .card{
    width: 25%;
  }

</style>
