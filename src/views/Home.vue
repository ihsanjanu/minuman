<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <hero />

      <div class="row mt-4">
        <div class="col">
          <h2>Best <strong>Seller</strong></h2>
        </div>
        <div class="col">
          <router-link to="/Drink" class="btn btn-succes float-right"
            ><b-icon-eye></b-icon-eye>Lihat semua</router-link
          >
        </div>
      </div>

      <div class="row mb-4">
        <div
          class="col-md-4 mt-4"
          v-for="product in products"
          :key="product.id"
        >
          <CardProduct :product="product" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import hero from "@/components/hero.vue";
import CardProduct from "@/components/CardProduct.vue";
import axios from "axios";

export default {
  name: "Home",
  components: {
    Navbar,
    hero,
    CardProduct,
  },
  data() {
    return {
      products: [],
    };
  },
  methods: {
    setProducts(data) {
      this.products = data;
    },
  },
  mounted() {
    axios
      .get("http://localhost:3000/best-seller")
      .then((response) => this.setProducts(response.data))
      .catch((error) => console.log(error));
  },
};
</script>