<template>
  <div>
    <b-form-input
      v-model="name"
      placeholder="add product name"
      required
    ></b-form-input>
    <b-form-input
      v-model="price"
      placeholder="add product price"
      required
    ></b-form-input>
    <b-form-input
      v-model="category"
      placeholder="add product category"
      required
    ></b-form-input>
    <b-button @click="addproduct()">Add</b-button>
    <b-table striped hover :items="products" :fields="fields"> </b-table>
  </div>

</template>
<script>
export default {
  name: "proDuct",
  data() {
    return {
      products: [
        { product_name: "nokia", product_price: 20000, product_category: "mobiles" },
        { product_name: "oneplus", product_price: 50000, product_category: "mobiles" },
        
      ],
      fields: ["product_name", "product_price", "product_category"],
      name: "",
      price: "",
      category: "",
    };
  },
  methods: {
    addproduct() {
      this.products.push({
        product_name: this.name,
        product_price: this.price,
        product_category: this.category,
      });
    },
  },
};
</script>
