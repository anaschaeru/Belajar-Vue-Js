<template>
  <div>
    <Navbar />
    <div class="container mt-5">
      <Hero />
      <BestFoods />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import BestFoods from "@/components/BestFoods.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    Hero,
    BestFoods
  }
};
</script>
 