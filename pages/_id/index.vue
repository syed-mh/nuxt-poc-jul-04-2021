<template>
  <div class="boxed">
    <h1>
      {{ d.name }}
    </h1>
    <h2>
      {{ d.brand }}
    </h2>
    <h3>
      Ingredients
    </h3>
    <ul>
      <li v-for="i in d.ingredient_list" :key="i">
        {{ i }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      d: {}
    };
  },
  async fetch() {
    this.d = await fetch(
      `https://skincare-api.herokuapp.com/products/${this.$route.params.id}`
    ).then(res => res.json());
  }
};
</script>
