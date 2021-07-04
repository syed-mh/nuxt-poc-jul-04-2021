<template>
  <article class="product-card card">
    <AspectRatio :image="image" :title="title" aspect-ratio="16x9" />
    <h3 class="product-card__title">
      <NuxtLink :to="`/products/${id}`">
        {{ title }}
      </NuxtLink>
    </h3>
    <span class="product-card__brand">
      {{ brand }}
    </span>
    <span class="product-card__price"> ${{ price }} </span>
  </article>
</template>

<script>
export default {
  props: {
    image: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    brand: {
      type: String,
      required: true
    },
    id: {
      required: true
    },
    price: {
      type: [String, Number],
      required: true
    }
  }
};
</script>

<style lang="scss" scoped src="./index.scss" />
