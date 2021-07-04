<template>
  <div class="boxed">
    <h1>
      {{ product.name }}
    </h1>
    <h2>
      {{ product.brand }}
    </h2>
    <h3>
      Ingredients
    </h3>
    <ul>
      <li v-for="ingredient in product.ingredient_list" :key="ingredient">
        {{ ingredient }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      product: {}
    };
  },
  async fetch() {
    this.product = await fetch(
      `https://skincare-api.herokuapp.com/products/${this.$route.params.id}`
    ).then(_response => _response.json());
  }
};
</script>
