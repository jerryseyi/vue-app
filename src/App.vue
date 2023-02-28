<script>
  export default {

    data() {
      return {
        authenticated: false,
        admin: true,
        products: [
          {id: 0, name: 'phone', type: 'Iphone'},
          {id: 1, name: 'phone', type: 'Samsung'},
          {id: 2, name: 'laptop', type: 'hp'},
          {id: 3, name: 'laptop', type: 'macbook'},
          {id: 4, name: 'laptop', type: 'Dell'}
        ]
      }
    },

    methods: {
      remove(id) {
        this.products.splice(id, 1);
      }
    },

    computed: {
      productLaptops () {
        return this.products.filter(product => product.name === 'laptop');
      },

      productPhones () {
        return this.products.filter(product => product.name === 'phone');
      }
    }

  }
</script>

<template>
  <div>
    <h3>Products</h3>
    <div v-for="product in products">
      {{product.name }} {{ product.type}}
      <a href="#" @click.prevent="remove(product.id)">remove</a>
    </div>

    <br><br>
    <h3>Laptop Products</h3>
    <div v-for="laptop in productLaptops">
      {{ laptop.name }} {{ laptop.type }}
    </div>
    <br><br><br><br>

    <h3>Phone Products</h3>
    <div v-for="phone in productPhones">
      {{phone.name }} {{ phone.type }}
    </div>
  </div>
</template>

<style scoped>

</style>
