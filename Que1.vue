<template>
  <div>
    <b-table striped hover :products="products" ></b-table>
      <b-form>
        <b-form-input
          v-model="hello"
          id="id"
          label="productname"
          placeholder="enter your product name"
        >
        </b-form-input>
        <b-form-input
          v-model="hello1"
          id="id1"
          label="productcategory"
          placeholder="enter your product category"
        >
        </b-form-input>
        <b-form-input
          v-model="hello2"
          id="id2"
          label="productprice"
          placeholder="enter your product price"
        ></b-form-input>
        {{ hii }}
        {{ one }}
        <b-button @click="add_product()">ADD</b-button>
      </b-form>

  </div>
</template>

<script>
export default {
  name: "NaveeN",
  components: {
  
  },
  data() {
    return {
      product: [{ productname: "nokia", productcategory :"mobiles", price:"10000" },
      { productname: "oneplus", productcategory:"mobiles", price:"20000" } ],
     
      hello: "",
      hii: "",
      hello1: "",
      one: "",
      hello2:"",
      two:"",
    };
  },
  methods: {
  
    add_product() {
      this.hii = this.hello;
      this.one = this.hello1;
      this.two=this.hello2;
    },
  },
};
</script>

<style>
</style>