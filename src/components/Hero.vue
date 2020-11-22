<template>
  <div class="container">
    <div class="hero">
      <!-- Dekstop -->
      <div class="d-none d-md-block">
        <div class="row">
          <div class="col-md-6">
            <div class="d-flex h-100">
              <div class="justify-content-center align-self-center">
                <h1>
                  <strong>Delicious Food Menu,</strong><br />
                  In Your Gadget
                </h1>
                <p>Ayo segera pilih dan pesan mekanan favorite anda</p>
                <router-link class="btn btn btn-success btn-lg" to="/">
                  <b-icon-arrow-right></b-icon-arrow-right>
                  Pesan
                </router-link>
              </div>
            </div>
          </div>
          <div class="col-md-6">
            <img src="../assets/images/hero.png" width="100%" />
          </div>
        </div>
      </div>

      <!-- Mobile -->
      <div class="d-sm-block d-md-none">
        <div class="row">
          <div class="col-md-6 mb-3">
            <img src="../assets/images/hero.png" width="100%" />
          </div>
          <div class="col-md-6">
            <div class="d-flex h-100">
              <div class="justify-content-center align-self-center">
                <h1>
                  <strong>Delicious Food Menu,</strong><br />
                  In Your Gadget
                </h1>
                <p>Ayo segera pilih dan pesan mekanan favorite anda</p>
                <router-link class="btn btn btn-success btn-lg" to="/">
                  <b-icon-arrow-right></b-icon-arrow-right>
                  Pesan
                </router-link>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>