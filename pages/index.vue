<template>
  <div class="grid">
    <NuxtLink
      v-for="product in products"
      :key="product.id"
      :to="`/${product.id}`"
    >
      {{ product.name }}
    </NuxtLink>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: []
    };
  },
  async fetch() {
    this.products = await fetch("https://skincare-api.herokuapp.com/products", {
      mode: "no-cors"
    }).then(_response => _response.json());
  }
};
</script>

<style lang="scss" scoped src="./index.scss" />
