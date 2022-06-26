<template>
  <div>
    <DesktopNav />
    <HomeCarousel :sale_items="sale_items" />
    <br /><br />
    <v-container>
      <h1 class="text-md-h4 text-h6">Check these out 🔥</h1>
      <br />
      <ProductSlider :products="products" />
      <br /><br /><br />
      <Newsletter />
    </v-container>
    <br /><br />
    <Footer />
    <ScrollTop />
  </div>
</template>

<script>
import Nav from '~/components/Nav.vue';
import HomeCarousel from '../components/HomeCarousel.vue';
import Footer from '../components/Footer.vue';
export default {
    components: { Nav, HomeCarousel, Footer },
    async created() {
    this.sale_items = await this.$content("products")
      .where({ onSale: true })
      .fetch();
    this.products = await this.$content("products").fetch();
  },
  data() {
    return {
      products: null,
      sale_items: null,
    };
  },
};
</script>

<style>

</style>
