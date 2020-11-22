<template>
  <div>
    <Navbar />
    <div class="container">
      <div class="container mt-4">
        <div class="row">
          <div class="col">
            <nav aria-label="breadcrumb">
              <ol class="breadcrumb">
                <li class="breadcrumb-item">
                  <router-link to="/">Home</router-link>
                </li>
                <li class="breadcrumb-item">
                  <router-link to="/foods">Foods</router-link>
                </li>
                <li class="breadcrumb-item active" aria-current="page">
                  Food Order
                </li>
              </ol>
            </nav>
          </div>
        </div>

        <div class="row">
          <div class="col-md-6">
            <img class="img-fluid" :src="'../assets/images/' + product.gambar" alt="" />
          </div>
          <div class="col-md-6">
            <h2>
              <b>{{ product.nama }}</b>
            </h2>
            <hr>
            <h3><b>Rp. {{product.harga}}</b></h3>
            <div class="form-group">
                <label for="jumlah-pesanan">Jumlah Pesanan:</label>
                <input class="form-control" type="number">
            </div>
            <div class="form-group">
                <label for="jumlah-pesanan">Keterangan:</label>
                <textarea class="form-control" placeholder="Keterangan seperti: Pedas, Nasi Setengah .."></textarea>
            </div>
            <button type="submit" class="btn btn-success"><b-icon-cart></b-icon-cart> Pesan</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import axios from "axios";

export default {
  name: "FoodDetail",
  components: {
    Navbar,
  },

  data() {
    return {
      product: {},
    };
  },

  methods: {
    setProduct(data) {
      this.product = data;
    },
  },

  mounted() {
    axios
      .get("http://localhost:3000/products/" + this.$route.params.id)
      .then((response) => this.setProduct(response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style>
</style>